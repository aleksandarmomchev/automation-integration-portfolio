# AI Tuning Infrastructure Architecture

## Overview

AI Tuning is an independent, pre-revenue technical project built around self-hosted automation, local AI services and supporting web infrastructure.

The environment is designed and maintained personally by Aleksandar Momchev.

This public document intentionally excludes private IP addresses, credentials, tokens, internal service URLs and sensitive file paths.

## Architecture Goals

The infrastructure is designed to support:

- workflow automation
- REST API integration
- local AI model services
- service monitoring
- structured validation
- workflow orchestration
- WordPress publishing
- secure external access
- fault isolation
- controlled troubleshooting

## Main Infrastructure Components

### Linux Servers

Multiple Ubuntu Linux systems are used for separate technical responsibilities.

Typical responsibilities include:

- workflow automation
- AI model execution
- web services
- monitoring
- validation
- API routing
- supporting infrastructure

Separating responsibilities helps isolate failures and makes troubleshooting more controlled.

### Docker Services

Docker and Docker Compose are used to run and manage containerised services.

This provides:

- consistent service configuration
- isolated dependencies
- easier service restarts
- repeatable deployment
- clearer log inspection
- controlled service networking

### n8n Automation

n8n is used for workflow automation involving:

- REST APIs
- webhooks
- JSON processing
- conditional routing
- validation
- error handling
- WordPress publishing
- structured data workflows

### Nginx

Nginx is used as a reverse proxy and supporting web-service layer.

Responsibilities may include:

- routing requests to internal services
- handling public web traffic
- forwarding API requests
- supporting secure access
- separating public endpoints from internal services

### Cloudflare Tunnels

Cloudflare Tunnels provide controlled access to selected self-hosted services without directly exposing the local network.

The configuration is designed to avoid publishing internal addresses or unnecessary services.

### systemd Services

systemd is used to manage selected local processes and supporting services.

This allows:

- automatic startup
- controlled restarts
- service-status checks
- log inspection
- dependency management

### Local AI Services

Local AI model services are used for structured workflow tasks such as:

- content processing
- classification
- validation
- routing
- structured output generation
- workflow assistance

### Monitoring and Health Checks

Monitoring is used to confirm whether important services are available and responding correctly.

Checks may include:

- service status
- container status
- HTTP health endpoints
- API response validation
- workflow execution results
- log inspection

## Request Flow

A simplified request flow may look like this:

1. An external request reaches a controlled public endpoint.
2. Nginx or a tunnel routes the request to the appropriate internal service.
3. n8n receives or processes the request.
4. The workflow validates and transforms the data.
5. The workflow may call an API, local AI service or WordPress.
6. Results are checked before being stored, published or returned.
7. Errors are routed to a separate troubleshooting or review path.

## Reliability Approach

The infrastructure uses several reliability principles:

- separate services by responsibility
- use health checks
- inspect logs before restarting services
- restart only the affected service where possible
- validate workflow inputs and outputs
- preserve failed data for review
- limit retries
- distinguish temporary failures from permanent errors
- document configuration and corrective actions

## Personal Contribution

All infrastructure work is performed personally, including:

- Linux configuration
- Docker service deployment
- n8n setup
- Nginx configuration
- systemd service management
- Cloudflare Tunnel configuration
- workflow design
- monitoring
- troubleshooting
- documentation
- maintenance

## Security and Privacy

This public architecture overview does not include:

- passwords
- API keys
- OAuth tokens
- `.env` contents
- private IP addresses
- internal hostnames
- access credentials
- private service URLs
- sensitive server paths
- complete production configuration
