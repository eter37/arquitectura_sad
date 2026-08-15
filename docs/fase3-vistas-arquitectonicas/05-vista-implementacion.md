# 05 - Vista Implementacion

## 1. Introducción
La Vista de Implementación permite representar cómo se organizan los componentes de software que conforman ShopExpress. En esta Vista se busca mostrar cómo las diferentes partes del Sistema se encuentran separadas y cómo se relacionan para cumplir con las funciones definidas.

Esta Vista toma como base la organización realizada en la Vista Lógica, pero presenta los elementos desde una perspectiva más cercana a la implementación del Sistema.

## 2. Componentes de Software 
Para ShopExpress se consideran los siguientes componentes principales:

Interfaz de Usuario
Gestión de Usuarios
Gestión de Productos
Gestión de Inventario
Gestión de Carrito
Gestión de Pedidos
Gestión de Pagos
Base de Datos

## 3. Relación entre Componentes
**1:** La Interfaz de Usuario permite que el Administrador y el Cliente Final interactúen con ShopExpress.

**2:** Las solicitudes realizadas desde la interfaz son atendidas por los componentes correspondientes a cada función del Sistema.

**3:** Los componentes de Usuarios, Productos, Inventario, Carrito, Pedidos y Pagos trabajan de manera conjunta para cumplir con las diferentes operaciones de la plataforma.

**4:** La Base de Datos permite almacenar la información utilizada por los diferentes componentes del Sistema.

**5:** La Gestión de Pagos también se comunica con la Pasarela de Pagos, debido a que esta corresponde a un servicio externo utilizado para procesar las transacciones.

## 4. Diagrama de Implementación
El siguiente Diagrama representa los principales componentes de Software que conforman ShopExpress y la forma en que estos se relacionan para permitir el funcionamiento del problema.

![Diagrama de Implementación](<diagrama - implementacion.jpg>)

## 5. Explicación del Diagrama
El Diagrama de Implementación muestra cómo se organizan los diferentes componentes que hacen parte de ShopExpress y cómo se comunican entre ellos para cumplir con las funciones del Sistema.

En primer lugar se encuentra la **Interfaz de Usuario,** que representa el punto por donde el Cliente Final y el Administrador de la Tienda interactúan con ShopExpress. Desde esta interfaz se pueden realizar las diferentes acciones disponibles dependiendo del tipo de Usuario.

A partir de la Interfaz de Usuario se encuentran los componentes encargados de las diferentes funciones del Sistema. **Gestión de Usuarios** se encarga de la información relacionada con las cuentas, mientras que **Gestión de Productos** administra los Productos disponibles y **Gestión de Inventario** permite mantener controlada su disponibilidad.

Por otra parte, **Gestión de Carrito** administra los Productos seleccionados por el Cliente y se relaciona con **Gestión de Pedidos,** donde se registra la compra realizada. Posteriormente, Gestión de Pagos se encarga del proceso correspondiente al pago del Pedido.

Los diferentes componentes también se relacionan con la **Base de Datos,** donde se almacena la información necesaria para el funcionamiento del Sistema.

Finalmente, **Gestión de Pagos** se comunica con la **Pasarela de Pagos,** que corresponde a un Servicio Externo utilizado para procesar las transacciones. De esta manera, ShopExpress puede utilizar este servicio sin que la Pasarela de Pagos forme parte de la estructura interna del Sistema.