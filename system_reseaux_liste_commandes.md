

|COMMANDES  |UTILISATION  |EXEMPLE     |
|-----------|-------------|------------|
|passwd     |modifie le mot de passe|   |
|pwd|situe dans quel rép on est|	
|ls	|affiche le contenu |
|cd *nom rep*|Change de répertoire (rentre dans le répertoire)	|
|cd ..|remonte d’un cran (cd ../../) 2 crans, etc.|
|cat *nom fichier*|Affiche le contenu du fichier|Cat    $(find .) affiche tout|
|cat *	|affiche tout le contenu du répertoire|
|nano *nomfichieràcreer.txt* ou *repertoire*|créer un fichier ou répertoire|
|nano *nom fichier*|pour modifier du texte dans un fichier (ctrl o ; entrer ; ctrl x)|
|rm *nomfichier*|supprime le fichier|	
|mv *nomfichier* ../../ *nomfichier destination*|déplace un fichier|
|mv *anciennomfichier nouveaunom*|change le nom d’un fichier|
|cp	|copier des fichier|cp fichier1.txt fichier2.txt cp /tmp/fichier1.txt /home/plv/ cp -rp /home/plv/repertoire1/ /home/plv/repertoire2|
|find	|parcourir des répertoires seulement des noms de fichiers	|find . ou find . -name ‘*.php’ ou find . -type d ou find.grep .players|
|Grep  grep -i (casse) grep -u (num ligne) grep -v (ignore un mot) grep -r (recherche dans tous dossiers et sous dossiers) |recherche une chaine de caractère dans un fichier. note : grep est souvent utilisé avec find. Parcourt le contenu d’un fichier |	grep Toto fichier.txt grep -i toto fichier.txt find . | grep foo find . -type f -exec grep -iH foo {} \; |
|pipe	|Permet d’envoyer le résultat d’une commande à une autre commande	ls | grep “foo” : cherche dans un répertoire un fichier dont le nom contient “foo” cat toto.txt | grep “bar” : renvoie les lignes du fichier toto.txt qui contiennent “bar”|
|man	|affiche l’aide d’une commande unix |	man ls  man cp |
|chmod	|change les droits d’un fichier |	chmod a+rwx fichier1 chmod u+w /tmp/fichier2|
|ln -s|crée un lien “symbolique” vers un fichier	- ln -s fichier.txt mon_lien.txt ln -s /destination/fichier mon_lien |
|ssh	|se connecter à une autre machine |	ssh user@hostname ssh root@172.22.119.xxx |
|./mon_script.sh |	exécuter un programme ou un script|	./mon_script.sh /home/plv/mon_script.sh cd /home/plv/ ; mon_script.sh |
| Sortnom.txt |	 Trier le contenu	|
|Uniq	|Supprime les doublons|	
|Cut	|Coupe une partie d’un fichier	|
|Mkdir nomficheracreer	|Créer un fichier ou dossier	
|For do done	|Boucle pour modifier nom de tous les fichiers	|For f in .txt do $f |
		
		
		


