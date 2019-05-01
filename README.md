# Docker-compose environment for Drupal projects

This very simple setup contains a minimalistic approach for using Docker Compose and Composer to build a local environment.

# Requirements

1. Docker
1. Docker Compose
1. Composer

# Setup

1. `composer install`
1. `docker-compose up -d`
1. Navigate to http://localhost to install and use Drupal site, DB credentials:  
  Host: "db"  
  Database name: "drupal"  
  Database username: "drupal"  
  Database password: "drupal"
  
> Note: If you want to install using Drush, you may need to use the `cli` container (See below), and then install mysql client:
```
$ apt-get update
$ apt-get install mysql-client
```

# Usage

- Drush and Drupal Console:
  ``` 
  $ docker-compose run cli
  $ drush 
  $ drupal
  ```
- PHPMyAdmin: Navigate to `http://localhost:8001`
- Installing modules:
  ```
  $ composer require drupal/examples
  $ docker-compose run cli
  $ drush en examples
  ```
