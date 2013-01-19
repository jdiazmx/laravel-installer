l4i
===

Laravel 4 Install Script for Linux

This script will install a working development structure of Laravel 4 with a basic Twitter Booststrap template.

### Motivation

Some people asked me if Laravel 4 needed a installation script, actually it doesn't, it's better if you can install it manually, but if you're doing it many times, this script can save you a lot of time. Also, if you are a newbie, it takes some time and work until you get a working version of Laravel 4 really working, because you have to understand and install Composer, install PHPUnit, install some basic packages, create a Virtual Host on your webserver, point it correctly to your app directory and set the right permissions on storage folder...

### Requirements

You basically need a Linux box with PHP and a webserver (nginx, apache2 or lighthttpd) installed.

### Process of installation

* Git clone the current laravel app repository
* Install Composer
* Install PHPUnit (using Composer)
* Install packages: meido/Form, meido/HTML, raveren/kint
* Create VirtualHost (currently apache2 only) and restart webserver
* Download, install and configure Twitter Bootstrap from git
* Configure a main template, a home view using main template and a route to home, so we can see Laravel 4 and Blade running

### Screenshot 

![image from redmond barry building unimelb](http://puu.sh/1PI8I)

### Installed software

In the process of intalling Laravel 4, this script will also try to install, if needed, the following applications in your system:

* Composer (http://getcomposer.org/)
* git 
* curl
* PHPUnit (composer install)
* Twitter Bootstrap

### Installation and Examples

There is no need to clone this git repository, you just have to download the script:
```
wget -N --output-document=installFour.sh https://raw.github.com/antonioribeiro/l4i/master/installFour.sh
```

And run it:
```
bash installFour.sh <install directory> <site name> <Install twitter bootstrap? YES or NO>
```

Examples of usage:
```
bash installFour /var/www/blog blog YES
bash installFour /home/taylor/www blog NO
bash installFour /var/www/blog myBlog YES
```

### Tested Operating Systems

* Debian Squeeze 6.x
* Ubuntu Derver 11.10
