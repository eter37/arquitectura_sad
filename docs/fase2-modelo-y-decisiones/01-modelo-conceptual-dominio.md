# Modelo Conceptual del Dominio

## 1. Entidades principales

- **Usuario**: persona registrada en el sistema que puede comprar
  productos. Atributos principales: id, nombre, correo, contraseña
  (hash), dirección, teléfono, rol (cliente/administrador).
- **Producto**: artículo disponible para la venta. Atributos: id,
  nombre, descripción, precio, stock, categoría, imagen.
- **Categoría**: clasificación de los productos del catálogo. Atributos:
  id, nombre, descripción.
- **Carrito**: contenedor temporal de los productos que un usuario
  desea comprar, asociado a un único usuario. Atributos: id, usuario,
  fecha de creación, estado (activo/convertido).
- **ÍtemCarrito**: relación entre un carrito y un producto, con la
  cantidad seleccionada. Atributos: id, carrito, producto, cantidad,
  precio unitario.
- **Pedido**: orden de compra generada a partir de un carrito
  confirmado. Atributos: id, usuario, fecha, estado (pendiente, pagado,
  enviado, cancelado), total.
- **ÍtemPedido**: detalle de los productos incluidos en un pedido,
  con la cantidad y el precio al momento de la compra. Atributos: id,
  pedido, producto, cantidad, precio unitario.
- **Pago**: transacción asociada a un pedido. Atributos: id, pedido,
  monto, método de pago, estado (aprobado/rechazado), fecha,
  referencia de la pasarela externa.

## 2. Relaciones entre las entidades del dominio

- Un **Usuario** puede tener **uno o varios Pedidos** (1 : N).
- Un **Usuario** tiene **un Carrito activo** en un momento dado
  (1 : 1, mientras el carrito está activo).
- Un **Carrito** contiene **uno o varios ÍtemCarrito** (1 : N), y cada
  ÍtemCarrito referencia **un Producto** (N : 1).
- Un **Pedido** se genera a partir de **un Carrito** confirmado
  (1 : 1) y contiene **uno o varios ÍtemPedido** (1 : N).
- Un **Producto** pertenece a **una Categoría** (N : 1), y una
  Categoría puede tener **varios Productos** (1 : N).
- Un **Pedido** tiene **un único Pago asociado** (1 : 1); si el pago es
  rechazado, puede generarse un nuevo intento de Pago para el mismo
  Pedido.

## 3. Diagrama conceptual (descripción para modelar en herramienta UML)

Se recomienda representar este modelo como un **diagrama de clases de
dominio** (no de implementación) con las entidades y relaciones
descritas arriba. Sugerencia de notación de cardinalidades: