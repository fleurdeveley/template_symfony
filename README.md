# template_symfony

## Description
  * Ready to use symfony template.

## Technologies
  * PHP 7.4
  * Symfony 5.4
  * Composer 2.1.5

## Source
 1. Clone the GitHub repository :
```
  git clone https://github.com/fleurdeveley/template_symfony.git
```

## Installation
 2. Enter the project file :
```
  cd [project name]
```

 3. Configure your environment variables :
  * containers de Docker, à la racine du projet : 
```
  cp .env.example .env
```
 * SMTP server and database
```
  cp app/html/.env app/html/.env.local
```

 4. Create the docker network
```
  docker network create [project name]
```

 5. Launch the containers
```
  docker-composer up -d
```

 6. Enter the PHP container to launch the commands for the database
```
  docker exec -ti [nom du container php] bash
```

 7. Install php dependencies with composer
```
  composer install
```

 8. Leave the container
```
  exit
```

## Project
    * Connection to PHPMyAdmin : http://localhost:8082

## Database
  * Connection to PHPMyAdmin : http://localhost:8081
  * Server : [project name]_mysql
  * User : admin
  * Password : password

## Author 
Fleur (https://github.com/fleurdeveley)
