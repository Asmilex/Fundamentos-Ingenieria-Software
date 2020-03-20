---
title: Práctica 1. INGENIERÍA DE REQUISITOS. Lista inicial de requisitos
author: Ana Buendía, Andrés Millán, Paula Villanueva, Juan Antonio Villegas
date: \today
---


## Descripción y objetivos

**Dominio del problema**: software de gestión de viajes

El software *Control de Viajes Dual* permite a las agencias de viajes controlar la reserva de viajes, hoteles y actividades de sus clientes. Está diseñado para ofrecer una experiencia de usuario muy amigable, de forma que se requiere de poca formación para utilizarlo. Además, proporciona una interfaz básica en la que los clientes pueden consultar los servicios disponibles.

El objetivo de *Control de Viajes Dual* es, en esencia, ofrecer distintos destinos para que las personas puedan disfrutar de un viaje con alojamiento y actividades de la forma más cómoda posible.

A continuación se exponen los objetivos que se pretenden alcanzar:

- Crear una interfaz cómoda y simple para que los clientes realicen las reservas.
- Control de los pagos asociados a una reserva y el posterior viaje.
- Realizar envíos de publicidad personalizada a los clientes.
- Definir y gestionar circuitos turísticos creados por la agencia.
- Gestionar actividades turísticas.
- Llevar un control de los agentes comerciales de las distintas oficinas.


## Descripción de los implicados

### Entorno de usuario

La aplicación está diseñada de forma que todos los usuarios dispondrán de una interfaz sencilla de entender y manejar, ya que no podemos asumir nada con respecto a la experiencia de estos con aplicaciones informáticas. No obstante, se ofrecerá una documentación potente y sencilla de entender para que los empleados sean capaces de exprimir al máximo el potencial del software.

### Resumen de los implicados

* **Cliente**: representa un cliente de la empresa, esto es, un usuario que solicita un viaje mediante nuestra aplicación.
* **Empleado**: representa a los trabajadores que manejan y gestionan asuntos relativos a la agencia de viajes, por ejemplo, vuelos, hoteles, actividades,...
* **Cadena hotelera**: representante de una cadena de hoteles relacionada con la empresa. Cada cadena tiene una gama de hoteles diferentes.
* **Compañía de vuelos**: representante de una empresa de viajes en aviones. Cada empresa aérea de transportes a su vez nos ofrece viajes con diferentes orígenes, destinos, y horarios.
* **Compañía de transportes por carretera**: representante de una empresa de transportes mediante autobús y tren. Al igual que la de vuelos, ofrece viajes en con distintos orígenes, destinos y horarios.
* **Coordinadora de actividades**: empresa que organiza diversos tours y actividades en los diferentes destinos de nuestro viaje.
* **Jefe de empresa**: jefes de nuestra empresa que coordinan la labor de nuestros trabajadores.

## Requisitos funcionales

- **RF-1 Gestión de clientes** El sistema deberá proporcionar herramientas a los clientes para poder reservar un hotel en un destino deseado
    - **RF-1.1** Solicitud de reservas
        - **RF-1.1.1** Selección del destino tanto nacional como en el extranjero
        - **RF-1.1.2** Selección del alojamiento en diversos hoteles de distinta categoría
        - **RF-1.1.3** Selección de actividades complementarias
    - **RF-1.2** Realización de envíos de publicidad personalizada

- **RF-2 Gestión de hoteles** El sistema deberá proporcionar información acerca de los diversos hoteles de distinta categoría
    - **RF-2.1** Gestión de reservas de los clientes
        - **RF-2.1.1** Control, de manera flexible, de los pagos
        - **RF-2.1.2** Control de las habitaciones disponibles
    - **RF-2.2** Incorporar nuevos hoteles
    - **RF-2.3** Eliminar hoteles
    - **RF-2.4** Actualizar las características de los hoteles existentes
        - **RF-2.4.1** Actualizar número de habitaciones
        - **RF-2.4.2** Actualizar precio
        - **RF-2.4.3** Actualizar aforo

- **RF-3 Gestión de actividades** El sistema deberá proporcionar las diferentes actividades a realizar
    - **RF-3.1** Gestión de circuitos turísticos
        - **RF-3.1.1** Selección de excursiones
    - **RF-3.2** Gestión de actividades turísticas
        - **RF-3.2.1** Selección de espectáculos
        - **RF-3.2.2** Selección de reservas o alquileres de vehículos
    - **RF-3.3** Incorporar nuevas actividades
    - **RF-3.4** Eliminar actividades
    - **RF-3.5** Actualizar las características de las actividades turísticas existentes
        - **RF-3.5.1** Actualizar el número máximo de personas permitidas
        - **RF-3.5.2** Actualizar el horario de la actividad
        - **RF-3.5.3** Actualizar ruta del circuito turístico
        - **RF-3.5.4** Actualizar los espectáculos

- **RF-4 Gestión del trayecto** El sistema deberá proporcionar información acerca del trayecto
    - **RF-4.1** Selección del medio de transporte
    - **RF-4.2** Selección del horario de salida y llegada
    - **RF-4.3** Incorporar nuevos trayectos
    - **RF-4.4** Incorporar nuevos medios de transporte
    - **RF-4.5** Eliminar trayectos
    - **RF-4.6** Eliminar medios de transporte
    - **RF-4.7** Actualizar las características de un trayecto existente
        - **RF-4.7.1** Actualizar la ruta del trayecto
        - **RF-4.7.2** Actualizar el horario de salida
        - **RF-4.7.3** Actualizar el horario de llegada
    - **RF-4.8** Actualizar las características de un medio de transporte
        - **RF-4.8.1** Actualizar el número de plazas
    - **RF-4.9** Selección del tipo de viaje (estándar, turista, preferente, VIP, ...)

## Requisitos no funcionales

### Usabilidad

- **RNF-1** Se deberá proporcionar un menú intuitivo para facilitar al empleado la gestión.
- **RNF-2** Se deberá proporcionar una interfaz sencilla para que los clientes contraten servicios.
- **RNF-3** Se proporcionará una paleta de comandos que permita al empleado usar las funciones de forma rápida.
- **RNF-4** Se deberá proporcionar un mapa que permita ver hoteles y rutas de transportes.

### Fiabilidad

- **RNF-5** Se evitarán condiciones de carrera para garantizar la correcta contratación de los servicios.
- **RNF-6** Se mantendrán actualizados los servicios prestados por las compañías de terceros, para asegurar el correcto funcionamiento del sistema.

### Rendimiento

- **RNF-7** Las operaciones de contratación de servicios deben hacerse lo más rápido posible para evitar interbloqueos.

### Soporte

- **RNF-8** Se creará una sección de preguntas y respuestas habituales para los usuarios.
- **RNF-9** Se habilitará un servicio de atención telefónica para resolver las dudas de las empresas.

### Restricción de la implementación

- **RNF-10** Se utilizará el framework `Vue.js` para facilitar el desarrollo multiplataforma.
- **RNF-11** Las APIs proporcionadas por los servicios de terceros deben ser compatibles con nuestro sistema.


### Requisitos de logística

- **RNF-12** Los usuarios deben proporcionar su nombre, email y contraseña para registrarse.
- **RNF-13** Los clientes deben estar registrados para contratar los servicios

### Requisitos físicos

- **RNF-14** Existen diferentes servidores que mantengan la base de datos actualizada por si fallara uno.
- **RNF-15** La aplicación será soportada por cualquier sistema que permita usar una PWA.

### Requisitos legales

- **RNF-16** Todos los datos de usuario que permitan identificarlos serán privados y no se venderán a terceros.
- **RNF-17** Emails y contraseñas serán cifradas.
- **RNF-18** El usuario debe estar acorde con los términos de uso y las condiciones de privacidad de las compañías de terceros involucradas en el sistema.

## Requisitos de información
- **RI-1 Usuarios** Se almacenan los datos personales de cada cliente para poder realizar una reserva de un viaje.
    - DNI
    - Nombre
    - Apellidos
    - Fecha de nacimiento
    - e-mail
    - Contraseña
    - Información de pago
    - Reservas
- **RI-2 Empleados** Se guarda un registro de todos los datos de las personas contratadas de la agencia de viajes.
    - DNI
    - Nombre
    - Apellidos
    - Fecha de nacimiento
    - e-mail
    - Contraseña
    - Fecha inicio de contrato
    - Fecha fin de contrato
- **RI-3 Viaje** Se almacenan los viajes, incluyendo actividades, transporte y hotel.
    - Código identificador
    - Destino
    - Actividades incluidas
    - Hoteles
    - Duración del viaje
    - Transporte ida
    - Transporte vuelta
- **RI-4 Hoteles** Se guarda la información relativa al hotel.
    - Identificador de hotel
    - Precio
    - Marca
    - Ciudad
- **RI-5 Actividades** Se tiene un registro de la información de la actividad.
    - Identificador de actividad
    - Precio
    - Descripción
    - Horario
    - Ciudad
- **RI-6 Transporte** Se almacena la información relativa al transporte.
    - Identificador de viaje
    - Vehículo de transporte
    - Precio
    - Hora
    - Equipaje

## Glosario de términos

* **Agencia de Viajes**: empresa encargada de la organización y oferta de viajes a clientes.
* **Origen**: lugar del cual parte el viaje.
* **Destino**: lugar al cual llega el viaje y en el que se encuentran los hoteles en los que se alojarán los clientes y en el que se desarrollarán las actividades ofertadas.
* **Transporte**: medio por el cual se realiza el trayecto desde el origen al destino o viceversa.
* **Interfaz de la aplicación**: forma de presentar nuestra aplicación para que el usuario pueda contemplar todo lo que le ofrece la empresa de una forma clara.
* **Circuito turístico**: paseo y visita a distintos monumentos significativos de una ciudad destino dentro de un viaje.
* **Actividad turística**: forma de ocio ofertada a los viajeros durante el viaje. Por ejemplo, espectáculos.
* **Paleta de comandos**: una terminal interactiva con autocompletado que permite ejecutar casi cualquier comando disponible en la Interfaz Gráfica. Útil para usuarios avanzados.
* **Condiciones de carrera**: Situación a evitar consistente en que dos o más clientes deseen reservar al mismo tiempo algún servicio que solo pueda asignarse a uno de ellos. Por ejemplo, en el caso de que en un mismo vuelo dos usuarios quieran reservar el mismo asiento.
* **PWA**: Progressive Web App.
