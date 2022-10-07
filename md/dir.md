La ruta donde se encuentran los directorios y archivos de trabajo de Apache 2 es:
`/etc/apache2`
<br>  
Los más importantes son:
- **apache2.conf**: Es el archivo de configuración principal. En este archivo se incluyen todos los archivos de configuración adicionales.
- **envvars**: Este archivo se definen las variables de entorno que hacen referencia al servidor web Apache y se utilizan en el archivo apache2.conf.
- **ports.conf**: En este archivo se definen los puertos TCP donde el servidor Apache estará escuchando peticiones.
- **conf-available**: Este directorio contiene archivos de configuración que se aplican a todos los hosts virtuales de forma global.
conf-enabled: Este directorio contiene enlaces simbólicos a los archivos de configuración del directorio conf-available que están activos.
- **mods-available**: Este directorio contiene los archivos de configuración de los módulos que se pueden utilizar para añadir nuevas funcionalidades al servidor.
- **mods-enabled**: Este directorio contiene enlaces simbólicos a los archivos de configuración del directorio mod-available que están activos.
- **sites-available**: Este directorio contiene los archivos de configuración de los hosts virtuales.
- **sites-enabled**: Este directorio contiene enlaces simbólicos a los archivos de configuración del directorio sites-available que están activos.
