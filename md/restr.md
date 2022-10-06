## Restringir el acceso a una página web por IP:

Debe estar habilitado el módulo authz_host
    
    a2enmod authz_host

Se puede hacer por dos métodos:
- Con la directiva Order deny,allow (No recomendable, descatalogada)
- Con la directiva Require
<br>
#### Método Order allow, deny (no recomendado)
Denegar todo y permitir una IP/subred.

    <VirtualHost *:80>
	    ...
	    <Directory /directorio/web/>
		    Order allow,deny
		    Allow from 192.168.0.0/24
	    </Directory>
    </VirtualHost>

<br>
#### Método Require (Módulos --> mod_auth_host - Require)
Permitir a todos y denegar a uno.

    <VirtualHost *:80>
	    ...
	    <Directory /directorio/web/>
		    <RequireAll>
			    Require all granted --> permitir a todo
			    Require not ip 192.168.0.0/24
		    </RequireAll>
	    </Directory>
    </VirtualHost>  
<br>
Permitir a todos y denegar a un conjunto de host.

    <VirtualHost *:80>
	    ...
	    <Directory /directorio/web/>
		    <RequireAll>
			    Require all granted --> permitir a todo
			    Require not host host.ejemplo.es host2.dominio.es bloquear.es
		    </RequireAll>
	    </Directory>
    </VirtualHost>
 <br> 
Denegar todo y permitir a uno

    <VirtualHost *:80>
	    ...
	    <Directory /directorio/web/>
    		<RequireAll>
	    		Require all denied --> denegar a todo
		    	Require ip 192.168.0.0/24
    		</RequireAll>
	    </Directory>
    </VirtualHost>
