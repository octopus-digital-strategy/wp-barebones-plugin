#Bare Bones WordPress Plugin
 
This project helps you build a WordPress plugin faster.
Some elemental tasks have been pre-configured so you can get down to coding.

**This Bare Bones uses [Composer](http://getcomposer.com) to handle PSR-4 autoloading.** 

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

1. Download the files to your local plugin directory
2. Rename the directory from **bare-bones-wp-plugin** to **YOUR-PLUGIN-NAME**
3. Customize your Plugin Name
4. Change the Namespace
5. Dump autoload
6. Add styles and scripts as needed

###Steps 1 and 2

Right now you have 2 options to get this project **Cloning** the repository, or **Download** the current release.


###Cloning

From your terminal window

```bash
cd /path/to/your/plugins/directory/

git clone https://github.com/octopus-digital-strategy/barebones-wp-plugin.git

mv ./barebones-wp-plugin ./your-plugin-name


```

###Downlad 

* Go to [Bare Bones WordPress Plugin Github Project](https://github.com/octopus-digital-strategy/barebones-wp-plugin)
* Click on download zip
* Unzip on your local plugins directory
* Rename the directory from **bare-bones-wp-plugin-NUMBER** to **YOUR-PLUGIN-NAME**


The steps 3 to X are equal for either od these options.

###Step 3 Customize Plugin Name

Open the file init.php within your plugin folder. Locate the first comments-block and customize it accordingly   

```php

/**
 * Plugin name: YOUR PLUGIN NAME
 * Plugin URI: http://LINKTOYOURPLUGIN.COM
 * Description: QUITE TO OBVIOUS
 * Version: 0.1
 * Author: YOUR NAME
 * Author URI: http://YOURWEBSITE.COM
 */


```

###Step 4. Change Namespace

To accomplish this task you have to locate 2 files. composer.json on the root of your plugin and SetupPlugin.class.php on the **src/** directory

Change **BareBonesPlugin** to **YourPluginNameSpace** remember that in composer.json the namespace always ends with two forward slashes ** \ \ **

###Step 5. Dump Autoload

You are almost ready to get coding. The only thing you have to do is to dump the autoload. 

```bash

cd path/to/your/plugin/root

composer dump-autoload -o

```

This command will generate the class map for autoloading of the SetupPlugin class used on the init file. And all other classes with the proper [PSR-4](http://www.php-fig.org/psr/psr-4/) within your **src/** directory

Remember to run this command every time you add a class.

###Step 6. Scripts and Styles

SetupPlugin.class.php contains code and files where you can place your scripts and styles out of the box. 

If you want to add another resource like javascript, views, templates or files, add an extra folder on the ***resources/*** directory and use the static method **getResourceURL** or **getResourceDirectory** to get a path to the file. 


##Change Log


###Version 0.1

* Implemented SetupClass instance on init.php file 
* Added empty css and js files
* Added readme file with basic documentation
* Implemented pre-configured css and script enqueue for both admin and front end
* Added Basic Setup class 
* Added WordPress Plugin comments
* Implemented Basic Init File with Composer autoload implementation
* Implemented Composer PSR-4 autoload configuration
