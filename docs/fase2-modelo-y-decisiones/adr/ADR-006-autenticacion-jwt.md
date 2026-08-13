# ADR-006: Autenticación basada en JWT

**Fecha:** 2026-08-12
**Estado:** Aceptada

## Contexto

El sistema necesita distinguir entre usuarios autenticados y no
autenticados (RF-02, RF-07), y entre roles (cliente/administrador,
RF-05), sin mantener sesiones con estado en el servidor, para
mantener el backend simple de escalar horizontalmente si fuera
necesario.

## Decisión

Se utilizará **autenticación basada en tokens JWT (JSON Web Token)**,
integrada con Spring Security (ADR-002): al iniciar sesión, el sistema
emite un token firmado que el cliente envía en cada petición mediante
el encabezado `Authorization`.

## Consecuencias

**Positivas**
- Autenticación sin estado (*stateless*), coherente con una API REST
  (ADR-005).
- Permite validar fácilmente el rol del usuario (cliente/administrador)
  en cada endpoint.
- Facilita una eventual extracción de módulos como servicios
  independientes en el futuro, sin depender de sesiones compartidas.

**Negativas**
- La revocación de tokens antes de su expiración requiere mecanismos
  adicionales (por ejemplo, lista negra), lo cual no se contempla en el
  alcance inicial.

## Alternativas consideradas

- **Sesiones de servidor con cookies**: descartado por depender de
  estado en el servidor, lo cual complica una eventual escalabilidad
  horizontal del sistema.