# What is bootlex?

Bootlex is a theme for the [pelican](https://github.com/ametaireau/pelican) static blog generator.
It is based on a modified bootstrap and works nicely with a lot of pelican features.

# Installation

Just pull the repo with `git clone git://github.com/alexex/bootlex.git` and include its location via the `THEME` option in your settings.py

There are some required settings you will need though:

1. Your `SITEURL`must have a **trailing slash**
2. You need to enable `CLEAN_URLS`

You will probably need some RewriteRules for your Webserver aswell, my `.htaccess` looks like this:

	::apache
	RewriteEngine On
	
	RewriteBase /

	RewriteCond %{REQUEST_FILENAME}.html -f
	RewriteRule ^(.+)/$ $1.html [L]
	
# Features

You can make use of the following settings:

* Pages (will be included in the menu automatically)
* MENUITEMS (will be included aswell)
* LINKS (as the above)
* Analytics (will be included automatically, if set)

# Missing

I do not know whether it works, but as I never cared about it, I suppose that Categorys will not work properly
