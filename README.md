<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://news.silabs.com/download/silicon-labs-logo-red-2014-1538x769px_1.jpg" width="200" alt="Nest Logo" /></a>
</p>

  <p align="center">Si labs project</p>

## Description

This ReadMe file demonstrate steps to set up backend and frontend to run the dashboard application.

### Table of Contents

- [Purpose/Scope](#purposescope)
- [Prerequisites](#prerequisites)
  - [Hardware Requirements](#hardware-requirements)
  - [Software Requirements](#software-requirements)
  - [Azure Cloud Configuration](#azure-cloud-configuration)
  - [Azure App Registration](#azure-app-registration)
- [Getting Started](#getting-started)
- [Getting Started Dashboard](#dashboard)
- [Run the Application](#run-the-application)
- [Test the Application](#test-the-application)
- [API Documentation](#api-documentation)

## Purpose/Scope

This application demonstrates how to configure the Azure device with iot hub and how to receive all the device sensor message on backend node server and display this on client side.
Also it demonstrates the chart reprenstation of Temperature, Humidity, Elevation, Accelerometer and Gyroscope reading.It will show latest 10 data points on chart.Also it will contain download feature to download session data and GPX file.

## Prerequisites

### Hardware Requirements

- A Windows/Linux/Mac PC
- System config
  - Processor:- 1 GHZ or faster, 32 bit or 64 bit processor.
- Active Internet connection

### Software Requirements

- Install Nodejs >= v20.14.0 LTS
  - Install [Nodejs](#hardware-requirements)
- Install MongoDB >= 7.0 LTS
  - Install [MongoDB](#hardware-requirements)

### Azure Cloud Configuration

> **Note:**
>
> - Please follow the azure cloud readme to setup cloud configuration
> - Path of this readme file is [root-folder]/azure_cloud/README_CLOUD.md

### Azure App Registration


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

### Replace these environment variable With your actual value in backend .env file

**Note:**

- Refer Azure cloud readme to know all the steps to get these ENV values
- Path of the Azure readme is [root-folder]/azure_cloud/README_CLOUD.md

**Note:**

- Path of the backend .env is
  [root-folder]/dashboard/backend/.env
- keep all the other env file as it it, update only these variables

```bash
  STORAGE_CONNECTION_STRING='DefaultEndpointsProtocol=https;AccountName=sa1sasyd;AccountKey=rn3fsfwfvfdQs2Hi3sqwcA99OsNLASPSRvnTXCotbEfsdfwersadasUf4CQfpOv1PQsfiujklhadscjnjkdf+AStW3+MGw==;EndpointSuffix=core.windows.net'

  CONTAINER_NAME='telemetry-event-checkpoint'

  IOT_EVENT_HUB_ENDPOINT='Endpoint=sb://silajndhs.servicebus.windows.net/;SharedAccessKeyName=telemetry-event-listen-policy;SharedAccessKey=m4hsjfhksnjfn/ddskhkjjsd+asdasdAEhGdajNM=;EntityPath=telemetry-event'

  DEFAULT_DEVICE_ID="ajeet-si-labs0011"
```

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

## Getting Started_Dashboard

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
  ```
    npm install
  ```
- Run below command to start dashboard application
  ```
   npm run dev
  ```
- After running above commands you can open your chrome browser and type http://localhost:5173/ where you can see login page of our dashboard application.

  ![login_page](frontend/images/login-page.png)

- Click on login button and it will open Microsoft login popup and enter your credentials

  ![login_mfa](frontend/images/login-mfa.png)

- After successful login you will see dashboard page as below where you will see charts for Temperature, Humidity, Elevation, Accelerometer, Gyroscope and Wifi details.

  ![dashboard-1](frontend/images/dashboard-1.png)

  ![dashboard-2](frontend/images/dashboard-2.png)
