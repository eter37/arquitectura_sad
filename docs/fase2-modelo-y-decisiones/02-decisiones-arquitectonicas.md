# Decisiones Arquitectónicas

## 1. Selección del estilo arquitectónico

Se selecciona una **arquitectura monolítica organizada en capas
(layered monolith / monolito modular)**.

El sistema se construye y despliega como una única aplicación, pero
internamente se organiza en:

1. **Capa de Presentación**: interfaz web con la que interactúa el
   usuario (cliente y administrador).
2. **Capa de Lógica de Negocio (Servicios de Aplicación)**: reglas de
   negocio de cada módulo funcional (Usuarios, Catálogo, Carrito,
   Pedidos, Pagos).
3. **Capa de Dominio**: entidades y reglas propias del negocio,
   independientes de la tecnología.
4. **Capa de Acceso a Datos**: persistencia de la información en una
   base de datos relacional.

Adicionalmente, dentro de la capa de lógica de negocio, el código se
organiza por **módulos funcionales independientes** (usuarios, catálogo,
carrito, pedidos, pagos), cada uno con su propia lógica y modelos,
comunicándose entre sí mediante interfaces internas bien definidas.
Esto facilita que, si en el futuro el sistema crece, alguno de estos
módulos pueda extraerse como un servicio independiente sin rediseñar
todo el sistema.

## 2. Justificación de la decisión

| Criterio | Justificación |
|---|---|
| **Simplicidad** | Un solo despliegue reduce la complejidad operativa, adecuada para una tienda única (no multi-vendedor). |
| **Coherencia transaccional** | Operaciones críticas como "confirmar pedido → descontar stock → generar pago" requieren consistencia fuerte; en un monolito esto se resuelve con transacciones locales, evitando la complejidad de transacciones distribidas propias de microservicios. |
| **Costo y equipo reducido** | El proyecto es desarrollado por un equipo pequeño (académico); un monolito organizado en capas y módulos es más rápido de construir y mantener que una arquitectura distribuida. |
| **Mantenibilidad** | La separación en capas y módulos internos evita el problema de un monolito "desordenado", permitiendo ubicar y modificar funcionalidad fácilmente. |
| **Escalabilidad futura** | Si el negocio crece (por ejemplo, se necesita escalar solo el catálogo o los pagos), la separación modular interna facilita una futura migración parcial a microservicios sin reescribir todo el sistema. |
| **Desempeño** | Al no requerir llamadas de red entre módulos (como sí ocurre en microservicios), se reduce la latencia entre las operaciones internas del sistema. |

## 3. Estilos considerados y descartados

- **Microservicios**: se descartó por la sobrecarga operativa
  (despliegue, monitoreo y comunicación entre servicios) que no se
  justifica para el alcance y tamaño de este proyecto (tienda única,
  equipo pequeño).
- **Monolito clásico sin separación modular interna**: se descartó
  porque, aunque es más simple de iniciar, tiende a generar alto
  acoplamiento entre módulos a medida que el sistema crece, dificultando
  el mantenimiento.
- **Arquitectura basada en eventos (event-driven) pura**: se consideró
  para el flujo de pedidos y pagos, pero se descartó como estilo
  arquitectónico principal por la complejidad adicional; sin embargo,
  se recomienda evaluarlo puntualmente para la comunicación entre el
  módulo de Pedidos y el módulo de Pagos en una evolución futura del
  sistema.

## 4. Relación con los atributos de calidad

- **Rendimiento**: se favorece al evitar comunicación de red entre
  módulos internos.
- **Mantenibilidad**: se favorece mediante la organización en capas y
  módulos con responsabilidades claras.
- **Seguridad**: se centraliza el manejo de autenticación en el módulo
  de Usuarios y se delega el manejo de datos sensibles de pago a la
  pasarela externa.
- **Escalabilidad**: aunque el despliegue es único, la separación
  modular interna deja preparado el sistema para una eventual
  extracción de módulos como servicios independientes.