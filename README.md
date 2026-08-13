# Arquitectura SAD — ShopExpress

Documento de Especificación Arquitectónica de Software (SAD) para
ShopExpress, una plataforma de comercio electrónico de tienda única,
elaborado siguiendo los lineamientos de RUP y el modelo 4+1 de
Kruchten.

## Documento principal

El documento consolidado se encuentra en [`docs/SAD.md`](docs/SAD.md).

## Caso de estudio

**Opción 1: Plataforma de comercio electrónico** (tienda única) —
gestión de usuarios, catálogo de productos, carrito de compras,
procesamiento de pedidos e integración con pagos.

## Estilo arquitectónico

Arquitectura monolítica organizada en capas (presentación, lógica de
negocio, dominio, acceso a datos), con módulos funcionales internos
independientes. Ver justificación completa en
[ADR-001](docs/fase2-modelo-y-decisiones/adr/ADR-001-estilo-arquitectonico.md).

## Stack tecnológico

- **Lenguaje / Framework:** Java 17 + Spring Boot
- **Base de datos:** PostgreSQL
- **Contenerización:** Docker + Docker Compose
- **API:** REST (JSON)
- **Autenticación:** JWT

## Equipo

- [Santiago Rodriguez Ospina — Fase 1 (Visión y requisitos) y Fase 2 (Modelo conceptual y decisiones arquitectónicas)
- [Juanita cortes lopez — Fase 3 (Vistas arquitectónicas) y fase 4

