# ASI Mercury Gateway Node API

**Arybit Super Intelligence (ASI) — Mercury Platform**

The ASI Mercury Gateway Node API is the controlled application entry point for the Arybit Mercury platform. It provides authenticated application routing and request orchestration between the Mercury user interface and the platform's application services.

The Gateway exposes two principal application namespaces:

- **`/geoaltersense/`** — GeoAlterSense application and geospatial API routing.
- **`/core/`** — CORE application and API routing.

The Gateway is responsible for controlled application access, namespace routing, and coordination of incoming application requests.

It does **not** own or replace the underlying user identity systems, database infrastructure, or geospatial processing workloads. These responsibilities remain within their respective platform services.

## 1. Service URLs

### Production Target

The production Gateway endpoint is:

```text
https://asi-mercury-gateway-node-api.arybit.co.ke/
```

### Local Development

The local development endpoint is:

```text
https://127.0.0.1:8443/
```

The local TLS proxy publishes exactly one listener:

```text
127.0.0.1:8443
```

All local HTTPS application traffic is exposed through this listener.

### Application Namespaces

| Namespace | Responsibility |
|---|---|
| `/geoaltersense/` | GeoAlterSense application and geospatial API routing |
| `/core/` | CORE application and API routing |

Both namespaces are exposed through the Gateway, providing a unified and controlled entry point into the Mercury application environment.

## 2. Architectural Responsibility

The ASI Mercury Gateway Node API operates as an application-layer gateway.

Its responsibilities include:

- Exposing the supported Mercury application namespaces.
- Routing incoming requests to their designated application services.
- Providing a controlled entry point for application traffic.
- Coordinating communication between the Mercury UI and backend application services.
- Supporting secure application access through the platform's authentication and authorization integrations.

The Gateway maintains clear service boundaries and delegates specialized responsibilities to the appropriate backend components.

**Service ownership boundaries:**

- **Identity and Authentication:** Owned by the designated identity and authentication services.
- **Database and Persistence:** Owned by the platform's persistence infrastructure.
- **Geospatial Processing:** Owned by the GeoAlterSense and associated geospatial processing services.
- **Application Routing:** Managed by the ASI Mercury Gateway Node API.

This separation preserves modularity, reduces infrastructure coupling, and allows individual Mercury services to evolve independently.

---

**ASI Mercury Gateway Node API**  
Arybit Super Intelligence (ASI)  
*The controlled application gateway for the Mercury platform.*
