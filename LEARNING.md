# LEARNING.md

## Project Overview
This project is a **local infrastructure setup for n8n** (a workflow automation tool) using **Docker Compose**. It integrates **ngrok** to create a secure tunnel, exposing the local n8n instance to the public internet. This architecture allows the local n8n instance to receive external webhooks, simulating a production-like environment for development and testing of automation workflows without the need for a cloud VPS.

## Tech Stack and Key Technologies
- **Containerization & Orchestration**: Docker, Docker Compose
- **Automation Platform**: n8n (Workflow Automation)
- **Networking & Tunneling**: ngrok (Secure Tunneling)
- **Configuration**: YAML (Docker Compose, ngrok config), Bash (Environment setup)
- **OS/Environment**: Linux/Unix-based containers (Alpine/Debian based images)

## Notable Libraries & Images
- **`n8nio/n8n:latest`**: The core workflow automation engine. It solves the problem of integrating disparate services (APIs, databases, etc.) into cohesive workflows.
- **`ngrok/ngrok:latest`**: Provides a secure tunnel to localhost. It solves the problem of exposing a local server behind a NAT/firewall to the public internet, which is critical for testing webhooks.

## Major Achievements and Skills Demonstrated
- **Infrastructure Orchestration**: Designed and implemented a `docker-compose.yml` file to orchestrate multi-container services (n8n and ngrok) with dependency management (`depends_on`).
- **Secure Local Exposure**: Integrated ngrok to securely expose a local web service to the internet using a static domain, enabling real-time webhook testing.
- **Network Configuration**: Configured a private Docker bridge network (`n8n-network`) to ensure secure and direct communication between the automation engine and the tunneling service.
- **Data Persistence**: Implemented Docker volumes (`n8n_data`) to ensure workflow data and user credentials persist across container restarts and updates.
- **Environment Management**: Utilized `.env` files to manage sensitive configuration (API keys, auth tokens) and environment-specific variables (Timezones, URLs), adhering to 12-Factor App principles.

## Skills Gained/Reinforced
- **Docker & Docker Compose**: Deepened understanding of container lifecycles, networking, and volume management.
- **DevOps & Infrastructure as Code (IaC)**: Practical experience in defining infrastructure using declarative configuration files.
- **Networking**: Understanding of tunneling, reverse proxies, and container-to-container communication.
- **Workflow Automation**: Setting up and maintaining the environment for complex automation logic.
- **System Administration**: Managing local server environments and service dependencies.
