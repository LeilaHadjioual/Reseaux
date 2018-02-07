PROCEDURE HTTPS 
---- 
protocole sécurisé  

**Se mettre à la racine**
  
        $ sudo apt-get install python-certbot-apache -t stretch-backports    
        $ sudo certbot --authenticator webroot --installer apache
    
**Choisir le nom où installer le https (taper le chiffre qui correspond)**

        taper 1 pour confirmer
        
**Entrer la route du projet**  
  
        ex : /var/www/html/Leila/machine_cafe_laravel/public  
        
        select the appropriate number : taper 2 
