# Sample openAPI Specification

## Overview
This repository contains the OpenAPI Specification for the **Payment Initiation** and **Retrieve Payment Status** APIs. These APIs are designed to handle the initiation of customer credit transfer payments and to retrieve the status of these payments.

## Table of Contents
- [Introduction](#introduction)
- [API Specification](#api-specification)
- [Endpoints](#endpoints)
- [Authentication](#authentication)
- [Schemas](#schemas)
- [Responses](#responses)
- [Running Locally](#running-locally)
- [License](#license)

## Introduction
This repository provides a detailed OpenAPI 3.0.3 specification for payment-related APIs. The documentation is intended to help developers understand how to interact with the APIs for initiating payments and retrieving their status.

The APIs include the following operations:
- **Initiate Payment**: Allows clients to create new credit transfer payments.
- **Retrieve Payment Status**: Allows clients to retrieve the status of a payment by its ID or get all payment statuses.

## API Specification
The OpenAPI specification can be found in the `openapi.yaml` file in this repository. This file defines the endpoints, request parameters, response formats, authentication methods, and more.

### Key Sections in the Specification:
- **Servers**: Defines different environments (e.g., sandbox, development).
- **Tags**: Organizes the API operations.
- **Security**: Defines various authentication methods supported by the API.
- **Components**: Reusable elements like schemas, parameters, request bodies, and responses.

## Endpoints
### Retrieve All Payments Status
- **GET** `/payment/status`
- Retrieves the status of all payments.

### Retrieve Single Payment Status
- **GET** `/payment/status/{paymentId}`
- Retrieves the status of a specific payment by `paymentId`.

### Initiate Payment
- **POST** `/payment/initiate`
- Initiates a new customer credit transfer payment.

## Authentication
The API supports multiple authentication methods, including:
- **Basic Authentication**
- **Bearer Token**
- **API Key Authentication**
- **OAuth2 Authorization Code Flow**
- **OAuth2 Client Credentials Flow**

Each endpoint may require different authentication mechanisms, as defined in the OpenAPI specification.

## Schemas
The OpenAPI specification defines several schemas for request bodies and responses, including:
- **paymentDetailsSchema**: Contains details about the payment, such as `paymentId`, `amount`, `currency`, and `creationDate`.
- **bankTransferDetailsSchema**: Contains details specific to bank transfers, including `creditorAccount` and `debtorAccount`.
- **walletTransferDetailsSchema**: Contains details specific to wallet transfers, including `walletId` and `walletProvider`.

## Responses
Common responses defined in the API include:
- **200 OK**: The request was successful, and the response contains the requested data.
- **400 Bad Request**: The request failed validation.

## Running Locally
To run and test the APIs locally:
1. Clone the repository.
2. Review the `openapi.yaml` file for API details.
3. Copy API specification to [Swagger UI]([https://swagger.io/tools/swagger-ui/](https://editor.swagger.io/)) to check the API endpoints as per specification.
