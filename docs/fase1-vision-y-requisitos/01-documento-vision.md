# Documento de Visión

## Proyecto:  Plataforma de Comercio Electrónico

## 1. Descripción del problema

Las pequeñas y medianas tiendas que desean vender en línea enfrentan
dificultades para ofrecer una experiencia de compra completa, segura y
escalable sin depender de plataformas de terceros que limitan su
personalización y cobran comisiones elevadas por transacción. Se requiere
una plataforma propia de comercio electrónico que permita gestionar
usuarios, productos, carritos de compra, pedidos y pagos de forma
integrada, confiable y con buen desempeño ante el crecimiento del
catálogo y de la base de clientes.

## 2. Objetivos del sistema

**Objetivo general**
Desarrollar una plataforma de comercio electrónico de tienda única que
permita a los clientes explorar un catálogo de productos, gestionar un
carrito de compras, realizar pedidos y efectuar pagos en línea de forma
segura y eficiente.

**Objetivos específicos**
- Permitir el registro, autenticación y gestión de cuentas de usuario.
- Ofrecer un catálogo de productos con búsqueda y filtrado.
- Permitir la gestión del carrito de compras (agregar, modificar, eliminar
  productos).
- Procesar pedidos de forma consistente, garantizando la integridad de la
  información entre el carrito, el inventario y el pago.
- Integrar un mecanismo de pago en línea seguro.
- Garantizar tiempos de respuesta adecuados y disponibilidad del sistema
  durante picos de tráfico (por ejemplo, temporadas de descuentos).

## 3. Alcance

El sistema cubrirá los siguientes procesos de negocio:
- Registro y autenticación de usuarios (clientes y administrador).
- Gestión del catálogo de productos (creación, edición, baja, consulta).
- Gestión del carrito de compras por usuario.
- Procesamiento de pedidos, desde la confirmación del carrito hasta la
  generación de la orden de compra.
- Integración con una pasarela de pagos externa para el cobro de pedidos.

Quedan fuera del alcance de este proyecto:
- La gestión logística de envíos (transportadoras, tracking físico).
- La administración de múltiples vendedores o tiendas (marketplace).
- Aplicaciones móviles nativas (el sistema se plantea como aplicación
  web).

## 4. Stakeholders (interesados)

| Stakeholder | Rol / Interés |
|---|---|
| Cliente final | Usuario que navega el catálogo, compra productos y realiza pagos. |
| Administrador de la tienda | Gestiona el catálogo, precios, inventario y supervisa los pedidos. |
| Equipo de desarrollo | Diseña, construye y mantiene la plataforma. |
| Proveedor de la pasarela de pagos | Servicio externo encargado de procesar transacciones de forma segura. |
| Dueño del negocio / Patrocinador | Define los objetivos comerciales y valida que el sistema cumpla las metas del negocio. |

## 5. Identificación de los módulos funcionales

- **Módulo de Usuarios:** registro, autenticación, gestión de perfil.
- **Módulo de Catálogo:** gestión y consulta de productos, categorías y
  búsqueda.
- **Módulo de Carrito de Compras:** administración de ítems seleccionados
  por el usuario antes de la compra.
- **Módulo de Pedidos:** creación, seguimiento y consulta del estado de
  las órdenes de compra.
- **Módulo de Pagos:** integración con la pasarela de pagos externa y
  confirmación de transacciones.