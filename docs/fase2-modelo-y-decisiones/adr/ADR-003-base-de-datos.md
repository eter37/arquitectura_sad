# ADR-003: Selección del motor de base de datos

**Fecha:** 2026-08-12
**Estado:** Aceptada

## Contexto

El dominio del sistema (Usuario, Producto, Carrito, Pedido, Pago, ver
Modelo Conceptual) tiene relaciones bien definidas y requiere
consistencia fuerte, en particular en operaciones como el descuento de
stock al confirmar un pedido (RF-18) y la relación 1:1 entre Pedido y
Pago. Se requiere un motor de base de datos que soporte transacciones
ACID y relaciones entre entidades.

## Decisión

Se selecciona **PostgreSQL** como sistema de gestión de base de datos
relacional.

## Consecuencias

**Positivas**
- Soporte completo de transacciones ACID, necesario para mantener la
  consistencia entre Carrito, Pedido, Stock y Pago.
- Buen soporte para claves foráneas y restricciones de integridad,
  coherente con las relaciones del modelo conceptual del dominio.
- Integración directa y madura con Spring Data JPA (ADR-002).
- Es open source, sin costo de licenciamiento, adecuado para el
  contexto académico.

**Negativas**
- Menor flexibilidad que una base de datos NoSQL ante cambios de
  esquema muy frecuentes (no es un problema aquí porque el dominio es
  relativamente estable).
- Requiere definir y mantener migraciones de esquema a medida que
  evolucione el modelo.

## Alternativas consideradas

- **MongoDB (NoSQL)**: descartado porque el dominio tiene relaciones
  estructuradas y necesita consistencia transaccional fuerte (pedidos,
  pagos, stock), algo para lo que un modelo relacional es más natural.
- **MySQL**: alternativa viable, pero se prefiere PostgreSQL por su
  mejor soporte de integridad referencial avanzada y extensiones.