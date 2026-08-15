# 04 - Vista Lógica

## 1. Introducción
La Vista Lógica permite representar como se encuentra organizado internamente ShopExpress. Para esta Vista se mostraran los principales módulos que conforman el Sistema y la relación que existe entre ellos para cumplir con las funciones establecidas en los requisitos y también en la organización interna de sus principales responsabilidades.

## 2. Organización de los Módulos
Para esta Vista se toman como base los módulos identificados durante las fases anteriores:

**Gestión de Usuarios:** Permite administrar la información relacionada con los Usuarios.

**Gestión de Productos:** Permite administrar los Productos disponibles en la tienda.

**Gestión de Inventario:** Controla la cantidad y disponibilidad de los Productos.

**Gestión de Carrito:** Administra los Productos seleccionados por el Cliente durante el proceso de compra.

**Gestión de Pedidos:** Permite gestionar los Pedidos realizados por los Clientes.

**Gestión de Pagos:** Se encarga de gestionar el proceso relacionado con los pagos y la comunicación con la Pasarela de Pagos.

## 3. Relación entre los módulos
Los módulos se relacionan de acuerdo con el funcionamiento del proceso de compra.

La **Gestión de Productos** proporciona la información necesaria para que el Cliente pueda consultar los Productos.

La **Gestión de Carrito** utiliza la información de los Productos seleccionados y posteriormente permite generar un Pedido.

La **Gestión de Pedidos** recibe la información correspondiente a la compra y se relaciona con la Gestión de Pagos para completar el proceso.

Por otra parte, la **Gestión de Inventario** se relaciona con Productos y Pedidos para mantener actualizada la disponibilidad de los Productos.

La **Gestión de Usuarios** permite administrar la información de los Usuarios que utilizan el Sistema.

## 4. Diagrama de Vista Lógica

![Diagrama Vista Lógica](<diagrama - logica.jpg>)

**Productos --> Inventario:** Los productos tienen una disponibilidad que debe controlarse.

**Productos --> Carrito:** El cliente agrega al carrito productos existentes en el catálogo.

**Carrito --> Pedidos:** Cuando se confirma el carrito, se genera el pedido.

**Pedidos --> Pagos:** El pago corresponde al pedido realizado.

**Pedidos --> Inventario:** El pedido afecta la disponibilidad de los productos.

**Usuarios --> Productos:** Permite relacionar la gestión de usuarios con las funciones de administración de productos.

## 5. Explicación del Diagrama
El Diagrama representa la organización interna de ShopExpress mediante sus principales Módulos. Cada módulo tiene una responsabilidad específica y se relaciona con los demás para permitir el funcionamiento completo de la plataforma.

El proceso principal comienza con los Productos disponibles, continúa con el Carrito de Compras y posteriormente con los Pedidos y los Pagos. El Inventario permite mantener controlada la disponibilidad de los Productos durante este proceso, mientras que la Gestión de Usuarios administra la información correspondiente a quienes utilizan el Sistema.