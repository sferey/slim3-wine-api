# slim3-wine-api

# Installation

`git clone https://github.com/sferey/slim3-wine-api.git`

`cd slim3-wine-api`

Pour s'informer si le module pdo_sqlite est installé

`php -m | grep pdo_sqlite`

Installation de php5-sqlite

`sudo apt-get install php5-sqlite`

Démarrage de l'application

`php -S localhost:8080 -t api api/index.php`

Installation de la BDD

[http://localhost:8080/v1/install](http://localhost:8080/v1/install)

## URL disponnible dans l'api
| Method | URL | SQL |
| ----- | --------- | --- |
| GET | http://localhost:8080/ping |
| GET | http://localhost:8080/v1/wines | SELECT * FROM wine ORDER BY name |
| GET | http://localhost:8080/v1/wines/{id:[0-9]+} | SELECT * FROM wine WHERE id=:id |
| PUT | http://localhost:8080/v1/wines/{id} | UPDATE wine SET ... WHERE id=:id |
| POST | http://localhost:8080/v1/wines	| INSERT INTO wine (...) VALUES (...) |
| DELETE | http://localhost:8080/v1/wines/{id} | DELETE FROM wine WHERE id=:id |
| GET | http://localhost:8080/v1/wines/search?name=BODEGA |	SELECT * FROM wine WHERE name LIKE %BODEGA% ORDER BY name |

## Les permissions d'accès HTTP

[Contrôle d'accès HTTP](https://developer.mozilla.org/fr/docs/HTTP/Access_control_CORS)

## Article sur les API

[Top 12 Best PHP RESTful Micro Frameworks (Pro/Con)](http://www.gajotres.net/best-available-php-restful-micro-frameworks/)

[Top 8 Java RESTful Micro Frameworks](http://www.gajotres.net/best-available-java-restful-micro-frameworks/)

## Outils pour les API RESTful

[Postman](https://www.getpostman.com/)
