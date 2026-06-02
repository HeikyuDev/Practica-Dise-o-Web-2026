## Presentaciones

### 1. ¿Aplicación Web = Sitio Web? ¿Por qué?
Una aplicación web es un software codificado en un lenguaje soportado por navegadores, en el cual se confía la ejecución al navegador. Se considera una extensión dinámica de la web que genera páginas interactivas con contenido dinámico en respuesta a peticiones.

*Nota: Los sitios web tradicionales suelen ser páginas principalmente informativas y estáticas, mientras que las aplicaciones web se centran en la interacción, el procesamiento de datos y la lógica de negocio.*

### 2. ¿A qué nos referimos cuando hablamos de “cliente” en desarrollo web?
El cliente principal en la web son los navegadores (browsers) que solicitan información al servidor. En una arquitectura Cliente/Servidor, el cliente asume un papel activo: inicia las solicitudes o peticiones, espera y recibe las respuestas del servidor, y normalmente interactúa de forma directa con los usuarios finales a través de una interfaz gráfica.

### 3. ¿A qué nos referimos cuando hablamos de lenguaje del lado del cliente? Mencione ejemplos.
Son aquellos lenguajes que son totalmente independientes del servidor, lo que permite que la página pueda ser albergada en cualquier sitio. Estos lenguajes son directamente "digeridos" por el navegador y no necesitan un pretratamiento.

* **Ejemplos:** HTML, Java (Applets), JavaScript y CSS.

### 4. ¿A qué nos referimos cuando hablamos de lenguaje del lado del servidor? Mencione ejemplos.
Son los lenguajes que son reconocidos, ejecutados e interpretados por el propio servidor. Una vez que el servidor procesa el código, envía el resultado al cliente en un formato que este pueda comprender.

* **Ejemplos:** CGI (habitualmente escrito en Perl, C, C++ o Visual Basic), ASP.net, PHP y Java Server Pages (JSP).

### 5. ¿Puedo conectarme a una base de datos utilizando HTML?
No. HTML es un lenguaje del lado del cliente que se utiliza exclusivamente para indicarle al navegador dónde colocar texto, imágenes o videos, y la forma que tendrán en la pantalla. El almacenamiento de información ocurre en la "capa de datos", que incluye la base de datos en sí, y las validaciones ocurren en la "capa de negocios". Para conectar y manipular datos se requiere obligatoriamente un lenguaje del lado del servidor.

---

## Web Estáticas y Dinámicas

### 1. ¿Qué es una página web dinámica? Mencione sus características.
Es una página interactiva generada por una aplicación web orientada a la presentación. Sus características principales son que combinan lenguajes de marca (como HTML o XML) con contenido dinámico generado en respuesta a las peticiones, requiriendo aplicaciones y procesamiento en el servidor.

### 2. Nombre 3 ejemplos de ellas.
Un formulario web de inscripción, donde los datos pasan por una capa de presentación, luego son verificados en una capa de negocios y finalmente guardados en una base de datos.

* **Otros ejemplos actuales:** Plataformas de comercio electrónico como Amazon y redes sociales como Facebook.

### 3. ¿Qué es una página web estática? Mencione sus características.
Una página web estática es aquella cuyos archivos se entregan al navegador del usuario exactamente como están almacenados en el servidor, sin pasar por un procesamiento previo. Sus características principales son el uso exclusivo de lenguajes del lado del cliente (como HTML y CSS) y que su contenido es el mismo para todos los usuarios a menos que un desarrollador modifique el código fuente.

### 4. Nombre 3 ejemplos de ellas.
1. El portafolio online básico de un fotógrafo.
2. Una página de "Próximamente" o "En construcción" para un sitio que aún no se lanza.
3. Una landing page informativa sencilla de un restaurante local que solo muestra su dirección, teléfono y un menú fijo.

### 5. En la actualidad, en qué caso utilizaría cada uno de ellas.
* **Páginas estáticas:** Se utilizan cuando se requiere un sitio meramente informativo, de bajo costo de alojamiento, que exija tiempos de carga muy rápidos y cuyo contenido no necesite actualizarse con frecuencia.
* **Páginas dinámicas:** Se utilizan en sistemas complejos que requieren paneles de administración de contenido, registro e inicio de sesión de usuarios, procesamiento de compras o manipulación constante de información en bases de datos.

---

## Instalación

### 1. ¿Qué aplicación utilizaron para instalar el servidor Web? Y ¿Por qué?
Se utilizó XAMPP. Se eligió porque es una herramienta todo en uno que integra de manera conjunta Apache, MySQL, PHP y Perl, destacando principalmente por su facilidad de instalación y uso, lo que permite levantar un servidor local "en un abrir y cerrar de ojos".

### 2. ¿Cómo puedo saber que versión de PHP tengo instalado?
Puedes averiguarlo ejecutando el comando `php -v` en la terminal o línea de comandos de tu sistema operativo. Alternativamente, puedes crear un archivo llamado `info.php` en tu directorio de servidor con el código `<?php phpinfo(); ?>` y abrirlo en tu navegador web.

### 3. Indique en qué directorio del servidor tengo que alojar mi sitio/sistema para poder utilizarlo/probarlo.
Por defecto en XAMPP, el directorio raíz donde debes alojar los documentos es `C:\xampp\htdocs`. En caso de que configures Hosts Virtuales para distintos proyectos, puedes establecer directorios personalizados, como por ejemplo `C:\miproyecto\httpdocs`.

### 4. ¿Qué archivo de configuración tengo que editar para mostrar/ocultar los errores en tiempo de ejecución? Y ¿Cuáles son las distintas opciones para eso?
Para configurar el reporte de errores en PHP, debes editar el archivo `php.ini`. Las opciones principales incluyen la directiva `display_errors` (que puede configurarse en `On` para visualizar errores durante el desarrollo, o `Off` para ocultarlos en un entorno de producción) y la directiva `error_reporting` (que define el nivel de errores a reportar, como `E_ALL` para mostrar todas las advertencias y errores).

### 5. ¿Cuáles son las variables que debo modificar para no tener grandes sobresaltos a la hora de implementar un sistema/sitio web?
Para evitar problemas de acceso y permisos (como "Problemas con Apache") al momento de configurar los directorios del host virtual, se deben modificar las siguientes variables dentro de la etiqueta `<Directory>` en el archivo `httpd-vhosts.conf`:

```apache
Options All
AllowOverride All
Require all granted