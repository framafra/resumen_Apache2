## Mecanismos de Autenticación
### BASIC
    <Directory "/var/www/html/privado">
       	AuthType Basic
	    require valid-user
	    AuthBasicProvider file
  	    AuthUserFile /etc/apache2/credenciales
 	    AuthName  "Sitio Privado"
    </Directory>

Creación de los usuarios y passwords

    htpasswd –c /ruta/al/fichero/de/passwords nombreusuario

### DIGEST
Para utilizarlo hay que activar el módulo auth_digest
    
    a2enmod auth_digest  

Y luego añadir:

    <Directory "/var/www/html/privadoDigest">
    	AuthType Digest
	    AuthName " Autenticacion Digest"
	    AuthUserFile /etc/apache2/credencialesdigest
	    Require valid-user
    </Directory>
    '''

Creación de los usuarios y passwords

    htdigest -c /etc/apache2/credencialesdigest ‘Autenticacion Digest’ paco

