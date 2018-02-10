##FAILLE SECURITE WEB  

51.15.215.183 à taper dans URL  
se loguer

Exemple de faille xss
   
   Dans le champs message, taper le message suivant :
   
     <script>alert("pwnd");</script>


###Exemple d'injection SQL

Dans le champs message, taper la chaîne :  
	
	    test', 'tutu') #

Cela nous permet d'écrire un message sous le nom de quelqu'un d'autre  

###Solutions  

Pour éviter les failles sur le login, message, ajouter dans le code login et message

        ajouter htmlescapechars()  
    
Pour eviter les faille injection SQL , ajouter dans la requete SQL

        mysql_escape_string()   //deprecated
        
        utiliser :  
        mysql_real_escape_string()