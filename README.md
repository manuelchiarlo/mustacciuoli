#Mustacciuoli

This is an implementation of **[PHP Console](https://github.com/barbushin/php-console)** as a [WordPress](http://www.wordpress.org) plugin.


> PHP Console allows you to handle PHP errors & exceptions, dump variables, execute PHP code remotely and many other things using [Google Chrome PHP Console extension](https://chrome.google.com/webstore/detail/php-console/nfhmhhlpfleoednkpnnnkolmclajemef) and [PhpConsole server library](https://github.com/barbushin/php-console).

This implementation for WordPress allows you to test any WordPress specific function or class (including those introduced by your active theme and plugins!) from PHP Console terminal and inspect results, catch error and warnings with stack trace straight from Chrome Dev Tools console. 


## Installation

Follow these steps: 

1. First, install **[PHP Console for Google Chrome](https://chrome.google.com/webstore/detail/php-console/nfhmhhlpfleoednkpnnnkolmclajemef)**. 

2. Then, add this plugin to your WordPress installation (by placing it into your `wp-content/plugins/` directory). **Note:** If you are cloning or manually downloading this git repo from GitHub, make sure to init PHP Console git submodule (i.e. `lib\php-console` directory should not be empty - this step is not necessary if you happen to download this plugin from WordPress.org).

3. Once installed, activate WP PHP Console from WordPress plugins dashboard page; then go to `PHP Console` settings page from the `Settings` menu. From here you need to enter a password for the eval terminal (required, otherwise the eval terminal simply won't work).

### Options

In WP PHP Console settings page, you can also tick a checkbox to use the terminal only on a SSL connection (of course then if you don't have SSL the terminal simply won't work). You can also specify IP addresses to restrict the accessibility to the eval terminal (a single address eg. `192.168.0.4`; or an address mask eg. `192.168.*.*` or multiple IPs, comma separated `192.168.1.22,192.168.1.24,192.168.3.*`).   


## Usage

Once you have set up a password, you can navigate any of your WordPress page (including WordPress admin) and try the console. You will se a "key" icon in your browser address bar. By clicking on it, it will prompt for the password you have set just before. After entering the correct password, you can use the eval terminal and run any PHP code from it, including WordPress own functions. Furthermore, in Chrome Dev Tools console you will also see printed any PHP errors, warnings, notices with stack trace, which will be useful to debug your plugin or theme.  

### Caveats

You should not use this plugin or PHP Console library in a production environment, rather a development/testing environment. You will otherwise add more load to your server and even put your site at risk since you're exposing PHP code publicly.

### Browser support

Currently PHP Console only supports Google Chrome browser. If you're using for example Firefox or Opera this plugin won't be of much use to you at the moment.