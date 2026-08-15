# Consolidación. 

## 1. Introducción
La Fase 4 tiene como propósito consolidar los diferentes elementos desarrollados durante el proyecto y comprobar que exista coherencia entre los requisitos, el modelo conceptual, las decisiones arquitectónicas y las Vistas Arquitectónicas de ShopExpress.

Durante las fases anteriores se identificaron las necesidades principales del Sistema, los Usuarios que interactúan con él, los módulos funcionales, las entidades del dominio y las decisiones tomadas para definir la arquitectura.

A partir de estos elementos se construyeron las diferentes Vistas Arquitectónicas, permitiendo representar ShopExpress desde diferentes perspectivas y comprender tanto su funcionamiento general como su organización interna y su infraestructura.

## 2. Integración de las Fases
El desarrollo de ShopExpress se realizó de manera incremental, tomando como base los resultados obtenidos en cada una de las fases.

**1:** En la Fase 1 se realizó la identificación del problema, los objetivos, el alcance, los Stakeholders, los módulos funcionales, los requisitos funcionales y no funcionales y las restricciones del Sistema.

**2:** En la Fase 2 se desarrolló el modelo conceptual del dominio, identificando las principales entidades y relaciones del Sistema. También se establecieron las decisiones arquitectónicas y se seleccionó la arquitectura monolítica como la más adecuada para ShopExpress.

**3:** En la Fase 3 se representaron las diferentes Vistas Arquitectónicas, mostrando el Sistema desde diferentes perspectivas: Contexto, Conceptual, Casos de Uso, Lógica, Implementación y Física.

**4:** La Fase 4 permite reunir estos elementos y comprobar que las decisiones tomadas durante el desarrollo se encuentren representadas de manera coherente en la arquitectura propuesta.

## 3. Coherencia entre Requisitos y Arquitectura
Las Vistas Arquitectónicas fueron construidas teniendo en cuenta los requisitos identificados durante las fases anteriores. Las Funciones relacionadas con la **Gestión de Usuarios, Productos, Inventario, Carrito de Compras, Pedidos y Pagos** se encuentran representadas en las diferentes Vistas y permiten relacionar los Requisitos con la organización interna propuesta para ShopExpress.

El proceso principal de compra también mantiene una relación entre las diferentes Vistas. El Usuario consulta los Productos disponibles, los agrega al Carrito de Compras, confirma la Compra para generar un Pedido y posteriormente realiza el Pago mediante la Pasarela de Pagos.

De esta manera, todas las funcionalidades definidas inicialmente se mantienen presentes en la representación arquitectónica del Sistema.

## 4. Coherencia entre las Vistas Arquitectónicas
Las Vistas desarrolladas representan diferentes aspectos del mismo Sistema y mantienen una relación entre ellas.

**01:** La Vista de Contexto permite identificar a los Usuarios y al Servicio Externo que se relacionan con ShopExpress.

**02:** La Vista Conceptual muestra los principales Dominios Funcionales que forman parte del Sistema y las relaciones entre ellos.

**03:** La Vista de Casos de Uso representa las principales funciones que pueden realizar el Administrador de la Tienda y el Cliente Final.

**04:** La Vista Lógica representa la organización interna mediante los principales módulos y sus relaciones.

**05:** La Vista de Implementación lleva estos módulos a una representación mediante componentes de software y muestra su relación con la Base de Datos y la Pasarela de Pagos.

**06:** La Vista Física representa dónde se ejecutan estos componentes y cómo se distribuyen dentro de la infraestructura propuesta.

Estas Vistas permiten observar ShopExpress desde diferentes niveles sin perder la relación entre los elementos representados.

## 5. Coherencia con la Arquitectura Seleccionada
Para ShopExpress se seleccionó una **Arquitectura Monolítica,** debido a que permite mantener las principales funciones del Sistema dentro de una misma aplicación y facilita su desarrollo y administración. 

La organización realizada en las Vistas mantiene esta decisión, ya que los Módulos principales de Usuarios, Productos, Inventario, Carrito, Pedidos y Pagos hacen parte de la misma aplicación. Aunque los Módulos se encuentran separados de acuerdo con sus responsabilidades, estos forman parte de un mismo Sistema y trabajan de manera conjunta.

Por otro lado la Base de Datos se mantiene como un elemento separado para almacenar la información del Sistema, mientras que la Pasarela de Pagos corresponde a un Servicio Externo con el cual ShopExpress se comunica.

## 6. Atributos de Calidad
Para los Atributos de Calidad, la Arquitectura que se definió durante las fases anteriores tuvimos siempre en cuenta este paso tan importante donde, **La Seguridad** se considera principalmente en el manejo de Usuarios y en el proceso de Pagos, especialmente porque la Pasarela de Pagos se mantiene como un Servicio Externo. Por otra parte **La Disponibilidad** se relaciona con la necesidad de que ShopExpress pueda estar disponible para que los Usuarios puedan consultar Productos, gestionar sus Carritos y realizar Pedidos. Luego **La mantenibilidad** se favorece mediante la separación de las diferentes responsabilidades en Módulos, permitiendo identificar de manera más clara dónde se encuentra cada función del Sistema. Y por última una de las más importantes **La Escalabilidad** Mediante la separación entre el Servidor de Aplicaciones y el Servidor de Base de Datos, permite administrar estos elementos de manera independiente.

## 7. Conclusiones
El desarrollo del Documento de Especificación Arquitectónica permitió representar la propuesta de ShopExpress desde diferentes perspectivas y relacionar los requisitos definidos inicialmente con las decisiones tomadas durante el diseño del Sistema. La utilización del **Modelo 4+1 de Kruchten** permitió organizar las diferentes Vistas Arquitectónicas y representar aspectos como el Contexto, los Casos de Uso, la organización Lógica, la Implementación y el Despliegue del Sistema.

La **Arquitectura Monolítica** seleccionada permite mantener las principales funcionalidades de ShopExpress dentro de una misma aplicación, mientras que la separación de responsabilidades mediante módulos permite mantener una organización clara del Sistema y finalmente, las Vistas desarrolladas permiten comprender cómo interactúan los Usuarios con ShopExpress, cómo se organizan sus principales funciones, cómo se implementan sus componentes y cómo se distribuyen dentro de la infraestructura propuesta.