# Moumen Qasiim

**Backend & Systems Engineer** · Working remote · Building things that don't break under load.

I write software for the hard parts — concurrency, auth boundaries, distributed state, protocols, server infrastructure, and getting real AI systems to behave reliably in production. Not here for hype or surface polish; I enjoy the grind of taking ugly, fragile systems and making them solid. I use AI tools for leverage, and I actually read, review, and verify the code that ships.

---

### What I Do

- **Architecture & Code Review:** Designing and refactoring systems using **Clean Architecture**, **Layered Architecture**, and **Modular Monoliths** (`.NET`, `FastAPI`, `NestJS`) — enforcing strict layer boundaries, reviewing code for correctness, security, and failure modes, and decomposing legacy monoliths without breaking live traffic.
- **Servers & Full Infrastructure:** Taking raw rented servers from a blank OS to full production environments — Docker / Compose stacks, Nginx / Traefik reverse proxies, TLS, PostgreSQL & Redis operations, SSH/network hardening, automated migrations, readiness checks, and CI/CD pipelines.
- **Data, Vectors & Applied AI:** PostgreSQL schema design, optimistic concurrency, tenant isolation, transactional outbox/inbox pipelines, **vector search & embeddings** (`pgvector`, RAG ingestion/retrieval), and multi-provider LLM gateways with structured outputs and strict data boundaries.
- **Systems & Tooling:** Linux automation, background daemons/workers, and operational guardrails.

---

### Core Stack

| Area | Tools |
|---|---|
| **Backend & Architecture** | C# / .NET (`ASP.NET Core`, `EF Core`, `SignalR`, `Hangfire`, Clean / Layered / Modular Monolith, CQRS), Python (`FastAPI`, `SQLAlchemy`, `Alembic`), TypeScript / JavaScript (`NestJS`, `Node.js`) |
| **Data, Vectors & Messaging** | PostgreSQL (`pgvector`), Vector Embeddings & Similarity Search, Redis, SQL Server, RabbitMQ, S3 / MinIO |
| **Testing & Quality** | `xUnit`, `Testcontainers`, `NetArchTest`, `pytest` |
| **Servers & Infra** | VPS Provisioning & Full-Stack Deployment, Docker / Compose, Nginx, Traefik, GitHub Actions, Linux (`systemd`, SSH, `iptables`) |
| **Frontend (when shipping end-to-end)** | TypeScript, JavaScript, React, Next.js |

---

<details>
<summary><strong>Full technical &amp; systems skill breakdown</strong> (click to expand)</summary>

#### Languages
C# (`.NET 10`), Python (`3.11+`), TypeScript, JavaScript, SQL, Bash / Shell, HTML / CSS

#### Backend Frameworks & Architecture
- **.NET:** ASP.NET Core (Minimal APIs & Controllers), EF Core 10, .NET Aspire (`AppHost` / `ServiceDefaults`), Central Package Management (`Directory.Packages.props`), strict Roslyn analyzer enforcement (`TreatWarningsAsErrors`)
- **Python:** FastAPI, SQLAlchemy 2.0, Alembic, Pydantic / `pydantic-settings`, Uvicorn / Gunicorn
- **Node.js / TypeScript:** NestJS (`@nestjs/core`, `@nestjs/common`), Express
- **Patterns:** Clean Architecture, Layered Architecture, Modular Monoliths, Vertical Slice Architecture, custom CQRS Mediator & `FluentValidation` pipeline behaviors, Specification pattern, Domain Events, `Result` pattern, RFC 7807 `ProblemDetails`, Transactional Outbox / Inbox (`ExecuteUpdateAsync` claim leasing), Strangler-Fig legacy migrations

#### Databases, Vectors & Caching
- **Relational:** PostgreSQL (`Npgsql`, `psycopg`), SQL Server, SQLite
- **Vectors & Search:** `pgvector` cosine similarity search, embeddings ingestion & retrieval pipelines, text/markdown chunking, RAG pipelines (`Microsoft.Extensions.AI` + Ollama, Python `pgvector`)
- **Caching & Multi-Tenancy:** Redis (rate limiting, per-user/IP auth lockouts, distributed cache), `Finbuckle.MultiTenant`, `ContextVar` tenant scoping, dynamic EF Core expression-tree global query filters (soft-delete & tenant isolation), optimistic concurrency (`RowVersion` conflict retries), bulk seeding

#### Servers, VPS Infrastructure & DevOps
- **Server Provisioning & Operations:** Setting up raw rented Linux VPS servers from scratch, SSH hardening, `systemd` service daemons, `iptables` container network isolation
- **Containers & Proxies:** Docker, multi-service Docker Compose stacks, Nginx, Traefik, TLS/reverse proxy routing, automated health & readiness polling scripts
- **CI/CD & Observability:** GitHub Actions (selective multi-service builds, migration & preflight gating, automated PR workflows), Makefiles, Serilog, OpenTelemetry, structured JSON logging, `MailKit` / templated SMTP pipelines
- **Messaging & Object Storage:** Hangfire, RabbitMQ, S3 / MinIO (`boto3`, `@aws-sdk/client-s3`)

#### Applied AI & Document / Domain Processing
- **LLM Infrastructure:** In-process multi-provider AI gateways (`google-genai`, OpenAI-compatible, RunPod serverless vLLM), model fallbacks, retries, circuit breakers, structured JSON schema outputs, multi-turn tool calling
- **Data Guardrails & Tooling:** Sensitive-data / PII scrubbing & tokenization pipelines, fail-closed provider & tenant resolution, MCP servers (`fastmcp`, `mcp`), survival/statistical analytics (`lifelines`, `scikit-learn`), CAD & document pipelines (`ezdxf`, `ezdwg`, `pypdf`, `python-docx`, `reportlab`)

#### Real-Time, Streaming & Low-Level I/O
- **SignalR & Protocols:** Server-to-client `IAsyncEnumerable`, client-to-server `ChannelReader<T>`, custom binary `IHubProtocol` over `MessagePackHubProtocol`
- **Memory & Zero-Alloc Primitives:** `Span<byte>`, `ArrayPool<byte>`, `IBufferWriter<byte>`, `ReadOnlySequence<byte>`, `BinaryPrimitives`
- **SSE & Browser Workers:** `fetch` `ReadableStream` SSE parsing, cross-tab `SharedWorker` stream persistence

#### Auth, Security & Code Review
- **AuthN / AuthZ:** JWT (`PyJWT`, `JwtBearer`, `jsonwebtoken`), Cookie Auth, OAuth 2.0 & SSO, TOTP MFA (`pyotp`), break-glass recovery flows, HMAC-signed session tokens, constant-time comparisons
- **Crypto & Hardening:** `argon2-cffi`, `bcrypt`, `AesGcm`, `HKDF`, `CryptographicOperations.ZeroMemory`, RBAC permission factories, security headers & request body-size middleware
- **Code Review & Engineering Standards:** Auditing PRs for auth bypasses, tenant leaks, concurrency bugs, and failure modes; architecture boundary tests; ADRs, Diátaxis docs, and operational runbooks

#### Linux Systems & Hardware Tooling
- Reading kernel `sysfs` / `hwmon` CPU & GPU thermal/frequency telemetry, CPU boost thermal hysteresis controllers, `systemd` background watchdogs
- Linux CLI / TUI tooling (`pacman` package/desktop entry indexing with `mtime` caching, Flatpak/AppImage management, Hyprland display management scripts)

#### Testing & Frontend (End-to-End Delivery)
- **Testing:** `xUnit`, `FluentAssertions`, `NSubstitute`, `NetArchTest`, `WebApplicationFactory`, `Testcontainers.PostgreSql`, `Respawn`, `pytest`, `pytest-asyncio`, Starlette `TestClient`, `node --test` / `tsx`, React Testing Library, `jsdom`
- **Frontend:** React (`18` / `19`), Next.js `16`, TypeScript, JavaScript, Vite, `@tanstack/react-query`, Tailwind CSS, RTL & multi-locale i18n

</details>

---

> Most of my production and client work lives in private repositories.
