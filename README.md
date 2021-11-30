# SAS Customer Intelligence 360 - Extensions


## Overview
SAS CI360 Connector Framework and Agent SDK provide infrastructure to integrate CI360 applications with other applications. This repository contains a number of connectors and agents that are ready to be used to enhance the capabilities of CI360 and connect to 3rd party services. In addition, there are other integration assets included as well. All integration assets included in this repository are listed below, with short description. Details about each are included within specific sub-folders.

## Table of Contents

This topic contains the following sections:
* <a href="#prerequisites">Prerequisites</a>
* <a href="#installation">Installation</a>
* <a href="#list-of-extensions">List of Extensions</a>
* <a href="#getting-started">Getting Started</a>
* <a href="#contributing">Contributing</a>
* <a href="#license">License</a>
* <a href="#resources">Additional Resources</a>

## Prerequisites

Prerequisites vary between integration assets included here, and are listed in detail for each in the respecitive sub-folders. But some of the prerequisites include:
- Amazon Web Service account with access to Lambda and API Gateway service
- Microsoft Azure account with access to Functions and other Azure services
- Java 1.8 or newer
- Python 3.7 or newer

## Installation

Installation instructions for every extension are included in the project specific sub-folder README file. Installation and deployment instructions are platform specific.

## List of Extensions

This is a list of connectors and agents included in this repository:
- [__SMS/MMS Connector (via Syniverse)__](ci360-scg-connector): Syniverse Communication Gateway (SCG) connector, enables SMS and MMS communication through Syniverse
- [__WhatsApp Connector (via Syniverse)__](ci360-scg-connector): Syniverse Communication Gateway (SCG) connector, enables WhatsApp communication through Syniverse
- [__WeChat Connector (via Syniverse)__](ci360-scg-connector): Syniverse Communication Gateway (SCG) connector, enables WeChat communication through Syniverse
- [__SMS Connector (via SFMC)__](ci360-sfmc-connector): Salesforce Marketing Cloud (SFMC) connector, enables Email communication through Salesforce Marketing Cloud
- [__Email Connector (via SFMC)__](ci360-sfmc-connector): Salesforce Marketing Cloud (SFMC) connector, enables SMS through Salesforce Marketing Cloud
- [__SMS Connector (via Twilio)__](ci360-twilio-connector): Twilio connector, enables SMS through Twilio
- [__Google Analytics Integration__](google-analytics-integration): Implementation of connection with Google Analytics (GA)
- [__Facebook Event Manager Integration__](facebook-event-manager-integration): Implementation of connection with Facebook Event Manager
- [__Adobe Audience Manager Integration__](adobe-audience-manager-integration): Implementation of connection with Adobe Audience Manager (AAM)
- [__SAS ESP CI360 Adapter__](esp-ci360-adapter): SAS Event Stream Processing adapter that allows streaming of events from an ESP window to CI360
- [__SAS ESP Agent__](ci360-esp-agent): SAS Event Stream Processing agent enables streaming of CI360 events into ESP

## Getting Started

To set up and use the provided extension code you need to perform the following steps :

### Download sample code
1. Download a `ci360-extensions` project source code into zip/tar.gz/tar.bz2/tar file format on your local machine.<br/>
   `Note:` You can also clone the project on your local machine

2. The project will be downloaded on your local machine in your specified file format. You need to unzip/untar the downloaded project.  

3. You can see the folder `ci360-extensions` after unzip/untar the project.

4. Open the `ci360-extensions` folder. It will contain multiple sub-folders for various connector and agent integration resources.

### Build or Deploy
Build and deployment instructions are included for each of the integration assets in their respoective sub-folders.


### Deploying CI360 Connectors
Please refer [Set up a Custom Connector](https://go.documentation.sas.com/doc/en/cintcdc/production.a/cintag/ext-connectors-custom.htm) section in SAS Customer Intelligence 360 admin guide.

##### Register your connector into CI360

For most connector or agent integration assets, you need to register the connector and endpoint with these details into the CI360 system to use the connector. Details are included for each connector or agent in their sub-folders. Documentation sections are referenced below for eacy access.

**Add and Register a Connector**
Please refer to [`Add and Register a Connector`](https://go.documentation.sas.com/doc/en/cintcdc/production.a/cintag/ext-connectors-add.htm) in SAS Customer Intelligence 360 admin guide.

**Add an Endpoint**
Please refer to [`Add an Endpoint`](https://go.documentation.sas.com/doc/en/cintcdc/production.a/cintag/ext-connectors-add-endpoint.htm) in SAS Customer Intelligence 360 admin guide.

### Deploying CI360 Agents

For CI360 agent development, agent SDK needs to be downloaded and installed into the local Maven repository. See [`Download an Access Point SDK`](https://go.documentation.sas.com/doc/en/cintcdc/production.a/cintag/extapi-config-downloadsdk.htm) in SAS Customer Intelligence 360 admin guide.

To install SDK JAR into local Maven repository:
```
mvn install:install-file -Dfile=<path where CI360 agent was downloaded>/sdk/mkt-agent-sdk-jar-1.current release.jar -DpomFile=path where CI360 agent was downloaded/sdk/pom.xml
```

**Create an Access Point Definition**
Please refer to [`Create an Access Point Definition`](https://go.documentation.sas.com/doc/en/cintcdc/production.a/cintag/extapi-config-agentdefa.htm) in SAS Customer Intelligence 360 admin guide.


## Contributing

> We welcome your contributions! Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on how to submit contributions to this project. 


## License

> This project is licensed under the [Apache 2.0 License](LICENSE).


## Additional Resources

For more information, see [External Data Integration with Connectors](http://documentation.sas.com/?cdcId=cintcdc&cdcVersion=production.a&docsetId=cintag&docsetTarget=ext-connectors-manage.htm&locale=en#p0uwf5nm4rrkn1n1gwrm03rh911r).