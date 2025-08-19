🏋️‍♂️ ZonaFitSpring

ZonaFitSpring es una aplicación desarrollada en Java con Spring Boot para la gestión de clientes en un gimnasio.
El sistema combina una interfaz gráfica de escritorio con Swing y una arquitectura en capas con Spring Data JPA, lo que permite manejar de forma ordenada la lógica de negocio, la persistencia y la presentación.

🚀 Tecnologías utilizadas

Java 24

Spring Boot 3.5.4

Spring Data JPA → Persistencia de datos

MySQL → Base de datos relacional

Lombok → Simplificación de código (getters/setters/constructores)

Swing + FlatLaf → Interfaz gráfica moderna


📂 Estructura del proyecto
ZonaFitSpring/
 └── src/main/java/gm/zona_fit/
     ├── modelo/            → Entidades JPA (ej: Cliente.java)
     ├── repositorio/       → Interfaces de acceso a datos (ClienteRepositorio.java)
     ├── servicio/          → Lógica de negocio (ClienteServicio.java, IClienteServicio.java)
     ├── gui/               → Interfaz gráfica (ZonaFitForma.java)
     ├── ZonaFitApplication.java → Clase principal Spring Boot
     └── ZonaFitSwing.java       → Lanzador de la app de escritorio

🔹 Módulos principales

modelo: Define las entidades JPA (como Cliente), que representan las tablas de la base de datos.

repositorio: Interfaces que extienden JpaRepository, permitiendo operaciones CRUD automáticamente.

servicio: Capa intermedia donde vive la lógica de negocio (ClienteServicio).

gui: Interfaz de usuario desarrollada en Swing con estilo FlatLaf.

Clases principales:

ZonaFitApplication: arranca el contexto de Spring Boot.

ZonaFitSwing: inicializa la ventana gráfica de la aplicación.

⚙️ Configuración

Editar el archivo src/main/resources/application.properties con tus datos de conexión a MySQL:

spring.datasource.url=jdbc:mysql://localhost:3306/zonafit
spring.datasource.username=usuario
spring.datasource.password=contraseña
spring.jpa.hibernate.ddl-auto=update

▶️ Ejecución

Clonar el repositorio:

git clone https://github.com/frangcalzada/ZonaFitSpring.git

cd ZonaFitSpring


Configurar la base de datos en application.properties.

Ejecutar con Maven:

mvn spring-boot:run


La aplicación abrirá la interfaz gráfica ZonaFit.
