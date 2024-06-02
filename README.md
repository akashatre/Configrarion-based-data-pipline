# Configuration-Based Data Pipeline

## Overview
This project implements a configuration-based data pipeline using AWS Lambda functions. It pulls data from SharePoint, processes it, and integrates it with other data sources. The project leverages DynamoDB for configuration management and AWS Secrets Manager for secure handling of credentials. The core functionality is divided into three main Lambda functions.

## Table of Contents
- [Overview](#overview)
- [Architecture](#architecture)
- [Lambda Functions](#lambda-functions)
- [Setup](#setup)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Architecture
The project follows a 3-layer architecture:
1. **Data Layer**: Interacts with SharePoint to fetch data.
2. **Configuration Layer**: Manages configurations using DynamoDB.
3. **Credential Management Layer**: Uses AWS Secrets Manager to handle credentials securely.

## Lambda Functions
The project consists of three main Lambda functions:

1. **getting_files_from_source**: 
   - Description: This function pulls data from the SharePoint site.
   - Purpose: To retrieve raw data files from the specified SharePoint list.

2. **cleaning_data_process**:
   - Description: This function processes and cleans the fetched data.
   - Purpose: To prepare the raw data for further analysis by cleaning and normalizing it.

3. **converting_data_harmonised**:
   - Description: This function harmonizes and merges the cleaned data with other data sources.
   - Purpose: To create a consolidated dataset ready for use in downstream applications or analytics.

## Setup
### Prerequisites
- AWS account with necessary permissions (Lambda, DynamoDB, Secrets Manager).
- AWS CLI installed and configured.
- Python 3.x installed.
- Access to the SharePoint site from which data will be pulled.

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/akashatre/-Configrarion-based-data-pipline.git
   cd -Configrarion-based-data-pipline
