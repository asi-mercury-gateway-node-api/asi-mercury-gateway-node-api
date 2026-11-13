# ASI Mercury Gateway Node API

**Arybit Super Intelligence (ASI) — Mercury Platform**

The ASI Mercury Gateway Node API is the central application gateway for Arybit Mercury. It provides authenticated routing, request orchestration, and integration between the Mercury user interface and backend services, including authentication, geospatial processing, and persistence.

## Overview

The gateway serves as the primary API entry point for the Mercury platform, coordinating communication between platform components while maintaining consistent authentication, authorization, and service access patterns.

## Core Responsibilities

- **API Gateway:** Centralized entry point for Mercury application requests.
- **Authentication:** Integration with identity and authentication services.
- **Request Orchestration:** Coordinates communication between backend services.
- **Geospatial Integration:** Routes requests to geospatial processing services.
- **Persistence Integration:** Coordinates access to platform data and persistence services.
- **Security:** Provides a structured boundary for authenticated service communication.

## Architecture

```text
                 MERCURY UI
                      |
                      v
          ASI MERCURY GATEWAY NODE API
                      |
          +-----------+-----------+
          |           |           |
          v           v           v
     AUTH SERVICE  GEO SERVICE  PERSISTENCE
          |           |           |
          +-----------+-----------+
                      |
                      v
               MERCURY PLATFORM
```

## Technology

The gateway is designed around a Node.js API architecture.

Core technology and implementation details should be documented as the project evolves.

## Getting Started

### Prerequisites

- Node.js (LTS recommended)
- npm
- Git

### Clone the Repository

```bash
git clone https://github.com/asi-mercury-gateway-node-api.git
cd asi-mercury-gateway-node-api
```

### Install Dependencies

```bash
npm install
```

### Environment Configuration

Create a `.env` file in the project root.

```env
NODE_ENV=development
PORT=3000

# Authentication service
AUTH_SERVICE_URL=

# Geospatial service
GEO_SERVICE_URL=

# Persistence service
PERSISTENCE_SERVICE_URL=

# Security configuration
JWT_SECRET=
```

Never commit secrets, credentials, or production environment variables to version control.

### Run the Application

The execution command depends on the scripts configured in `package.json`.

Typical development command:

```bash
npm run dev
```

Typical production command:

```bash
npm start
```

## API Documentation

API endpoints and request/response contracts will be documented here as they are implemented.

Recommended documentation sections:

- Authentication endpoints
- Gateway routing endpoints
- Geospatial service endpoints
- Persistence endpoints
- Health and readiness endpoints

## Security

Security is a core responsibility of the gateway.

Implementation guidelines:

- Enforce authentication on protected routes.
- Apply authorization checks where required.
- Validate incoming requests.
- Protect sensitive environment variables.
- Use HTTPS in production.
- Implement appropriate rate limiting.
- Avoid exposing internal service credentials.
- Maintain structured security and application logs.

## Development Guidelines

- Keep service integrations modular.
- Maintain consistent API response structures.
- Validate request payloads.
- Document new endpoints.
- Include tests for critical gateway functionality.
- Keep dependencies updated.

## Project Status

**Development:** Active project development.

Features, integrations, and API contracts are subject to implementation and revision.

## License

License information will be added when the project's distribution and licensing model is finalized.

---

**ASI Mercury Gateway Node API**  
*Arybit Super Intelligence (ASI)*  
*Powering the Mercury platform through secure, orchestrated service connectivity.*
