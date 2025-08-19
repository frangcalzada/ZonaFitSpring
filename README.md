🏋️‍♂️ ZonaFitSpring

ZonaFitSpring es una aplicación desarrollada en Java con Spring Boot para la gestión de clientes en un gimnasio. Combina una interfaz gráfica de escritorio con Swing y una arquitectura moderna basada en servicios con Spring Data JPA.

🚀 Tecnologías utilizadas

Java 24

Spring Boot 3.5.4

Spring Data JPA → Persistencia de datos.

MySQL → Base de datos relacional.

Lombok → Reducción de código boilerplate (getters, setters, constructores).

Swing + FlatLaf → Interfaz gráfica de escritorio moderna.

📂 Estructura del proyecto
ZonaFitSpring/
 └── src/main/java/gm/zona_fit/
     ├── modelo/            → Entidades (Ej: Cliente.java)
     ├── repositorio/       → Interfaces de acceso a datos (ClienteRepositorio.java)
     ├── servicio/          → Lógica de negocio (ClienteServicio.java, IClienteServicio.java)
     ├── gui/               → Interfaz gráfica con Swing (ZonaFitForma.java)
     ├── ZonaFitApplication.java → Clase principal (Spring Boot)
     └── ZonaFitSwing.java       → Lanzador de la aplicación de escritorio


🔹 Módulos principales

modelo
Contiene las entidades JPA, como Cliente.java, que representan las tablas en la base de datos.

repositorio
Interfaces que extienden de JpaRepository, permitiendo operaciones CRUD de forma sencilla.

servicio
Capa de negocio. Define las interfaces (IClienteServicio) y sus implementaciones (ClienteServicio) para encapsular la lógica de la aplicación.

gui
Contiene la interfaz gráfica de usuario con Swing (ZonaFitForma.java), estilizada con FlatLaf.

Aplicación principal

ZonaFitApplication.java: punto de entrada de Spring Boot.

ZonaFitSwing.java: inicializa la aplicación de escritorio.

⚙️ Configuración

En el archivo src/main/resources/application.properties se definen los parámetros de conexión a MySQL:

spring.datasource.url=jdbc:mysql://localhost:3306/zonafit
spring.datasource.username=usuario
spring.datasource.password=contraseña
spring.jpa.hibernate.ddl-auto=update


▶️ Ejecución

Clonar el repositorio

git clone https://github.com/usuario/ZonaFitSpring.git
cd ZonaFitSpring



Configurar la base de datos MySQL en application.properties.

Ejecutar la aplicación:

mvn spring-boot:run



La aplicación se abrirá con la interfaz gráfica ZonaFit.
