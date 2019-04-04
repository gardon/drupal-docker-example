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

1. `docker-compose run drush [drush-cmmd]` for drush commands
1. `docker-compose run drupal [drupal-console-cmd]` for Drupal Console commands

