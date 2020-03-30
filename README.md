# Docker-X-Symfony

Ma premiere images avec docker.

#Details:
- SymfonyMailDev:http://localhost:8002/#/
- Symfony_db_:http://localhost:3307/
- SymfonyphpmyAdmin:http://localhost:8080/
  - Login phpMyAdmin: root/
- Symfony_PHP710:http://localhost:9071/
- Symfony_PHP720:http://localhost:9072/



Arborescence:
MonFichierDeTête:
- php71
  - DockerFile
  - php.ini
- php72
  - DockerFile
  - php.ini
- vhost
  - stackfs.conf
- vhosts
- docker-compose.yml


Premiers pas:
Une fois 'linstallation effectué, on va pouvoir créer notre projet symfony (tro bi1).
On va se connecter au bash d’un contenaire php (peu importe lequel).

Alors vous avez deux possibilité pour ce faire soir vien un terminal et avec la commande suivante:

***
docker exec -u 1000 -it $(docker ps -aqf « name=php71 ») bash;
***

Soit en allant sur le dashboard de docker, dans l'onglet "container list", et vous choisissé le container lancer avec php.
Selectionné le button "CLI" et hop un terminal vas souvrire directement dans le repertoir '/www/'

Vous arrivez dans le répertoire www, vous pouvez donc exécuter votre commande favorite :

***
composer create-project symfony/website-skeleton 'MyApp'
***

Surtout ne pas oublier le pack apache :

composer require symfony/apache-pack

Il n’y a plus qu’à se rendre sur MyApp.localhost:9071 et 9072, et vérifier que les version de PHP soient bien différentes.
