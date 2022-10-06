## Permitir listar contenido de un directorio:
    <VirtulHost *:80>
	    ...
	    <Directory /home/usuario/documentos/pdfs/>
		    Options Indexes FollowSymLinks
		    Options Indexes
	    </Directory>
    </VirtualHost>
