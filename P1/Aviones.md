# Prácticas Ingeniería del Software

> Por Ana Buendía, Andrés Millán, Paula Villanueva, Juan Antonio Villegas


## Descripción y objetivos

**Dominio del problema**: software de gestión de viajes

El software Control Operacional de Vuelos Inmersivo Didáctico (COVID) (WIP) permite a las agencias de viajes controlar la gestión de los destinos posibles, así como la reserva de hoteles y la contratación de actividades. Está diseñado para ofrecer una experiencia de usuario muy amigable, de forma que se requiere de poca formación para utilizarlo.

El objetivo de *Nombresuperchuloaqui* es, en esencia, ofrecer distintos destinos para que las personas puedan disfrutar de un viaje con alojamiento y actividades de la forma más cómoda posible.
A continuación se exponen los objetivos que se pretenden alcanzar:
- Crear una interfaz cómoda y simple para que los clientes realicen las reservas.
- Control de los pagos asociados a una reserva y el posterior viaje.
- Realizar envíos de publicidad personalizada a los clientes.
- Definir y gestionar circuitos turísticos creados por la agencia.
- Gestionar actividades turísticas.
- Llevar un control de los agentes comerciales de las distintas oficinas.


## Descripción de los implicados

### Entorno de usuario

La aplicación está diseñada de forma que los clientes tendrán una interfaz sencilla de entender y manejar, ya que no podemos asumir nada con respecto a la experiencia de estos con aplicaciones informáticas. Sin embargo los trabajadores de la empresa serán formados de cara a saber manejar el sistema desde una perspectiva mas compleja.

### Resumen de los implicados

* **Cliente**: representa un cliente de la empresa, esto es, un usuario que solicita un viaje mediante nuestra aplicación.
* **Trabajador**: representa a los trabajadores que manejan y gestionan asuntos relativos a la agencia de viajes, por ejemplo, vuelos, hoteles, actividades,...
* **Cadena hotelera**: representante de una cadena de hoteles relacionada con la empresa. Cada cadena tiene una gama de hoteles diferentes.
* **Empresa aérea de transportes**: representante de una empresa de viajes en aviones. Cada empresa aérea de transportes a su vez nos ofrece viajes con diferentes orígenes, destinos, y horarios.
* **Empresa terrestre de transportes**: representante de una empresa de transportes mediante autobús. Al igual que la aérea, ofrece viajes en autobús con distintos orígenes, destinos y horarios.
* **Coordinadora de actividades**: empresa que organiza diversos tours y actividades en los diferentes destinos de nuestro viaje.
* **Jefe de empresa**: jefes de nuestra empresa que coordinan la labor de nuestros trabajadores. 
* Añadir o quitar gente

### Perfiles

Esto hay que hacerlo?


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

- **RF-3 Gestión de actividades** El sistema deberá proporcionar las diferentes actividades a realizar
    - **RF-3.1** Gestión de circuitos turísticos
        - **RF-3.1.1** Selección de excursiones
    - **RF-3.2** Gestión de actividades turísticas
        - **RF-3.2.1** Selección de espectáculos
        - **RF-3.2.2** Selección de reservas o alquileres

- **RF-4 Gestión del trayecto** El sistema deberá proporcionar información acerca del trayecto
    - **RF-4.1** Selección del medio de transporte
    - **RF-4.2** Selección del horario de salida y llegada


## Requisitos no funcionales

### Usabilidad

- **RNF-1** Se deberá proporcionar un menú intuitivo para facilitar al empleado la gestión.
- **RNF-** Se proporcionará una paleta de comandos que permita al usuario usar las funciones de forma rápida.
- **RNF-** Se deberá proporcionar un mapa que permita ver hoteles y rutas de transportes.
- **RNF-** Se mantendrá actualizada la base de datos online en todo momento para evitar solapaciones de servicios.

### Fiabilidad

- **RNF-** Se evitarán condiciones de carrera para garantizar la correcta contratación de los servicios.
- **RNF-** Se mantendrán actualizados los servicios prestados por las compañías de terceros, para asegurar el correcto funcionamiento del sistema.

### Rendimiento

- **RNF-** Las operaciones de contratación de servicios deben hacerse lo más rápido posible para evitar interbloqueos.

### Soporte

- **RNF-** Se creará una sección de preguntas y respuestas habituales para los usuarios.
- **RNF-** Se habilitará un servicio de atención telefónica para resolver las dudas de las empresas.

### Restricción de la implementación

- **RNF-** Se utilizará el framework `Vue.js` para facilitar el desarrollo multiplataforma.
- **RNF-** Las APIs proporcionadas por los servicios de terceros deben ser compatibles con nuestro sistema.

### Restricciones de diseño


### Requisitos de logística

- **RNF-** Los usuarios deben proporcionar su nombre, email y contraseña para registrarse.
- **RNF-** Los clientes deben estar registrados para contratar los servicios

### Requisitos físicos

- **RNF-** Existen diferentes servidores que mantengan la base de datos actualizada por si fallara uno.
- **RNF-** La aplicación será soportada por cualquier sistema que permita usar una PWA.

### Requisitos legales

- **RNF-** Todos los datos de usuario que permitan identificar a los usuarios serán privados y no se venderán.
- **RNF-** Emails y contraseñas serán cifradas.
- **RNF-** El usuario debe estar acorde con los términos de uso y las condiciones de privacidad de las compañías de terceros involucradas en el sistema.

## Requisitos de información
- **RI-1** Usuarios: Se almacenan los datos personales de cada cliente para poder realizar una reserva de un viaje.
    - DNI
    - Nombre
    - Apellidos
    - Fecha de nacimiento
    - e-mail
    - Contraseña
    - Información de pago
    - Reservas
- **RI-2** Empleados: Se guarda un registro de todos los datos de las personas contratadas de la agencia de viajes.
    - DNI
    - Nombre
    - Apellidos
    - Fecha de nacimiento
    - e-mail
    - Contraseña
    - Fecha inicio de contrato
    - Fecha fin de contrato
- **RI-3** Viaje: Se almacenan los viajes, incluyendo actividades, transporte y hotel.
    - Código identificador
    - Destino
    - Actividades incluidas
    - Hoteles
    - Duración del viaje
    - Transporte ida
    - Transporte vuelta
- **RI-4** Hoteles: Se guarda la información relativa al hotel.
    - Identificador de hotel
    - Precio
    - Marca
    - Ciudad
- **RI-5** Actividades: Se tiene un registro de la información de la actividad.
    - Identificador de actividad
    - Precio
    - Descripción.
    - Horario
    - Ciudad
- **RI-6** Transporte: Se almacena la información relativa al transporte.
    - Identificador de vuelo
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
* **Paleta de comandos**: **Rellena Andrés que lo harás mejor que yo**.
* **Condiciones de carrera**: Situación a evitar consistente en que dos o más clientes deseen reservar al mismo tiempo algún servicio que solo pueda asignarse a uno de ellos. Por ejemplo, en el caso de que en un mismo vuelo dos usuarios quieran reservar el mismo asiento.
