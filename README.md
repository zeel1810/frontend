# Dashboard Application

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
-  Install Nodejs >= v20.14.0
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
            - Select platform as  Single-page application (SPA)
            - Redirect Url as (http://localhost:5173)
      
      ![azure_app_registration](images/azure-app-registration.png)

     - After providing above details click on Register.
     - Then make a note of the Application (client) ID and Directory (tenant) ID  which we will required when setting up 
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

    ![login_page](images/login-page.png)

  - Click on login button and it will open Microsoft login popup, enter your     credentials

    ![login_mfa](images/login-mfa.png)
  
  - After successful login you will see dashboard page as below where you will see charts for Temperature, Humidity, Elevation ,Satellites, Accelerometer, Gyroscope and Wifi details.

    ![dashboard-1](images/dashboard-1.png)

    ![dashboard-2](images/dashboard-2.png)





 
