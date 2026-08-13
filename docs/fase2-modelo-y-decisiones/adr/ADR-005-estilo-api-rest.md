# ADR-005: Comunicación mediante API REST

**Fecha:** 2026-08-12
**Estado:** Aceptada

## Contexto

La capa de presentación (frontend web) necesita comunicarse con la
capa de lógica de negocio del monolito para consumir funcionalidades
de los módulos de Usuarios, Catálogo, Carrito, Pedidos y Pagos.

## Decisión

Se expondrá la lógica de negocio mediante una **API REST**, con
recursos organizados por módulo (`/api/usuarios`, `/api/productos`,
`/api/carrito`, `/api/pedidos`, `/api/pagos`), usando JSON como formato
de intercambio.

## Consecuencias

**Positivas**
- Estándar ampliamente conocido, fácil de documentar (por ejemplo con
  OpenAPI/Swagger) y de consumir desde cualquier cliente web.
- Permite, a futuro, separar el frontend del backend sin cambiar la
  lógica de negocio.
- Se alinea naturalmente con la organización por módulos definida en
  ADR-001.

**Negativas**
- Para operaciones muy interactivas en tiempo real (por ejemplo,
  actualización de stock en vivo) REST no es tan eficiente como
  WebSockets, aunque no es un requisito del alcance actual.

## Alternativas consideradas

- **GraphQL**: descartado por añadir complejidad innecesaria para el
  alcance y tamaño de este proyecto.