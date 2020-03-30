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
