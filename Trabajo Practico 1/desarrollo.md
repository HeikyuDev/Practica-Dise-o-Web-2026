
---

##  Presentaciones

### 1. ¿Aplicación Web = Sitio Web? ¿Por qué?
* **Respuesta de la fuente:** Las fuentes definen una Aplicación Web como un software al que se accede mediante un navegador de internet o intranet, codificado en un lenguaje soportado por dicho navegador. Se destaca por ser una "extensión dinámica de la web" que genera páginas interactivas con contenido dinámico en respuesta a peticiones.
* **Aclaración externa (no incluida en las fuentes):** No son exactamente lo mismo. Un "sitio web" suele definirse como un conjunto de páginas principalmente informativas y de consumo pasivo, mientras que una "aplicación web" (como lo definen los textos) implica interactividad, procesamiento de datos y un enfoque orientado a servicios o presentación dinámica.

### 2. ¿A qué nos referimos cuando hablamos de “cliente” en desarrollo web?
* **Respuesta de la fuente:** El cliente principal en la web son los navegadores (*browsers*) que solicitan información al servidor. En la arquitectura Cliente/Servidor, el cliente asume un papel activo en la comunicación: inicia las solicitudes o peticiones, espera y recibe las respuestas del servidor, e interactúa directamente con los usuarios finales mediante una interfaz gráfica de usuario.

### 3. ¿A qué nos referimos cuando hablamos de lenguaje del lado del cliente? Mencione ejemplos.
* **Respuesta de la fuente:** Son aquellos lenguajes que pueden ser directamente "digeridos" e interpretados por el navegador web del usuario, sin necesidad de un pretratamiento por parte del servidor. Son totalmente independientes del servidor, lo que permite albergar la página en cualquier sitio.
* **Ejemplos:** HTML, Java (Applets), JavaScript y CSS.

### 4. ¿A qué nos referimos cuando hablamos de lenguaje del lado del servidor? Mencione ejemplos.
* **Respuesta de la fuente:** Son lenguajes que son reconocidos, ejecutados e interpretados por el propio servidor web. Tras procesar la información, envían el resultado final al cliente en un formato que este pueda comprender (como HTML).
* **Ejemplos:** CGI (usando C, C++, Perl o Visual Basic), ASP.NET, PHP y Java Server Pages (JSP).

### 5. ¿Puedo conectarme a una base de datos utilizando HTML?
* **Respuesta de la fuente:** **No.** Según las fuentes, HTML es un lenguaje del lado del cliente cuya única función es indicar al navegador dónde colocar texto, imágenes o video y la forma que tendrán en la página. 
* **Flujo arquitectónico:** Por el contrario, las bases de datos operan en la "Capa de datos" del servidor. Para conectar una interfaz gráfica con la base de datos se requiere una "Capa de negocios" procesada en el servidor, lo cual hace obligatorio el uso de un lenguaje del lado del servidor (como PHP o JSP) y no simplemente HTML.

---

## 🌐 Web Estáticas y Dinámicas

### 1. ¿Qué es una página web dinámica? Mencione sus características.
* **Respuesta de la fuente:** Es una página interactiva generada por una aplicación web que combina lenguajes de marcado (como HTML o XML) con contenido dinámico que cambia en respuesta a las peticiones del usuario. Se apoyan en lenguajes del lado del servidor (CGI, ASP, PHP, etc.) que ejecutan procesos, validan reglas de negocio y se conectan a bases de datos antes de enviar la información final al navegador.

### 2. Nombre 3 ejemplos de ellas.
* **Respuesta de la fuente:** Las fuentes mencionan arquitectónicamente un "formulario web de inscripción" como ejemplo de una interacción dinámica en tres capas (presentación, negocio y datos).
* **Aclaración externa (las fuentes no nombran 3 sitios reales):** Ejemplos típicos son las redes sociales (Facebook), plataformas de comercio electrónico (Amazon) o los sistemas de gestión académica universitarios (SIU Guaraní).

### 3. ¿Qué es una página web estática? Mencione sus características.
* **Aclaración de la fuente:** Las fuentes proporcionadas no definen ni mencionan las páginas web estáticas, enfocándose enteramente en las dinámicas.
* **Aclaración externa:** Una página estática es aquella cuyo contenido está escrito exclusivamente en código cliente (HTML y CSS) y se muestra exactamente igual a todos los usuarios, sin interactuar con bases de datos ni poseer procesamiento en un servidor.

### 4. Nombre 3 ejemplos de ellas.
* **Aclaración externa (no presente en las fuentes):** 1. Una página de "Próximamente" o "En construcción".
  2. El portafolio personal básico de un diseñador.
  3. Una landing page sencilla de un restaurante que solo muestra su menú fijo, dirección y teléfono.

### 5. En la actualidad, en qué caso utilizaría cada uno de ellas.
* **Aclaración externa (no presente en las fuentes):**
  * **Estáticas:** Se usan cuando el presupuesto es muy bajo, se necesita máxima velocidad de carga y el contenido casi nunca cambia (páginas informativas o blogs muy básicos).
  * **Dinámicas:** Se usan cuando se requiere interacción del usuario, gestión de cuentas, compras online, paneles de administración o actualización frecuente del contenido sin tocar el código fuente.

---

## 🛠️ Instalación

### 1. ¿Qué aplicación utilizaron para instalar el servidor Web? Y ¿Por qué?
* **Respuesta de la fuente:** Los documentos destacan **XAMPP** para configurar hosts virtuales y entornos de desarrollo local. Se utiliza porque es una herramienta "todo en uno" que integra Apache, MySQL, PHP y Perl, destacando por su facilidad de instalación y uso, permitiendo iniciar un servidor local "en un abrir y cerrar de ojos". También se exponen alternativas según el sistema operativo, como WampServer (Windows), MAMP (macOS), LAMP (Linux) y Laragon.

### 2. ¿Cómo puedo saber qué versión de PHP tengo instalada?
* **Aclaración de la fuente:** Esta información no se encuentra en los documentos provistos.
* **Aclaración externa:** Puedes crear un archivo llamado `info.php` en tu directorio raíz con el código:
  ```php
  <?php phpinfo(); ?>
y abrirlo en tu navegador; o bien, ejecutar el comando php -v en la terminal de tu sistema operativo.

3. Indique en qué directorio del servidor tengo que alojar mi sitio/sistema para poder utilizarlo/probarlo.
Respuesta de la fuente: Por defecto en XAMPP, debes alojar los archivos en el directorio raíz de documentos, que es C:\xampp\htdocs. Si configuras "Hosts Virtuales", puedes asignar directorios personalizados en otras ubicaciones, como por ejemplo C:\miproyecto\httpdocs.

4. ¿Qué archivo de configuración tengo que editar para mostrar/ocultar los errores en tiempo de ejecución? Y ¿Cuáles son las distintas opciones para eso?
Aclaración de la fuente: Las fuentes proporcionadas explican cómo configurar hosts virtuales mediante los archivos httpd.conf y httpd-vhosts.conf, pero no mencionan la configuración de reporte de errores de ejecución.

Aclaración externa: Para controlar los errores en PHP se debe editar el archivo php.ini. Las opciones principales involucran la directiva display_errors (que puede estar en On para desarrollo o Off para producción) y error_reporting (donde se define el nivel de detalle de los errores, como E_ALL).

5. ¿Cuáles son las variables que debo modificar para no tener grandes sobresaltos a la hora de implementar un sistema/sitio web?
Respuesta de la fuente: Basado estrictamente en la configuración de Hosts Virtuales mostrada en las fuentes, para evitar errores de acceso (como problemas con Apache), dentro de la etiqueta <Directory> en el archivo httpd-vhosts.conf, se deben configurar adecuadamente los permisos con las variables Options All, AllowOverride All y fundamentalmente asegurar los permisos con Require all granted.

Aclaración externa: Las fuentes no detallan variables globales de servidor (como límite de memoria de PHP, tiempos máximos de ejecución o peso máximo de subida de archivos), las cuales también suelen ser críticas al implementar sistemas en entornos reales (ej. memory_limit, max_execution_time, upload_max_filesize en el php.ini).