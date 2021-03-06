## General information

Website: http://www.geniuswiki.com

Github home page: https://github.com/GeniusWiki/GeniusWiki

License: GNU General Public License version 2

##  What is GeniusWiki

GeniusWiki is a free open source enterprise level wiki software. It is a web system that is able to create, share and collect knowledge, ideas and files etc. It is the better way to set up your organization Intranet or create a public website. It runs for geniuswiki.com and hosts thousands users and spaces in last 4 years that never fail users expectations. 

Here are some highlight features:

* Powerful markup or WYSIWYG editor by seamless switching.
* Customized dashbard
* Fine-grained access control
* Skins and Themes
* Support keyboard shortcut
* Powerful administrator portal
* Easy to install and upgrade
* Support most popular Java web server and database - MySQL, PostgreSQL, Oracle, DB2, SQL Server and HSQL 
* Plugins framework
* Keyboard shortcut support
* Full text searching with advanced search options
* Many fancy functions, watch/favorite list, comment, page tree, draft auto saving, revision, and DND dashboard etc.

More detail for build, installation and development,  please visit our document wiki space:
[GeniusWiki Document Center](http://www.geniuswiki.com/page/GeniusWiki+document/GeniusWiki+document)


##  Build

```
ant ivy.retrieve
ant package
```

## Docker

Switch to folder ./docker and build `docker-build.sh` to create docker image. After success build, run `docker-compose up -d`.  Open http://localhost:8080 in your browser. 

In setup step, 
* In 2nd step is using default data root option, simply click 'OK'. 
* In 3rd step, replace `127.0.0.1:61616` with `activemq.docker.geniuswiki:61616` for activemq address. **Must TURN OFF** `Use embedded ActiveMQ server` option.
* In 4th step, choose `MySQL` database, fill the host with `mysql.docker.geniuswiki`, root user name is `root`, root password is `password`, user name/password/retype password is any value you prefered for your database login.

All data, include database, log, uploads files are saved into ./docker/data directly. If you want to refresh install geniuswiki, just simply delete all files and folders under ./docker/data.


Note, if you cannot success build geniuswiki in `docker-build.sh`, download [latest release from github](https://github.com/GeniusWiki/GeniusWiki/releases) and copy geniuswiki.war to ./docker/geniuswiki/ folder, then comment ant command in docker-compose.yaml and try again.


Sponsor by [PlatoForms](https://www.platoforms.com). PlatoForms is an online form builder to help customers converting their PDF as a common web form. 