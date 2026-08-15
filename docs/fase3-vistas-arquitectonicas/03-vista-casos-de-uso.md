# 03 - Vista de Casos de Uso

## 1. Introducción
Las Vistas de Casos de Uso permite representar las principales Funciones que ofrece ShopExpress y la forma en que los diferentes Usuarios interactúan con ellas. Esta Vista se enfoca principalmente en mostrar qué puede realizar cada tipo de Usuario dentro del Sistema, sin entrar todavía en la forma en que estas Funciones que se encuentran implementadas internamente.

Para la construcción de esta Vista se tienen en cuenta los Actores y los Requisitos Funcionales definidos durante las Fases anteriores. De esta manera se busca mantener una relación directa entre lo que el Sistema debe realizar y las acciones que pueden ejecutar los Usuarios. En ShopExpress se identifican principalmente dos tipos de Usuarios: el Administrador de la Tienda y el Cliente Final. Cada uno tiene diferentes responsabilidades dentro del Sistema y por esta razón se relaciona con diferentes casos de uso.

## 2. Actores
**Administrador de la Tienda:** Es el Usuario encargada de realizar las funciones relacionadas con la administración de ShopExpress, aquí en las principales actividades se encuentra la Gestión de Usuarios, Productos, Inventario y Pedidos.

**Cliente Final:** Es el Usuario que utiliza ShopExpress para realizar la compra. Puede consultar los Productos disponibles, gestionar su Carrito de Compras, realizar Pedidos y efectuar los Pagos correspondientes.

## 3. Casos de Uso
Los Casos de Uso se desglosan de los requisitos plasmados anteriormente.

**Gestionar Usuarios:** Con los Usuarios del Sistema incluyendo su Registro, Consulta, Actualización y Administración.
**Actor:** Administrador de la Tienda.

**Gestionar Productos:** Permite administrar los Productos que se encuentran disponibles en la tienda.
**Actor:** Administrador de la Tienda.

**Gestionar Inventario:** Permite controlar la disponibilidad y las cantidades de Productos existentes.
**Actor:** Administrador de la Tienda.

**Gestionar Pedidos:**
Permite consultar y administrar los Pedidos realizados dentro de ShopExpress.
**Actor:** Administrador de la Tienda.

**Consultar Productos:** Permite al Cliente Final consultar los Productos disponibles en el Catálogo.
**Actor:** Cliente Final.

**Gestionar Carrito de Compras:** Permite agregar Productos al Carrito, modificar cantidades y eliminar Productos antes de confirmar la compra.
**Actor:** Cliente Final.

**Realizar Pedido:** Permite al Cliente Final confirmar los Productos seleccionados y generar un Pedido.
**Actor:** Cliente Final.

**Realizar Pago:** Permite realizar el pago correspondiente al Pedido mediante la Pasarela de Pagos.
**Actor:** Cliente Final.

## 4. Relaciones Principales
Para no complicar innecesariamente el Diagrama, vamos a mantener las relaciones principales.

El **Administrador de la Tienda** se relaciona con:
°Gestionar Usuarios, °Gestionar Productos, °Gestionar Inventario, °Gestionar Pedidos.

El Cliente Final se relaciona con: Consultar Productos, Gestionar Carrito de Compras,Realizar Pedido, Realizar Pago. Y entre los propios casos de uso tendremos una relación importante: 
**Gestionar Carrito de Compras --> Realizar Pedido**

Porque el Pedido se genera a partir de los Productos que el Cliente tiene en su Carrito.
También:
**Realizar Pedido --> Realizar Pago**

Porque el pago corresponde al Pedido que acaba de realizar el Cliente.

## 5. Diagrama de Casos de Uso
El siguiente Diagrama representa los principales Casos de Uso de ShopExpress y los dos tipos de Usuario que interactúan con el Sistema.

![Diagrama de Casos de Uso](<diagrama - casos de uso.jpg>)

## 6. Explicación del Diagrama
El Diagrama de Caso de Uso representa las principales funcionalidades de ShopExpress y permite identificar qué tipo de Usuario participa en cada una de ellas.

En la parte correspondiente al Administrador de la Tienda se encuentran las funciones relacionadas con la administración general del Sistema. Este Usuario puede gestionar los Usuarios, Productos, Inventario y Pedidos, de acuerdo con las funciones establecidas durante la especificación de requisitos. Por otra parte, el Cliente Final utiliza las funciones relacionadas directamente con el proceso de Compra. Primero puede consultar los Productos disponibles, posteriormente gestionar su Carrito de Compras, realizar el Pedido y finalmente realizar el Pago correspondiente.

El Diagrama permite observar de forma sencilla las responsabilidades de cada Usuario y cómo estas se relacionan con las principales funciones de ShopExpress.