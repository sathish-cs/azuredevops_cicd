# HelloWorld Python App

## Overview

This is a simple Python web application built using Flask. It deploy the code to Azure App Service and triggers the pipeline autmatically when changes pushed to the repo.


## Requirements

- Python 3.11+
- Flask (installed via `requirements.txt`)
- Azure DevOps Pipeline setup using YAML
- Azure App Service 

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/sathish-cs/azuredevops_cicd.git
    cd azuredevops_cicd
    ```

2. Create a virtual environment and install dependencies:

    ```bash
    python -m venv venv
    source venv/bin/activate  
    pip install -r requirements.txt
    ```

3. Run the application:

    ```bash
    python app.py
    ```

4. Access the app at:

    ```bash
    http://127.0.0.1:5000/
    ```

## Azure DevOps Pipeline (CI/CD)

This project includes an Azure DevOps YAML pipeline for automating deployment to Azure App Service.

### Pipeline Stages

#### 1. Build

- Installs dependencies.
- Packages the application as a ZIP file.
- Publishes the artifact for deployment.

#### 2. Deploy

Downloads the artifact.

Deploys the application to Azure App Service.
