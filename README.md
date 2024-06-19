# Dashboard Application

## Table of Contents

- [Purpose/Scope](#purposescope)
- [Prerequisites/Setup Requirements](#prerequisitessetup-requirements)
  - [Software Requirements](#software-requirements)
- [Getting Started](#getting-started)
- [Application Build Environment](#application-build-environment)
- [Test the Application](#test-the-application)
- [Steps to execute application](#follow-the-steps-below-for-successful-execution-of-the-application)
- [Appendix](#appendix)
- [Documentation](#documentation)

## Purpose/Scope

This dashboard application demonstrates the chart reprenstation of Temperature, Humidity, Elevation, Accelerometer and Gyroscope reading.It will show latest 10 data points on chart.Also it will contain download feature to download session data and GPX file.

## Prerequisites/Setup Requirements

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
    - Provide necessary details (Name, choose single/multi-tenant), set redirect uri-
      ![alt text](https://learn.microsoft.com/en-us/entra/identity-platform/media/quickstart-register-app/portal-02-app-reg-01.png#lightbox)



