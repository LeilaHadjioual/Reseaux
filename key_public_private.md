##CREER UNE CLE PUBLIQUE ET PRIVEE  


**1 - Pour verifier si clé ssh dejà existante** (facultatif) 
    
        $ cd ~/.ssh  
        
                  
        
**2 - Créer une clé SSH (sous git en local et non pas sur le serveur)**

        $ ssh-keygen 
        le chemin existe par défaut, le modifier si besoin
        passphrase : aucun
        
        
*Pour info :*  
public key = id_rsa.pub  
private key =  id_rsa  
on les retrouve dans le dossier .ssh  


        
**3 - Copier la clé dans le serveur** (sous git en local)
        
        
        $ ssh-copy-id user@host    //"le user@host est : root@ilot.digital"
        
        -Si 1ère connection, demande confirmation de connection, repondre yes
        
        -Demande le mdp, le taper  
        
        
**4 - Vérfier si la clé est bien copiée sur le serveur**  

        -se connecter au serveur via adresse (ssh root@adresseIP)
    
        -si aucun mdp demandé : TOUT EST OK
        
