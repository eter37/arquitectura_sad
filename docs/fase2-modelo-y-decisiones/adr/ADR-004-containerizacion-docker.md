# ADR-004: Uso de Docker para empaquetado y despliegue

**Fecha:** 2026-08-12
**Estado:** Aceptada

## Contexto

El sistema depende de un runtime específico (Java 17 / Spring Boot) y
de un motor de base de datos (PostgreSQL). El equipo necesita un
entorno de ejecución reproducible tanto en desarrollo como en una
eventual demostración/despliegue, evitando el problema de "en mi
máquina sí funciona".

## Decisión

Se utilizará **Docker** para empaquetar la aplicación monolítica en una
imagen de contenedor, y **Docker Compose** para orquestar localmente el
contenedor de la aplicación junto con el contenedor de PostgreSQL.

## Consecuencias

**Positivas**
- Entorno de ejecución reproducible e independiente del sistema
  operativo del desarrollador.
- Facilita que la vista física/de despliegue (Fase 3) describa nodos y
  contenedores de forma clara y realista.
- Simplifica la incorporación de nuevos integrantes del equipo (solo
  necesitan Docker instalado).

**Negativas**
- Añade una curva de aprendizaje adicional si el equipo no tiene
  experiencia previa con Docker.
- Requiere mantener el `Dockerfile` y `docker-compose.yml` sincronizados
  con los cambios de configuración de la aplicación.

## Alternativas consideradas

- **Despliegue directo sin contenedores**: descartado por depender del
  entorno local de cada máquina, dificultando la reproducibilidad y la
  demostración del proyecto.