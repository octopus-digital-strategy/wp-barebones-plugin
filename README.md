#Bare Bones WordPress Plugin
 
This project helps you build a WordPress plugin faster.
Some elemental tasks have been pre-configured so you can get down to coding.

**This Bare Bones uses [Composer](http://getcomposer.org) to handle PSR-4 autoloading.** 

This OSS project is courtesy of [Octopus Digital Strategy](http://octopus.mx) released under [GPL License](https://www.gnu.org/licenses/gpl.txt).

The software is released as-is.   

Developed and hopefully maintained by [Page-Carbajal](http://pagecarbajal.com).
 


##Features

* Readme file with implementation instructions
* WordPress Plugin comments
* Pre-configured css and script enqueue for both admin and front end
* Basic Setup class 
* Basic Init File with Composer autoload implementation
* Composer PSR-4 autoload configuration

##How to use this Bare Bones

Visit the [Getting Started Guide](https://github.com/octopus-digital-strategy/barebones-wp-plugin/wiki/Getting-Started-Guide) to understand how to use this project.  

##Change Log


###Version 0.1.2

* Tagged to 0.1.2 
* Fixed loadTextDomain errors 


###Version 0.1.1

* Fixed small error on enqueueScripts and enqueueStyles. Both functions were using SetupPlugin::getResourceDirectory instead of SetupPlugin::getResourceURL to get the URL to the file.
* Added link to the Getting Started Guide
* Getting Started documentation was moved to the Wiki of the project


###Version 0.1

* Tag for release 0.1
* Implemented SetupClass instance on init.php file 
* Added empty css and js files
* Added readme file with basic documentation
* Implemented pre-configured css and script enqueue for both admin and front end
* Added Basic Setup class 
* Added WordPress Plugin comments
* Implemented Basic Init File with Composer autoload implementation
* Implemented Composer PSR-4 autoload configuration
