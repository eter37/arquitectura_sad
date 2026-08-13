# Especificación de Requisitos

## 1. Requisitos funcionales por módulo

### Módulo de Usuarios
- RF-01: El sistema debe permitir a un cliente registrarse con nombre,
  correo electrónico y contraseña.
- RF-02: El sistema debe permitir a un usuario registrado iniciar sesión
  mediante correo y contraseña.
- RF-03: El sistema debe permitir al usuario editar los datos de su
  perfil (nombre, dirección, teléfono).
- RF-04: El sistema debe permitir al usuario recuperar su contraseña
  mediante correo electrónico.
- RF-05: El sistema debe permitir al administrador gestionar cuentas de
  usuario (bloquear, activar).

### Módulo de Catálogo
- RF-06: El sistema debe permitir al administrador crear, editar y dar
  de baja productos (nombre, descripción, precio, stock, categoría,
  imagen).
- RF-07: El sistema debe permitir a cualquier usuario consultar el
  catálogo de productos sin necesidad de autenticarse.
- RF-08: El sistema debe permitir buscar productos por nombre o
  categoría.
- RF-09: El sistema debe mostrar el detalle de un producto, incluyendo
  disponibilidad de stock.

### Módulo de Carrito de Compras
- RF-10: El sistema debe permitir a un usuario autenticado agregar
  productos al carrito.
- RF-11: El sistema debe permitir modificar la cantidad de un producto
  en el carrito.
- RF-12: El sistema debe permitir eliminar productos del carrito.
- RF-13: El sistema debe calcular automáticamente el subtotal y total del
  carrito.
- RF-14: El sistema debe validar la disponibilidad de stock antes de
  confirmar el pedido.

### Módulo de Pedidos
- RF-15: El sistema debe permitir generar un pedido a partir del
  contenido del carrito.
- RF-16: El sistema debe registrar el estado del pedido (pendiente,
  pagado, enviado, cancelado).
- RF-17: El sistema debe permitir al usuario consultar el historial de
  sus pedidos.
- RF-18: El sistema debe descontar el stock del catálogo al confirmarse
  un pedido.

### Módulo de Pagos
- RF-19: El sistema debe permitir seleccionar un método de pago
  disponible al confirmar el pedido.
- RF-20: El sistema debe integrarse con una pasarela de pagos externa
  para procesar la transacción.
- RF-21: El sistema debe actualizar el estado del pedido según la
  respuesta de la pasarela de pagos (aprobado o rechazado).
- RF-22: El sistema debe generar un comprobante de pago asociado al
  pedido.

## 2. Requisitos no funcionales (atributos de calidad)

| Categoría | Requisito |
|---|---|
| **Rendimiento** | El sistema debe responder a las consultas de catálogo en menos de 2 segundos bajo condiciones normales de carga. |
| **Escalabilidad** | La arquitectura debe permitir aumentar la capacidad de los módulos con mayor demanda (catálogo, pedidos) sin rediseñar el sistema completo. |
| **Disponibilidad** | El sistema debe estar disponible al menos el 99% del tiempo mensual. |
| **Seguridad** | Las contraseñas deben almacenarse cifradas (hash) y las comunicaciones deben usar HTTPS. |
| **Seguridad de pagos** | La información de pago no debe almacenarse directamente en el sistema; se delega a la pasarela de pagos externa (cumplimiento tipo PCI-DSS). |
| **Mantenibilidad** | El código debe organizarse por módulos y capas bien definidas para facilitar cambios futuros. |
| **Usabilidad** | La interfaz debe ser responsiva y utilizable desde dispositivos móviles y de escritorio. |
| **Portabilidad** | El sistema debe poder desplegarse en distintos entornos (desarrollo, pruebas, producción) mediante configuración externa. |

## 3. Restricciones técnicas y organizacionales

- El sistema se implementará como una **aplicación web monolítica
  organizada en capas** (presentación, lógica de negocio, dominio y
  acceso a datos), estructurada internamente por módulos funcionales.
- El pago se procesa mediante una **pasarela de pagos externa**; el
  sistema no maneja directamente los datos sensibles de tarjetas.
- El proyecto debe desarrollarse de forma colaborativa entre los
  integrantes del equipo, versionado en GitHub.
- El desarrollo debe seguir los lineamientos de RUP y el modelo 4+1 de
  Kruchten para la documentación arquitectónica.
- Tiempo y recursos limitados al contexto académico del curso (sin
  presupuesto de infraestructura en producción real).