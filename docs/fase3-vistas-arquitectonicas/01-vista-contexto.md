# Vista Contexto

## 1. Introducción

Para la realización de las Vistas Arquitectónicas, usé como base la Vista de Contexto, esto por que nos permite representar de manera general el sistema ShopExpress y los elementos externos que se relacionan con el. Su propósito es mostrar los límiters del Sistema y comprender quiénes y como interactúan con la plataforma.

Para esta vista se tiene en cuenta los elementos identificados durante las fases anteriores del proyecto, realizadas por el compañero. Aquí tenemos en cuenta los Stakeholders, los módulos funcionales y las restricciones establecidas, ya que en este caso ShopExpress es una plataforma que permite Gestionar Usuarios, Productos, Carritos de Compra, Pedidos y Pagos.

## 2. Elementos del Sistema

En esta Vista se identificaron los principales elementos externos que tienen una relación directa con el Sistema. Estos nos permitirán comprender quién utiliza el Sistema y con qué servicio externo se comunica para cumplir con algunas de sus funciones.

**Adminitrador de la Tienda:** Es el responsable de Administrar el funcionamiento del Sistema. Desde ShopExpress lo que el Administrador puede Gestionar serán Productos, Inventario y Pedidos, de acuerdo con las funciones establecidas en los Requisitos del Sistema.

**Cliente Final:** Es el Usuario que utiliza ShopExpress para consultar los Productos disponibles, gestionar el Carrito de Compras, realizar Pedidos y efectuar el Proceso de Compra.

**Pasarela de Pagos:** Este es el **Servicio externo** que permite procesar los pagos realizados en el Sistema. ShopExpress se comunica con este servicio para completar las transacciones, sin encargase directamente del manejo de la información sensible de las tarjetas.

**ShopExpress:** Este representa el Sistema que estamos diseñando. Es el punto central de toda la vista, este es el encargado de gestionar las funciones del Sistema y establecer la comunicación entre los Usuarios y los Servicios Externos que se necesitan para su funcionamiento.

## 3. Límites del Sistema

La Vista de Contexto permite establecer qué elementos hacen parte de ShopExpress y cuáles se encuentran fuera de él. En este caso ShopExpress representa el Sistema que se está desarrollando, mientras que el Cliente Final, el Administrador de la tienda y la Pasarela de Pagos se encuentran fuera de los límites y se relacionan con él para cumplir las diferencias funciones. 

El Cliente Final y el Administrador de la tienda interactúan directamente con ShopExpress, pero tienen responsabilidad diferentes. El Cliente Final utiliza las funciones relacionadas con las compra, mientras que el Administrador se encarga de las tareas de gestión de la tienda. Por otra parte, la Pasarela de Pagos corresponde a un Servicio Externo con el cual ShopExpress se comunica para realizar el procesamiento de pagos.

## 4. Diagrama de Contexto 

El siguiente diagrama representa los principales elementos que interactúan con ShopExpress y las relaciones que existen entre ellos. 

![Diagrama de Contexto](<diagrama - contexto.jpg>)

## 5. Explicación del Diagrama 

El Diagrama representa a ShopExpress como el Sistema central y muestra los elementos externos que tienen una relación directa con el. El Administrador de la tienda y el Cliente Final se encuentra fuera de los límites del Sistema, debido a que representan los diferentes tipos de Usuarios que interactúan con la plataforma.

Donde el Administrador como se expone en los límites y los elementos en ShopExpress realiza las tareas relacionadas con toda la Administración de la Tienda, mientras que el Cliente Final utiliza el Sistema para consultar los Productos, Gestionar su Compra y realizar los procesos correspondientes al Pedido. Y la Pasarela de Pago como Servicio Externo se relaciona con el Sistema para permitir el procesamiento de los pagos realizados durante las compras, de esta manera el Sistema puede utilizar un Servicio Externo sin que este forme parte de la estructura interna.