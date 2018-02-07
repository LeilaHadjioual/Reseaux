
#**DNS / REGISTRAR**  



- **DNS (Domaine name System):**  
	un DNS traduit un nom de domaine en adresse IP.
	Un serveur DNS sert à faire le lien entre des noms de domaine et une adresse IP  
	  
		ex : maps.google.com -> 216.58.204.110  


- **zone DNS :**   
	Une zone DNS est associée à un domaine. Elle associe tous les sous domaines à des adresses IP.  
	  
		exemple : campus-grenoble.fr IN A 23.45.132.98  
			www.campus-grenoble.fr IN A 23.45.132.98  
			mail.campus-grenoble.fr IN A 45.76.230.7


- **registrar (bureau d'enregistrement):**  
	désigne une société ayant choisi de se spécialiser dans l'enregistrement et la réservation de noms de domaine  


---


### ACHETER UN NOM DE DOMAINE  
*registrar : OVH ou Gandi*  
		 		 
	SOUS GANDI  
	  
1. créer un compte
2. taper un nom de domaine et sélectionner dans les propositions 
3. facturation
4. se connecter sur site Gandi
5. tableau de bord/domaines/ilot digital
6. configurer le domaine :  
  
        - enregistrement DNS : modifier IP , ajouter des sous domaines  
        - clic ajouter :  
            type : A 
            TTL : 300 sec  
            nom : nomsousdomaine 
            adress IP: 163.172.183.212  
					  
			*ex final : nomsousdomaine@ilot.digital*


---


###CREER UN VIRTUAL HOST

1. se connecter sur le serveur  

            ssh root@163.172.183.212
          
2. créer un fichier .conf dans etc/apache2/sites-available  
            création du fichier : nano leila.conf  
			insérer : *(ServerName et DocumentRoot important +++)*  
			
			<VirtualHost *:80>  
			    ServerName leila.ilot.digital
			    ServerAdmin webmaster@virtual.host
			    DocumentRoot /var/www/html/Leila
			    ErrorLog /var/log/apache2/virtual.host.error.log
			    CustomLog /var/log/apache2/virtual.host.access.log combined
			    LogLevel warn
			</VirtualHost>
3. créer le dossier projet  

            sous html : mkdir Leila

4. taper  
        
            a2ensite leila.conf

5. taper  

            service apache2 restart

6. ouvrir la page avec url  

            leila.ilot.digital

7. si affiche page projet, tout est ok

8. pour que laravel puisse retrouver le chemin des vues au delà de l'index  

	        a2enmod rewrite  

9. ajouter dans le fichier .conf (leila.conf) :  

	        <Directory/var/www/>  
		        Options Indexes FollowSymlinks  
		        Allowoverride All  
		        Required all granted  
	        </Directory>

10. redémarrer  
	
	        service apache2 restart  

11. rappatrier le projet machine à café dans le dossier du projet   
    (cf procédure recup projet laravel avec droits user et BDD)
