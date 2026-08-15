# 02 - Vista Conceptual

## 1. Introducción
Para la realización de la Vista Conceptual se busca representar de manera general cómo se encuentra organizado ShopExpress internamente a partir de los principales dominios funcionales identificados las fases anteriores.

A diferencia de la Vista de Contexto, en esta Vista ya no se busca mostrar quiénes están fuera del Sistema ni los Servicios Externos, sino comprender como se organiza las principales funciones de ShopExpress y como se relacionan entre ellas. 

Con base en los Módulos definidos anteriormente: Usuarios, Catálogo, Carrito de Compras, Pedidos y Pagos. Estos módulos representan las funciones principales que debe de cumplir el Ssitema para permitir que un Usuario pueda realizar todo el proceso de compra y que el Administrador pueda realizar las tareas correspondientes a la gestión de la tienda.

## 2. Dominios Funcionales
En esta Vista se identifican los principales Dominios Funcionales que hacen parte de ShopExpress. Aquí cada uno representa una función específica del Sistema y todos se encuentran relacionados para permitir que se pueda realizar el proceso completo de compra.

**Usuarios:** Se encargan de las funciones relacionadas con el Registro, Inicio de Sesión y Gestión de la información de los Usuarios. También permite al Administrador gestionar las cuentas de los Usuarios.

**Catálogo:** Se encarga de la gestión y consulta de los Productos disponibles en la tienda. En este módulo se encuentran funciones como crear, editar, consultar y dar de baja Productos, además de realizar búsquedas y consultar su disponibilidad.

**Carrito de Compras:** Permite que el Usuario pueda agregar los Productos que desea comprar, modificar sus cantidades o eliminarlos antes de realizar el Pedido. También se encarga de calcular el subtotal y total de los Productos seleccionados.

**Pedidos:** Se encarga de generar y registrar los Pedidos realizados a partir del Carrito de Compras. También permite consultar el estado de cada Pedido y actualizar la información correspondiente durante el proceso de compra.

**Pagos:** Se encarga de gestionar el proceso relacionado con el pago de los Pedidos y de comunicarse con la Pasarela de Pagos externa para procesar la transacción y conocer si esta fue aprobada o rechazada.

## 3. Relación entre Dominios
Los dominios funcionales no trabajan de manera aislada, ya que cada uno participa en diferentes partes del funcionamiento de ShopExpress.

**1:** El Módulo de Usuarios se relaciona principalmente con el Carrito de Compras y los Pedidos, ya que cada Usuario puede tener un Carrito y realizar diferentes Pedidos.

**2:** El Catálogo se relaciona con el Carrito de Compras porque los Productos disponibles son los que pueden ser agregados por los Usuarios. También existe una relación con los Pedidos, debido a que los Productos seleccionados terminan formando parte de una orden de compra.

**3:** El Carrito de Compras se relaciona con los Pedidos porque, una vez que el Usuario confirma los Productos seleccionados, se genera el Pedido correspondiente.

**4:** Los Pedidos se relacionan con el módulo de Pagos, debido a que cada Pedido debe pasar por un proceso de pago para determinar si la transacción fue aprobada o rechazada.

Estas relaciones permiten representar el proceso general de ShopExpress de una manera sencilla: El Usuario selecciona Productos del Catálogo, los agrega al Carrito, confirma la compra para generar un Pedido y posteriormente realiza el Pago correspondiente. Esta organización también mantiene coherencia con el modelo conceptual desarrollado en la Fase 2.

## 4. Diagrama Conceptual
El siguiente Diagrama representa los principales dominios funcionales que conforman ShopExpress y las relaciones existentes entre ellos.

![Diagrama Conceptual](<diagrama - conceptual.jpg>)

## 5. Explicación del Diagrama 
El Diagrama Conceptual representa los principales Dominios Funcionales de ShopExpress y la forma en que estos se relacionan para cumplir con las funciones definidas en los requisitos. Como primer lugar se encuentra el **Módulo de Usuarios,** que se relaciona con el Carrito de Compras y los Pedidos debido a que estas funciones son realizadas por los Usuarios registrados en el Sistema.

El **Módulo de Catálogo** se relaciona con el Carrito y los Pedidos, ya que los Productos que se encuentran disponibles en el Catálogo pueden ser seleccionados por los Usuarios y posteriormente formar parte de un Pedido.

El **Carrito de Compras** se encuentra relacionado con los Pedidos porque representa el paso anterior a la generación de una orden de compra. Una vez que el Usuario confirma el contenido del Carrito, el Sistema puede generar el Pedido correspondiente.

Por último, el **Módulo de Pagos** se relaciona con los Pedidos, ya que el pago se realiza sobre una orden de compra previamente generada. Este módulo también mantiene la comunicación con la Pasarela de Pagos, aunque esta última no se representa dentro de esta Vista porque corresponde a un elemento externo que ya fue identificado en la Vista de Contexto.

La Vista Conceptual permite comprender cómo están organizadas las principales funciones de ShopExpress y cómo cada una se relaciona con las demás para completar el proceso de compra.