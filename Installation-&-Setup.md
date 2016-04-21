# Installation & Setup Guide

The following sections detail the process for setting up Atlas and its dependencies.

## OHDSI Web API

1. [Install WebAPI](https://github.com/OHDSI/WebAPI/wiki/WebAPI-Installation-Guide) and configure the appropriate sources. The following figure provides an example topology to show the different elements involved in the WebAPI architecture and a visual representation of the [source configuration](https://github.com/OHDSI/WebAPI/wiki/Source-Configuration):
	


**Note:** The example above does not represent a physical architecture. The WebAPI configuration allows you to physically and logically segregate these data sources based on the requirements of your environment. 

## CDM Statistics (Achilles)

1. This page includes information and resources for setting up Achilles in your environment: [installation and support](http://www.ohdsi.org/web/wiki/doku.php?id=documentation:software:achilles). This is prerequisite before you can use the data sources feature within Atlas. Once you have successfully generated summary statistics and have exported your data to JSON format, you are ready to configure Atlas to use this information.

## Atlas

1. Grab the latest release of Atlas from here: https://github.com/OHDSI/Atlas/releases. Download and install this onto a web server such that the application will be reachable via the URL: http://<your_webserver>/Atlas .

2. Under the Atlas root folder, edit the file $/js/config.js to configure the following properties:

            define([], function () {
                var config = {};
        
                config.services = [{
                    name: '<YOUR ENVIRONMENT NAME>',
                    url: 'http://your_webserver/WebAPI/'
                }];
                
                config.webAPIRoot = config.services[0].url;
        
                config.dataSourcesLocation = '/achilles/data/datasources.json';
                config.dataSourcesRoot = '/achilles/data';
 		
                return config;
              });

    - Config.services: Edit this array to provide a name for your environment and the URL for the WebAPI that was set up in WebAPI section.
    - Config.dataSourcesLocation & Config.dataSourcsRoot: If you have set up your CDM statistics (Achilles), these properties should be set to the URL where your CDM statistics resides. In the configuration below, we are using a relative path since we assume you have hosted your CDM statistics on the same web server as Atlas but under a different directory.

3. Navigate to Atlas from your web browser: http://your_webserver/Atlas