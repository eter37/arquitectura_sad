# ADR-002: Selección de lenguaje de programación y framework

**Fecha:** 2026-08-12
**Estado:** Aceptada

## Contexto

Se necesita un lenguaje y framework que soporte de forma natural una
arquitectura en capas con módulos bien delimitados (RF-01 a RF-22),
que tenga buen soporte para desarrollo web, acceso a datos
transaccional y que sea ampliamente documentado, dado que el proyecto
es desarrollado por un equipo académico con tiempo limitado.

## Decisión

Se selecciona **Java 17** como lenguaje de programación y **Spring
Boot** como framework principal, usando **Spring MVC** para la capa de
presentación (API REST), **Spring Data JPA** para la capa de acceso a
datos y **Spring Security** para autenticación y autorización.

## Consecuencias

**Positivas**
- Spring Boot favorece de forma nativa la organización en capas y
  módulos mediante paquetes y componentes (`@Service`, `@Repository`,
  `@Controller`).
- Amplio ecosistema y documentación, lo que reduce la curva de
  aprendizaje para el equipo.
- Integración madura con bases de datos relacionales y con manejo de
  transacciones (`@Transactional`), clave para RF-14 y RF-18.
- Facilita la contenerización (imágenes oficiales de Java/Spring Boot
  livianas).

**Negativas**
- Mayor consumo de memoria en tiempo de ejecución comparado con
  alternativas como Node.js.
- Requiere que todo el equipo tenga familiaridad mínima con Java y el
  ecosistema Spring.

## Alternativas consideradas

- **Node.js + Express**: descartado por ofrecer un tipado más débil
  (salvo con TypeScript) y una estructura por capas menos convencional
  “out of the box”.
- **Python + Django**: descartado por preferencia del equipo hacia un
  lenguaje fuertemente tipado para un dominio con reglas de negocio
  transaccionales (pedidos, pagos, stock).