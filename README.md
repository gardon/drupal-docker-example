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

# Usage

1. Drush and Drupal Console:
  ``` 
  $ docker-compose run cli
  $ drush 
  $ drupal
  ```
1. PHPMyAdmin: Navigate to `http://localhost:8001`
1. Installing modules:
  ```
  $ composer require drupal/examples
  $ docker-compose run cli
  $ drush en examples
  ```
