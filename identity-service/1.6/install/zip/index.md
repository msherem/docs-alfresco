---
title: Install Identity Service from ZIP file
---

The Identity Service can be installed using a standalone ZIP distribution. 
A default realm called `Alfresco` is installed.

## Prerequisites

-   Java 8 or Java 11 JDK installed

## Installation steps

1. Download the zip file for the Identity Service from the [Support Portal](http://support.alfresco.com/).

2. Move the downloaded zip file to install location of choice and unzip the contents:

    For a Linux or Unix environment:

    ```
    $ unzip alfresco-identity-service-1.6.0.zip
    ```

    For a Windows environment:

    ```
    > unzip alfresco-identity-service-1.6.0.zip
    ```

3. Change directory to the `bin` directory of the unzipped folder and run the standalone start script:

    > **Note:** To bind to all public interfaces use `0.0.0.0` as the value of `IP_ADDRESS` otherwise use the address of a specific interface.

    For a Linux or Unix environment:

    ```
    $ cd alfresco-identity-service-1.6.0/bin
    $ ./standalone.sh -b <IP_ADDRESS>
    ```

    For a Windows environment using a bat script:

    ```
    > ...\alfresco-identity-service-1.6.0\bin\standalone.bat -b <IP_ADDRESS>
    ```

    For a Windows environment using a Powershell script:

    ```
    > ...\alfresco-identity-service-1.6.0\bin\standalone.ps1 -b <IP_ADDRESS>
    ```

4. Navigate to `http://localhost:8080/auth` once the service has started.

5. Enter a username and password to create an administrator user for the master realm.


The administrator console for the `Alfresco` realm can be accessed at `http://localhost:8080/auth/admin/alfresco/console/`. The administrator user for this realm has the following credentials:

|Property|Value|
|--------|-----|
|Administrator username|`admin`|
|Administrator password|`admin`|
|Administrator email address|`admin@app.activiti.com`|
|Alfresco client redirect URIs|`*`|

> **Important:** Reset the administrator password for the `Alfresco` realm when first signing into its administrator console.

The Identity Service can be [configured]({% link identity-service/1.6/config/index.md %}) further.

