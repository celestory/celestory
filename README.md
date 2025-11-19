# Celestory Self-Hosted

This repository contains the configuration and examples for self-hosting the Celestory suite on your own infrastructure.

## Prerequisites

Before you begin, ensure you have the following installed:

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

### License Requirement

> [!IMPORTANT] > **You must have an active Celestory license to use this software.**
> Please contact [Celestory Support](mailto:contact@celestory.io) or visit our [website](https://celestory.io) to obtain a license.

## Installation

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/celestory/celestory.git
    cd celestory
    ```

2.  **Configure Environment Variables:**
    Copy the example environment file to `.env`:

    ```bash
    cp .env.example .env
    ```

    Edit the `.env` file and update the values as needed. You can leave the defaults for a local test setup.

3.  **Start the Services:**
    Run the following command to start the Celestory suite:

    ```bash
    docker compose up -d
    ```

4.  **Access the Application:**
    Once the services are up and running, you can access the Celestory frontend at:
    http://localhost:3000 (or the port you specified in `FRONTEND_PORT`)

    You can access the **Hub (Licensing Manager)** at:
    http://localhost:3001 (or the port you specified in `HUB_PORT`)

## Configuration

The `.env` file controls the configuration of the services. Key variables include:

- `FRONTEND_PORT`: Port for the frontend application (default: 3000).
- `HUB_PORT`: Port for the Hub service (default: 3001).
- `DB_USERNAME`, `DB_PASSWORD`: Database credentials.
- `ADMIN_USERNAME`, `ADMIN_PASSWORD`: Initial admin credentials.

## Services

The stack includes the following services:

- `frontend`: The main user interface.
- `hub`: The central hub for managing projects, connections, and **licensing**. This is the administration page where you can redeem a license and assign seats to users in your organization.
- `api`: The backend API service.
- `generator`: Service for generating content.
- `auth`: Authentication service.
- `db`: PostgreSQL database.

## License

This project is licensed under a custom license requiring an active commercial license. See the [LICENSE](LICENSE) file for details.
