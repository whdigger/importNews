# Module for importing news to a site from the RSS feed
Should be developed, then convert it into news entities on website.
News entity consist of:
* Title
* Body
* Image (the main image of the news, should be stored on local server)
* Source (link to the news object’s source - details news page)

Also follow further conditions:
Keep in mind that there should be a possibility to import new news from time to time when RSS feed updates.
For every item take the first image from images listed under content attribute and store image on a local server.
This module should be installed to website as composer dependency.

Getting started
------------
This build includes CMS Drupal 8, Docker4Docker, the import module, and the news entity config.

Installation
------------
For project deployment, you must perform the following commands was in the folder with the project
```
git clone https://github.com/whdigger/importNews.git && cd importNews
make env && make up && make start && make shell
composer install
make settings && drush cr && drush sql-cli < backup/dump.sql
```
Log in via the browser at the address import.localhost, password for the database (username: drupal, password: drupal, database name: drupal).
Username: admin and password: admin

Example of use
------------
Examples of usage are described in this module https://github.com/whdigger/import
