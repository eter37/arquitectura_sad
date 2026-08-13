# ADR-001: Adopción de arquitectura monolítica en capas (modular)

**Fecha:** 2026-08-12
**Estado:** Aceptada

## Contexto

El sistema ShopExpress es una plataforma de comercio electrónico de
tienda única, desarrollada por un equipo académico pequeño, con
operaciones críticas (confirmar pedido → descontar stock → procesar
pago) que requieren fuerte consistencia transaccional. Se debe elegir
un estilo arquitectónico que equilibre simplicidad de desarrollo,
mantenibilidad y capacidad de evolución futura.

## Decisión

Se adopta una **arquitectura monolítica organizada en capas**
(presentación, lógica de negocio, dominio, acceso a datos), con la
capa de lógica de negocio subdividida internamente en **módulos
funcionales independientes**: Usuarios, Catálogo, Carrito, Pedidos y
Pagos, cada uno con responsabilidades y modelos propios.

## Consecuencias

**Positivas**
- Despliegue y operación simples (un solo artefacto).
- Consistencia transaccional fuerte sin necesidad de transacciones
  distribuidas.
- Menor curva de aprendizaje y costo operativo para un equipo pequeño.
- La separación modular interna facilita ubicar y modificar
  funcionalidad, y deja abierta la puerta a una futura extracción de
  módulos como servicios independientes.

**Negativas**
- Todo el sistema escala como una unidad (no se puede escalar solo el
  módulo de Catálogo, por ejemplo, sin escalar el resto).
- Un error grave en un módulo puede afectar la disponibilidad de toda
  la aplicación.
- Requiere disciplina del equipo para mantener los límites entre
  módulos y no generar acoplamiento excesivo.

## Alternativas consideradas

- **Microservicios**: descartados por la sobrecarga operativa
  (despliegue, monitoreo, comunicación entre servicios) injustificada
  para el alcance del proyecto.
- **Monolito sin separación modular interna**: descartado por el riesgo
  de alto acoplamiento a medida que el sistema crece.