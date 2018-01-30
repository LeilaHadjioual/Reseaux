##PROCEDURE HTTPS  

se mettre à la racine
  

    $ sudo apt-get install python-certbot-apache -t stretch-backports  
    

    $ sudo certbot --authenticator webroot --installer apache
    
choisir le nom où installer le https (taper le chiffre qui correspond)

    taper 1 pour confirmer
        
entrer la route du projet  
  
     ex : /var/www/html/Leila/machine_cafe_laravel/public  
        
     select the appropriate number : taper 2 
