# RetroVideo: Proyecto Intermodular (1º DAW)

Bienvenido al repositorio oficial de **RetroVideo**, el proyecto final intermodular que integra los conocimientos adquiridos durante el primer curso del ciclo superior de Desarrollo de Aplicaciones Web en el IES Severo Ochoa.

Este proyecto es un **MVP (Producto Mínimo Viable)** diseñado para modernizar la gestión de un videoclub, permitiendo la administración de películas, videojuegos, socios y la trazabilidad de alquileres.

---

## Arquitectura del Proyecto

El proyecto está diseñado siguiendo una arquitectura limpia y separada por capas para asegurar su escalabilidad en futuros desarrollos:

* **`backend/` (Capa Lógica y Persistencia - UP12)**
    * Desarrollado en Java 21.
    * Implementa el patrón DAO para centralizar el acceso a datos.
    * Utiliza JPA (Jakarta Persistence API) con Hibernate ORM para la conexión a la base de datos.
* **`database/` (Capa de Datos - UP5)**
    * Contiene el script `videoclub.sql`.
    * Base de datos relacional MySQL (MariaDB) que garantiza la integridad referencial y evita la pérdida o corrupción de datos.
* **`frontend/` (Capa de Presentación Visual - UP6)**
    * Prototipo visual (Mockup) desarrollado en HTML5 y CSS3.
    * Diseño responsive utilizando CSS Grid y variables nativas para un mantenimiento ágil.
    * Incluye scripts de prueba que demuestran la interactividad planificada.
* **`docs/api/` (Diseño de API REST - UP9)**
    * Documentación técnica en formato OpenAPI 3.0 (`openapi.yaml`).
    * Define los endpoints, esquemas de datos y métodos HTTP (GET, POST) necesarios para que, en un futuro (v2.0), el Frontend y el Backend se comuniquen de forma asíncrona.

---

## Instalación y Ejecución

Para ejecutar la parte funcional (Backend + Base de Datos) de este proyecto en tu entorno local:

### 1. Base de Datos
1. Asegúrate de tener instalado **XAMPP** (o un entorno similar con MySQL/MariaDB).
2. Inicia el servicio de MySQL.
3. Importa el archivo `database/videoclub.sql` en tu gestor (ej. phpMyAdmin) para crear la base de datos y cargar los datos de prueba.

### 2. Backend (Java)
1. Abre la carpeta `backend/` como proyecto en **IntelliJ IDEA** o Eclipse.
2. Asegúrate de que las dependencias de Maven (indicadas en el `pom.xml`) se descarguen correctamente.
3. Ejecuta la clase `app.Main`. El sistema se conectará a MySQL y desplegará la interfaz de consola.

### 3. Frontend (Prototipo)
* Simplemente abre el archivo `frontend/index.html` en tu navegador web de preferencia para visualizar la propuesta de diseño para la versión web.

---

## Trabajo en Equipo (Simulación de Escalado)

Si este proyecto se desarrollara en un equipo de múltiples personas, el flujo de trabajo propuesto sería:

1.  **Repositorios Centralizados:** Uso de esta Organización en GitHub para mantener el código fragmentado y organizado (Backend, Frontend).
2.  **Ramas (GitFlow):** Se bloquearía la rama `main`. Todo el desarrollo se haría en ramas de características (`feature/nueva-tabla`, `feature/diseño-nav`) que luego se integrarían mediante *Pull Requests*.
3.  **Roles Claros:** Asignación de desarrolladores a Frontend (Consumo de API y maquetación) y Backend (Lógica Java y diseño SQL).

---

## Autor
* **Adrián Martínez** - Alumno de 1º DAW - IES Severo Ochoa (2025/2026).
