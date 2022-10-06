
    
    <VirtalHost *:80>
	    ServerName dominio.es
	    ServerAlias www.dominio.es
	    ServerAdmin admin@dominio.es
	    DocumentRoot /directorio/web
    </VirtualHost>

Habilitar el sitio ¡¡IMPORTANTÍSIMO!!:

    a2ensite /etc/apache2/sites-available/dominio.es.conf

Después hay que reiniciar Apache para que funcione tal y como se explica en el apartado [servicio apache2](servicio.md)

### Añadir Alias:
	
	<VirtualHost *:80>
		...
		ServerAlias www.dominio.es web.dominio.es
		...
	</VirtualHost>

