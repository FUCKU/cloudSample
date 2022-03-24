# Introduction 
Repository store all microservice's config files. 

# Getting Started

<b>TODO: all microservice need create/update their config here</b>

1.	Folder name is environment name. e.g. "dev" is used for dev environment

2.	Standard name of the config file is :  \<application-name\>.yml
<br>e.g. "pg-sparc-product-service.yml"

3. <b>Structure of config repository:</b><br>
   
   * \<environment name\> &nbsp;&nbsp; -->folder name <br>
       > config.yml &nbsp;&nbsp;--> \<application name\>.yml <br>

    e.g.
    * -dev  -->folder name (*environment name/active profile name*)  
       > service1.yml &nbsp;&nbsp;-->\<application name\>.yml <br>
       > service2.yml <br>
       > service3.yml
    * -sit 
       > service1.yml   
       > service2.yml <br>
       > service3.yml


# Build and Test

<b>Local test guideline: </b><br>

Run docker command or compose :

````
docker run -it -p 8888:8888 -e SPRING_CLOUD_CONFIG_SERVER_GIT_URI=https://dev.azure.com/pg-consumer/SK-II-SPARC/_git/pg-sparc-cloud-configs 
-e SPRING_CLOUD_CONFIG_SERVER_GIT_DEFAULT_LABEL=main 
-e SPRING_CLOUD_CONFIG_SERVER_GIT_USERNAME=<user name>
-e SPRING_CLOUD_CONFIG_SERVER_GIT_PASSWORD=<password> 
-e SPRING_CLOUD_CONFIG_SERVER_GIT_SEARCH_PATHS='{profile}'
hyness/spring-cloud-config-server
````
After docker up: <br>
1. set your active profile 
2. then you will get your configurations 

# Contribute

