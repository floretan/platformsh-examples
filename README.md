# Example configuration for Platform.sh

This is a minimal custom PHP application with Mysql connectivity

It has a very minimal `.platform/routes.yaml` file. It will only respond on the
naked domain.

In the very minimal `.platform/services.yaml` file we declare a single MySql
service we call "mysql" and we allocate 2GB of disk space to it. 
In `.platform.app.yaml` (on line 6) we will call this mysql instance "database"
which is the name that will appear in the environment variable 
"PLATFORM_RELATIONSHIPS" and that we will use in our index.php

> **Note:** In the default configuration of Platform.sh we provide MySql, Redis
> and Solr, so actually this configuration removes Solr and Redis). 

In `.platform.app.yaml` we set the web root to be the root of the repository 
and we serve all non static calls from index.php (here we have just a single
image.jpg at the root).