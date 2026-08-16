# Documento de Especificación Arquitectónica de Software (SAD)
## Proyecto: ShopExpress — Plataforma de Comercio Electrónico

> Este documento integra todos los artefactos desarrollados durante la
asignatura, siguiendo los lineamientos de RUP y el modelo 4+1 de
Kruchten. Cada sección enlaza al artefacto detallado correspondiente.

## Índice

1. Introducción
2. [Documento de Visión](fase1-vision-y-requisitos/01-documento-vision.md)
3. [Especificación de Requisitos](fase1-vision-y-requisitos/02-especificacion-requisitos.md)
4. [Modelo Conceptual del Dominio](fase2-modelo-y-decisiones/01-modelo-conceptual-dominio.md)
5. [Decisiones Arquitectónicas](fase2-modelo-y-decisiones/02-decisiones-arquitectonicas.md)
   - [ADR-001: Estilo arquitectónico](fase2-modelo-y-decisiones/adr/ADR-001-estilo-arquitectonico.md)
   - [ADR-002: Lenguaje y framework](fase2-modelo-y-decisiones/adr/ADR-002-lenguaje-y-framework.md)
   - [ADR-003: Base de datos](fase2-modelo-y-decisiones/adr/ADR-003-base-de-datos.md)
   - [ADR-004: Containerización con Docker](fase2-modelo-y-decisiones/adr/ADR-004-containerizacion-docker.md)
   - [ADR-005: Estilo de API REST](fase2-modelo-y-decisiones/adr/ADR-005-estilo-api-rest.md)
   - [ADR-006: Autenticación con JWT](fase2-modelo-y-decisiones/adr/ADR-006-autenticacion-jwt.md)
6. Vistas Arquitectónicas (Modelo 4+1)
   - Vista de Contexto — **(Fase 3)** [01-Vista-Contexto](fase3-vistas-arquitectonicas/01-vista-contexto.md)
   - Vista Conceptual — **(Fase 3)** [02-Vista-Conceptual](fase3-vistas-arquitectonicas/02-vista-conceptual.md)
   - Vista de Casos de Uso — **(Fase 3)** [03-Casos-de-uso](fase3-vistas-arquitectonicas/03-vista-casos-de-uso.md)
   - Vista Lógica — **(Fase 3)** [04-Vista-Logica](fase3-vistas-arquitectonicas/04-vista-logica.md)
   - Vista de Implementación — **(Fase 3)** [05-Vista-Implementacion](fase3-vistas-arquitectonicas/05-vista-implementacion.md)
   - Vista Física (Despliegue) — **(Fase 3)** [06-Vista-Fisica](<fase3-vistas-arquitectonicas/06-vista - fisica.md>)
7. Conclusiones — **(Fase 4)** [Conclusiones](fase4-consolidacion-sad/fase4-consolidacion-sad.md)

## 1. Introducción

Este documento presenta la Especificación Arquitectónica de Software
(SAD) para ShopExpress, una plataforma de comercio electrónico de
tienda única. El documento se elabora siguiendo el Proceso Unificado
de Rational (RUP) y organiza las vistas arquitectónicas según el
modelo 4+1 de Kruchten (vista lógica, de procesos, de desarrollo,
física y de casos de uso), con el fin de describir de forma completa
y coherente las decisiones de diseño, los requisitos que las motivan
y su representación arquitectónica.