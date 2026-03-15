# Agentic Cold Chain Compliance Engine Usage Guide

## Introduction
The Agentic Cold Chain Compliance Engine is a robust solution designed to ensure compliance with pharmaceutical cold chain regulations. This guide provides a step-by-step overview of how to use the engine effectively.

## Prerequisites
Before using the Agentic Cold Chain Compliance Engine, ensure you have the following:
* Docker installed on your system
* Access to the pharma-cold-chain-compliance repository

## Running the Engine
To run the engine, follow these steps:
1. Clone the repository: `git clone https://github.com/your-username/pharma-cold-chain-compliance.git`
2. Navigate to the repository directory: `cd pharma-cold-chain-compliance`
3. Build the Docker image: `docker build -t agentic-cold-chain-compliance .`
4. Run the Docker container: `docker run -p 8080:8080 agentic-cold-chain-compliance`

## API Endpoints
The engine provides the following API endpoints:
* `POST /api/validate`: Validate a cold chain shipment against regulatory requirements
* `GET /api/status`: Retrieve the status of a cold chain shipment

## Example Use Cases
### Validating a Cold Chain Shipment
To validate a cold chain shipment, send a `POST` request to the `/api/validate` endpoint with the shipment details in the request body:
```json
{
    "shipment_id": "SHIP-123",
    "temperature_range": "2-8°C",
    "shipment_date": "2022-01-01"
}
```
### Retrieving Shipment Status
To retrieve the status of a cold chain shipment, send a `GET` request to the `/api/status` endpoint with the shipment ID as a query parameter:
```bash
curl -X GET 'http://localhost:8080/api/status?shipment_id=SHIP-123'
```

## Troubleshooting
For troubleshooting guides and FAQs, please refer to the [troubleshooting guide](troubleshooting.md).

## Contributing
To contribute to the Agentic Cold Chain Compliance Engine, please submit a pull request to the [pharma-cold-chain-compliance repository](https://github.com/your-username/pharma-cold-chain-compliance.git).