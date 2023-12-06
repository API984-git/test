sdfdfscall monitor
zdcdc
hftht
o;;p
gui
# MuleSoft Salesforce System API Project README

Welcome to the MuleSoft Salesforce System API Project! This README provides essential information to help you set up and understand the integration with Salesforce using MuleSoft.

## Overview

This MuleSoft project is designed to interact with the Salesforce System API, providing seamless integration with Salesforce CRM. The project includes flows and configurations to perform common Salesforce operations like retrieving records, creating new records, and updating existing ones.

## Table of Contents

1. [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)
2. [Configuration](#configuration)
    - [Salesforce Connection](#salesforce-connection)
    - [Environment Properties](#environment-properties)
3. [Usage](#usage)
    - [Executes A Salesforce Query](#executes-a-salesforce-query)
    - [Create/Update Salesforce Object](#create/Update-salesforce-object)
    - [Delete Salesforce Object]
    - [Calls An Apex Service]
    - [Calls Salesforce Composite API]
4. [Error Handling](#error-handling)
5. [Logging](#logging)
6. [API Collection](#api-collection)
7. [Contributing](#contributing)
8. [License](#license)

## Getting Started

### Prerequisites

Before using this MuleSoft project, ensure you have:

- MuleSoft Anypoint Studio installed.
- A Salesforce Developer account with API access.
- Salesforce Security Token (for authentication).

### Installation

1. Clone the project repository:

   ```bash
   git clone https://github.com/yourusername/mulesoft-salesforce-system-api.git
   ```

2. Import the project into Anypoint Studio.

3. Configure the Salesforce connection and environment properties (details below).

## Configuration

### Salesforce Connection

Configure the Salesforce connection in the `src/main/resources/properties/{env}.yaml` file. Replace `YOUR_SALESFORCE_USERNAME`, `YOUR_SALESFORCE_PASSWORD`,`YOUR_SECURITY_TOKEN`,`YOUR_CONSUMER_KEY` and `YOUR_CONSUMER_SECRET` with your encrypted Salesforce credentials.

```yaml
sf:
  username: "![YOUR_SALESFORCE_USERNAME]"
  password: "![YOUR_SALESFORCE_PASSWORD]"
  token: "![YOUR_SECURITY_TOKEN]"
  consumerKey: "![YOUR_CONSUMER_KEY]"
  consumerSecret: "![YOUR_CONSUMER_SECRET]" 
```

### Environment Properties

Adjust the environment properties in the `src/main/resources/properties/{env}.yaml` file as needed where `env` is either of local, qa, uat or prod.

## Usage

Please refer to Exchange for [API Contract](https://anypoint.mulesoft.com/exchange/f015bd3e-6860-45a2-8012-1af3eec6fdba/medspeed-salesforce-sapi/)

### Executes A Salesforce Query

> Endpoint: **POST /query** <br/>
> Functionality: Executes and return the SOQL query response

### Create/Update Salesforce Object

> Endpoint: **PUT /object** <br/>
> Functionality:  Updates a salesforce object if exists, otherwise creates a new one

### Delete Salesforce Object

> Endpoint: **DELETE /object** <br/>
> Functionality:  Deletes a salesforce object

### Calls An Apex Service

> Endpoint: **POST /apex** <br/>
> Functionality: Makes a call to salesforce apex service

### Calls Salesforce Composite API

> Endpoint: **POST /composite** <br/>
> Functionality:  Makes a call to composite API of salesforce

## Error Handling

The project includes error handling mechanisms to gracefully handle Salesforce API errors. Refer to the exception strategies in the flows for details.

## Logging

Logging is configured to provide visibility into the flow execution. Check the logs in Anypoint Studio or the deployed application for troubleshooting.

## API Collection 

Please refer the below API collection link to explore the endpoint(s) in real time.
<br/><br/>
[<img src="https://run.pstmn.io/button.svg" alt="Run In Postman" style="width: 128px; height: 32px;">](https://medspeed-mulesoft-testing.postman.co/collection/30441089-bb32bc02-1fd2-4d70-b8d5-f495af42af2d?source=rip_markdown&env=30441089-3b44484d-94fc-48a1-bb17-fb3504d13cbf)

## Contributing

We welcome contributions! If you find a bug or have a feature request, please open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
