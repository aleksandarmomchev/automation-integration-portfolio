# Automation & Integration Portfolio

Technical portfolio maintained by Aleksandar Momchev.

This repository presents sanitized documentation from independent technical projects involving workflow automation, API integration, self-hosted infrastructure, market-data processing, WordPress, technical SEO and AI-assisted content operations.

These projects were developed without paid clients or commercial customer deployments.

## Technical Areas

- n8n workflow automation
- REST APIs, webhooks and JSON
- API authentication and validation
- Data transformation and conditional routing
- Error handling and workflow recovery
- Duplicate prevention and idempotency
- Google Sheets as an operational control layer
- Linux and Ubuntu administration
- Docker and Docker Compose
- Nginx and systemd
- Cloudflare Tunnels
- WordPress and WordPress REST API
- Technical SEO and automated publishing
- JavaScript for workflow logic
- Basic Python scripting
- Monitoring and health checks
- Local AI workflow infrastructure
- Market-data processing and alert automation

## Featured Project: AI Tuning

AI Tuning is an independent technical project focused on self-hosted automation, local AI infrastructure, API routing, monitoring and workflow orchestration.

The project demonstrates hands-on work with:

- multiple Linux systems
- Docker-based services
- n8n workflows
- REST APIs and webhooks
- Nginx
- systemd services
- Cloudflare Tunnels
- local language models
- API gateways and routing
- monitoring and health checks
- structured workflow validation
- multi-server orchestration
- technical troubleshooting
- documentation and maintenance

I personally configure, test, troubleshoot, document and maintain the supporting systems.

- Website: https://aituning.io
- GitHub organization: https://github.com/AITuningEU
- Technical overview: [docs/ai-tuning-overview.md](docs/ai-tuning-overview.md)
- Infrastructure overview: [docs/infrastructure-architecture.md](docs/infrastructure-architecture.md)

## Market-Data Project: WaveFibs

WaveFibs is an independent market-data automation and technical-analysis project.

It demonstrates:

- cryptocurrency market-data processing
- structured data ingestion
- multi-timeframe analysis
- indicator-based workflow logic
- dashboard and signal-matrix updates
- automated market summaries
- alert generation and distribution
- data-freshness monitoring
- handling of missing, delayed or unavailable data
- website and Telegram information delivery

WaveFibs provides informational market analysis. It does not execute trades, manage customer funds or provide copy trading.

- Website: https://wavefibs.com
- Technical overview: [docs/wavefibs-overview.md](docs/wavefibs-overview.md)

## WordPress and Content Project: Eat With Rhythm

Eat With Rhythm is an independent WordPress, SEO and content-operations project.

It demonstrates:

- WordPress administration
- website structure and content planning
- technical SEO
- structured content workflows
- WordPress REST API publishing
- Google Sheets workflow control
- automated media generation and processing
- WordPress media uploads
- metadata and alt-text management
- publishing validation
- website operations
- content organisation and maintenance

The article workflow uses structured records for article configuration, SEO, sections, sources, links, media, authorship and validation before WordPress publishing is allowed.

- Website: https://eatwithrhythm.com
- Project overview: [docs/eat-with-rhythm-overview.md](docs/eat-with-rhythm-overview.md)
- Sanitized n8n workflow examples: [docs/n8n-workflow-examples.md](docs/n8n-workflow-examples.md)

## n8n Workflow Example

The portfolio documents a sanitized version of the **EWR Article Pipeline v31 — Deterministic Preflight** workflow.

The workflow includes patterns for:

- selecting one eligible article from a queue
- record locking and execution verification
- reading structured data from multiple Google Sheets tabs
- deterministic pre-write validation
- blocker and warning classification
- canonical article-package construction
- media-generation job preparation
- ComfyUI image generation
- image conversion to WebP
- WordPress REST API media upload
- WordPress media metadata updates
- article assembly and validation
- failure-state recording
- controlled publishing

The complete workflow export is not published because it contains credential references, private infrastructure information, internal addresses and operational configuration.

- Workflow examples: [docs/n8n-workflow-examples.md](docs/n8n-workflow-examples.md)

## Troubleshooting Focus

The portfolio includes sanitized examples involving:

- missing or inconsistent workflow data
- duplicate-record prevention
- idempotency
- API authentication failures
- rate limits and temporary API failures
- Linux and Docker service recovery
- workflow error handling
- monitoring and health checks
- preserving failed records for review
- separating temporary and permanent failures

- Troubleshooting examples: [docs/troubleshooting-examples.md](docs/troubleshooting-examples.md)

## Portfolio Documentation

- [AI Tuning technical overview](docs/ai-tuning-overview.md)
- [Infrastructure architecture](docs/infrastructure-architecture.md)
- [Sanitized n8n workflow examples](docs/n8n-workflow-examples.md)
- [Automation and infrastructure troubleshooting examples](docs/troubleshooting-examples.md)
- [WaveFibs market-data automation overview](docs/wavefibs-overview.md)
- [Eat With Rhythm WordPress and content automation overview](docs/eat-with-rhythm-overview.md)

## Security and Privacy

This public repository does not contain:

- passwords
- API keys
- OAuth tokens
- `.env` files
- credential values
- private IP addresses
- private endpoints
- internal hostnames
- internal server paths
- Google Sheets document identifiers
- personal data
- complete unsanitized workflow exports
- proprietary operational configuration
- customer data

Screenshots, workflow examples and diagrams are sanitized before publication.

## Professional Objective

I am seeking a fully remote junior or associate role involving:

- automation and API integration
- technical support and implementation
- Linux and junior infrastructure
- WordPress and technical SEO
- AI workflow operations
- data and website operations
- workflow troubleshooting and maintenance

I am based in Varna, Bulgaria, available to start immediately and able to work up to 40 hours per week.

## Contact

- GitHub: https://github.com/aleksandarmomchev
- LinkedIn: https://www.linkedin.com/in/aleksandar-momchev-700885144
- AI Tuning: https://aituning.io
- WaveFibs: https://wavefibs.com
- Eat With Rhythm: https://eatwithrhythm.com
