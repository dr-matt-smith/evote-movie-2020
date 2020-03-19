# evote-movie-2020

## About
This is a sequence of progressive enhancements, taking a static HTML site into an authenticated modern PHP MVC website

The website is about movies and user voted stars

## Progressive enhancement 

1. Starting point
    - a flat HTML website with hardcoded links
    
    - https://github.com/dr-matt-smith/evote-movie-2020-01-basic-html

2. Change HTML to PHP
      - change all `.html` file extension to `.php` 
      - in every page change the navigation links to files ending with `.php`
      
      - https://github.com/dr-matt-smith/evote-movie-2020-02-all-files-dot-php

3. Add Front Controller PHP OO architecture
      - move all display pages into folder `/templates`
      - move images and css into new folder `/public`
      - add root website script `/public/index.php` to create `WebApplication` object and invoke `run()` method
      - change all navigation links to the form `/index.php?action=<PAGE>`
         - e.g. `/index.php?action=about` for link to about page
      - create `src` folder containing classes `WebApplication` and `MainController`
      - create `WebApplication` class to test for value of `GET` variable `action` and choose which `MainController` method to invoke
      - create `MainController` class with methods to display each of the page templates

    - https://github.com/dr-matt-smith/evote-movie-2020-03-front-controller
      

## Steps todo ... 

    
- Twig templates

- Header and Footer
      - remove common header and nav content to `_header.php`     
      - remove common footer content to `_footer.php`
      - add `require_once` to all pages to read in common header and footer
      - NOTE: we have lost title page name and current page nav indicator - we'll fix this soon :-)
      
- Current page name in HTML title
        - controller functions to pass values

- Current page indicated in nav bar CSS
        - controller functions to pass values

- List details from array

- Movies list from a Repository class

- List details from array of objects

- Move controller functions into a controller class

- List details from array of objects from DB

- Page to insert new movies into the datbase

- Links to delete movies from the database

- Link and form to EDIT movies

- List CHEAP movies - custom SQL method in Repository class
    
- Login to protect the database CRUD
    
- Movie-Category - DB many-to-one relationship
    
- Movie Charts - DB Many-to-many relationship

- different user ROLES

- Sticky forms if validation error
- Web user testing (acceptance testing with Codeception)



