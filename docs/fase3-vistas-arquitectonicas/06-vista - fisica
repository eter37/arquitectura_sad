# 06 - Vista Física

## 1. Introducción
En la Vista Física permite representar cómo se encuentra desplegado ShopExpress y qué elementos de infraestructura se utilizan para su funcionamiento. En esta Vista se muestran los principales nodos donde se ejecutan los componentes del Sistema y la forma en que estos se comunican.

Esta Vista permite complementar las anteriores, ya que después de identificar los Usuarios, las funciones, los módulos y los componentes de ShopExpress, se puede representar dónde se encuentran ubicados estos elementos para que el Sistema pueda funcionar.

## 2. Nodos del Sistema
Para el despliegue de ShopExpress se identifican los siguientes elementos:

**Dispositivo del Usuario:** Representa el computador, celular u otro dispositivo desde el cual el Cliente Final o el Administrador de la Tienda acceden a ShopExpress.

**Servidor de Aplicaciones:** Es el nodo encargado de ejecutar los componentes principales de ShopExpress y procesar las solicitudes realizadas por los Usuarios.

**Servidor de Base de Datos:** Almacena la información necesaria para el funcionamiento del Sistema, como Usuarios, Productos, Inventario, Carritos, Pedidos y datos relacionados con las operaciones realizadas.

**Pasarela de Pagos:** Corresponde al Servicio Externo utilizado para procesar los pagos realizados por los Clientes.

## 3. Estrategia de Despliegue
Para ShopExpress se propone una estrategia de despliegue centralizada, donde los componentes principales del Sistema se encuentran en un Servidor de Aplicaciones y la información se almacena en un Servidor de Base de Datos separado.

Esta organización permite separar la ejecución del Sistema del almacenamiento de la información y facilita la administración de cada uno de estos elementos.

La Pasarela de Pagos permanece fuera de la infraestructura de ShopExpress, debido a que corresponde a un Servicio Externo utilizado para completar las transacciones.

## 4. Diagrama de Despliegue
El siguiente Diagrama representa los principales nodos utilizados para el funcionamiento de ShopExpress y los componentes que se ejecutan o almacenan en cada uno de ellos.

![Diagrama de Despliegue / Vista Fisica](<diagrama - fisico.jpg>)

## 5. Explicación del Diagrama
El Diagrama de Despliegue muestra cómo se distribuyen los diferentes elementos de ShopExpress dentro de la infraestructura necesaria para su funcionamiento.

El proceso comienza desde el Dispositivo del Usuario, donde el Cliente Final o el Administrador de la Tienda acceden a la plataforma. Las solicitudes realizadas son enviadas al Servidor de Aplicaciones, donde se encuentran los componentes encargados de procesar las diferentes funciones del Sistema.

El Servidor de Aplicaciones se comunica con el Servidor de Base de Datos para almacenar y consultar la información relacionada con Usuarios, Productos, Inventario, Carritos y Pedidos.

Por otra parte, cuando un Cliente realiza un pago, el componente de Gestión de Pagos se comunica con la Pasarela de Pagos, que se encuentra fuera de la infraestructura de ShopExpress y permite completar la transacción.

De esta manera, la Vista Física permite observar dónde se encuentran ubicados los principales elementos del Sistema y cómo se comunican entre ellos para permitir el funcionamiento de ShopExpress.