## Servicio Apache2:
**Con los comandos de servicio de Linux:**<br>

- Arranque:<br>
    
        sudo service apache2 start
        o
        /etc/init.d/apache restart

- Parada:<br>
    
        sudo service apache2 stop
        o
        /etc/init.d/apache stop

- Reinicio:<br>
    
        sudo service apache2 restart
        o
        /etc/init.d/apache restart

- Forzar lectura de la configuración sin parar el servicio<br>
  
        sudo service apache2 reload
        o­       
        /etc/init.d/apache reload

- Comprobar el estado<br>
­       
        sudo service apache2 status
        o
­       /etc/init.d/apache status

<br>
**Con los comandos propios de Apache desde la consola de Linux:**<br>

- Arranque:
        
            sudo apache2ctl start

- Parada
­
            sudo apache2ctl stop

- Reinicio:

    ­       sudo apache2ctl restart
    
- Forzar lectura de la configuración sin parar el servicio

            sudo apache2ctl gracefull
    
- Comprobar el estado

            sudo apache2ctl status

<br>
**Habilitar/Deshabilitar sitios y módulos**

- Habilitar módulo

        a2enmod nombredelmodulo

- Deshabilitar módulo
    
        a2dismod nombredelmodulo

- Habilitar sitio
  
          a2ensite nombredelarchivodeconfiguraciondelsitio

- Deshabilitar sitio

            a2dissite nombredelarchivodeconfiguraciondelsitio


**IMPORTANTÍSITIMO**<br>
Luego de habilitar/deshabilitar se tienen que reiniciar Apache.
