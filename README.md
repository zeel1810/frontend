<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://news.silabs.com/download/silicon-labs-logo-red-2014-1538x769px_1.jpg" width="200" alt="Nest Logo" /></a>
</p>

  <p align="center">Si labs project</p>

## Description

Si-labs projects

## Sections

- [Backend](#backend)
- [Frontend](#frontend)

## Backend

### Table of Contents

- [Purpose/Scope](#purposescope)
- [Prerequisites](#prerequisites)
  - [Hardware Requirements](#hardware-requirements)
  - [Software Requirements](#software-requirements)
  - [Azure Cloud Configuration](#azure-cloud-configuration)
- [Getting Started](#getting-started)
- [Run the Application](#run-the-application)
- [Test the Application](#test-the-application)
- [API Documentation](#api-documentation)

## Purpose/Scope

This application demonstrates how to configure the Azure device with iot hub and how to receive all the device sensor message on backend node server and display this on client side.

## Prerequisites

### Hardware Requirements

- A Windows/Linux/Mac PC
- A Wireless Access Point

### Software Requirements

- Install Nodejs >= v20.14.0
  - Install [Nodejs](#hardware-requirements)
- Install MongoDB >= 7.0
  - Install [MongoDB](#hardware-requirements)

### Azure Cloud Configuration

> **Note:**
>
> - Please follow the azure cloud readme to setup cloud configuration
> - Path of this readme file is [root-folder]/azure/readme.md

## Installation Of nodejs Version V20.14.0

1. Download from this link - https://nodejs.org/en/download/package-manager
2. Run the Installer.
3. Follow the Setup Wizard to finish installation
4. Run this command to check installed version

```bash
  node --version
```

## Installation Of MongoDB Community Server Version 7.0 with MongoDB Compass

- Download from this link - [Click Here](https://www.mongodb.com/try/download/community)
- Run the Installer.
- Follow the Setup Wizard to finish installation
- Launch MongoDB Compass from your applications folder or start menu
- Run this command to check installed version

```bash
  mongod --version
```

## Getting Started

### Create .env file

1. Go to [project-root-folder]/dashboard/backend
2. Create .env file
3. Put all the provided environment value in .env file

### Replace these environment variable With your actual value

```bash
    # path of .env file is [root-folder]/dashboard/backend

    STORAGE_CONNECTION_STRING='DefaultEndpointsProtocol=https;AccountName=sa1sasyd;AccountKey=rn3fsfwfvfdQs2Hi3sqwcA99OsNLASPSRvnTXCotbEfsdfwersadasUf4CQfpOv1PQsfiujklhadscjnjkdf+AStW3+MGw==;EndpointSuffix=core.windows.net'

    CONTAINER_NAME='telemetry-event-checkpoint'

    IOT_EVENT_HUB_ENDPOINT='Endpoint=sb://silajndhs.servicebus.windows.net/;SharedAccessKeyName=telemetry-event-listen-policy;SharedAccessKey=m4hsjfhksnjfn/ddskhkjjsd+asdasdAEhGdajNM=;EntityPath=telemetry-event'

    DEFAULT_DEVICE_ID="ajeet-si-labs0011"
```

### Follow these screenshot to get envrionment value

1. Follow this step to get this [ STORAGE_CONNECTION_STRING ]

- Go to storage account
  ![storage account1](backend/readme-assets/storage-account1.jpg)

- Create a new storage account
  ![create-storage1](backend/readme-assets/create-storage1.jpg)

- Click on new created storage account
  ![iot-hub-storage1](backend/readme-assets/iot-hub-storage1.jpg)

- Click on access key and copy connection string
  ![iot-hub-storage2](backend/readme-assets/iot-hub-storage2.jpg)

- Reaplce STORAGE_CONNECTION_STRING value with your copied string in .env file

2. CONTAINER_NAME

- Go to storage account
  ![storage account](backend/readme-assets/storage-account.jpg)

- Create a new storage account
  ![create-storage1](backend/readme-assets/create-storage1.jpg)

- Click on new created storage account
  ![iot-hub-storage1](backend/readme-assets/iot-hub-storage1.jpg)

- Click on containers and create new containers
  ![container2](backend/readme-assets/container2.jpg)

- Copy new containers name
  ![container3](backend/readme-assets/container3.jpg)

- Reaplce CONTAINER_NAME value with your copied string in .env file

2. IOT_EVENT_HUB_ENDPOINT

- Go to IoT Hub
  ![iot-hub1](backend/readme-assets/iot-hub1.jpg)

- Create a new IoT Hub
  ![iot-hub2](backend/readme-assets/iot-hub2.jpg)

- Click on new created IoT Hub and then click on shared access policies and copy
  primary connection string
  ![iot-hub-connection-string](backend/readme-assets/iot-hub-connection-string.jpg)

- Reaplce IOT_EVENT_HUB_ENDPOINT value with your copied string in .env file

3. DEFAULT_DEVICE_ID

- Go to IoT Hub
  ![iot-hub1](backend/readme-assets/iot-hub1.jpg)

- Got device and created new device
  ![create-device1](backend/readme-assets/create-device1.jpg)

- Copy new created deviceId
  ![create-device2](backend/readme-assets/create-device2.jpg)

- Reaplce DEFAULT_DEVICE_ID value with your copied string in .env file

## Run the Application

1. Go to [project-root-folder]/dashboard/backend
2. Open Terminal/Cmd/Poweshell/Bash Here
3. Run this command

```bash
  npm install
```

```bash
# development
$ npm run start

# watch mode
$ npm run start:dev

# production mode
$ npm run start:prod
```

## Test the Application

```bash
# unit tests
$ npm run test

# test coverage
$ npm run test:cov
```

## API Documentation

http://localhost:3005/api/v1/swagger

## Frontend

## Table of Contents

- [Purpose/Scope](#purposescope)
- [Prerequisites/Setup Requirements](#prerequisitessetup-requirements)
  - [Hardware Requirements](#hardware-requirements)
  - [Software Requirements](#software-requirements)
- [Getting Started](#getting-started)
- [Steps to execute application](#steps-to-execute-application)

## Purpose/Scope

This dashboard application demonstrates the chart reprenstation of Temperature, Humidity, Elevation, Accelerometer and Gyroscope reading.It will show latest 10 data points on chart.Also it will contain download feature to download session data and GPX file.

## Prerequisites/Setup Requirements

### Hardware Requirements

- A Windows/Linux/Mac PC

### Software Requirements

- Install Nodejs >= v20.14.0

  - Download the [Node Server](https://nodejs.org/en/download/package-manager).
  - Run the Installer
  - Follow the Setup Wizard to finish installation
  - Run below command to check installed version

    ```c
    node --version
    ```

- Azure App Registration

  - Login to Azure Account with your credentials on [Azure Portal](https://portal.azure.com/)
  - Browse to Home > App registrations and select New registration.
  - Provide necessary details

    - Name of your choice
    - Choose account type as Accounts in this organizational directory only (Single tenant)
    - Redirect URI
      - Select platform as Single-page application (SPA)
      - Redirect Url as (http://localhost:5173)

    ![azure_app_registration](frontend/images/azure-app-registration.png)

  - After providing above details click on Register.
  - Then make a note of the Application (client) ID and Directory (tenant) ID which we will required when setting up
    environment file.

## Getting Started

- Create and configure .env file

  - Go to [project-root-folder]/dashboard/frontend
  - Create .env file
  - Add Application (client) ID and Directory (tenant) ID details on .env file which we get while azure app registration

    ```c
    VITE_CLIENT_ID= "Application (client) ID"
    VITE_TENANT_ID= "Directory (tenant) ID"
    ```

## Steps to execute application

- Go to [project-root-folder]/dashboard/frontend
- Open Terminal/Cmd/Poweshell/Bash Here
- Run below command to install all dependencies
  ```c
  npm install
  ```
- Run below command to start dashboard application
  ```c
  npm run dev
  ```
- After running above commands you can open your chrome browser and type http://localhost:5173/ where you can see login page of our dashboard application.

  ![login_page](frontend/images/login-page.png)

- Click on login button and it will open Microsoft login popup and enter your credentials

  ![login_mfa](frontend/images/login-mfa.png)

- After successful login you will see dashboard page as below where you will see charts for Temperature, Humidity, Elevation, Accelerometer, Gyroscope and Wifi details.

  ![dashboard-1](frontend/images/dashboard-1.png)

  ![dashboard-2](frontend/images/dashboard-2.png)
