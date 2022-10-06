
**ServerName** *paco.com* --> indica el nombre del servidor.<br><br>
**ServerAdmin** *paco@paco.com* --> mail del administrador de la web.<br><br>
**ServerAlias** *www.paco.com paco.net* --> indica otros nombre para el servidor<br><br>
**DocumentRoot**  */home/paco* --> indica el directorio donde están los archivos de la web.<br><br>
**DirectoryIndex** *paco.html* --> indica el nombre del archivo índice de la web, si no se indica nada coge los nombre de archivo por defecto indicados en el archivo /etc/apache2/mods-available/dir.conf<br><br>
**< Directory /var/www > … < /Directory >** --> se utiliza para establecer las opciones sobre el control de acceso del directorio indicado. Como por ejemplo restringir el acceso a la web, configuración de autenticaciones, etc…<br><br>
**ServerSignature** *Off* --> para que no aparezca el nombre del servidor cuando no hay una web.<br><br>
