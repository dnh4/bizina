# Bizina
Mise en place d’un système de gestion d’offres et de demandes. Pour la societe AM WEB SOLUTIONS
![Apercus du projet](bizina.png)
## Mise en place et installation
- Cloner la repository
``` 
git clone https://github.com/dnh4/bizina.git
```
- Builder les images postgres et pgadmin
Vous avez acces a la pgadminsur `http://localhost:5001` apres ce commande
```
docker compose up -d
```
- Installation des bundules et lancement du serveur
```
cd code
composer install 

#Faire la migration de Version20240319061552 pour avoir le meme migration
php bin/console doctrine:migrations:migrate 'DoctrineMigrations\Version20240319061552
````
- Lancement du serveur
```
symfony server:start -d
```
- Stoper le serveur
``` 
symfony server:stop
```