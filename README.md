# Nicklas Vistoft Kleemann

MSc Software Engineering student at Aalborg University CPH, and Associate Software Engineer at NHTA.

I work across RAG and LLM document-extraction systems, full-stack products, and dabble in Linux and systems programming.

## Status

- Education: MSc Computer Software Engineering (2025 to June 2027)
- Role: Associate Software Engineer at NHTA (Aug 2024 to present)
- Focus: RAG frameworks, LLM-driven document extraction, full-stack systems

## Technical Toolbox

| Category | Tools and technologies |
| :--- | :--- |
| Languages | Python, TypeScript, JavaScript, Go, Java, C / C++, OCaml, Dart, SQL, Bash, LaTeX |
| AI, RAG and LLM | LlamaIndex, LlamaParse, PageIndex, Pinecone, Ragas, Langfuse, BM25 and hybrid retrieval, parent-child chunking, Pydantic extraction, OpenAI, Claude, Ollama |
| Backend | FastAPI, Django REST, NestJS, Hono, Express, Node.js, Spring Boot, Azure (Durable) Functions, SSE |
| Frontend | React, React Native, Expo, Flutter, Redux, React Router, Tailwind, NativeWind, Storybook |
| Data and storage | PostgreSQL, MongoDB, MySQL, Redis / Valkey, Prisma, Mongoose, pandas, NumPy, Matplotlib |
| Systems and Linux | Linux, PAM, TPM 2.0, FIDO2 / CTAP2, WebAuthn, USB/IP, systemd, udev, WebAssembly, compiler construction (OCamllex, Menhir) |
| Infra and tooling | Docker, Azure, Cloudflare Workers, Caddy, Prometheus, GitHub Actions, pnpm, Turborepo, Maven, Git |
| Testing | TDD, pytest, Jest, JUnit, OUnit2, CUnit, Go testing |
| Practices | Large-Scale Scrum (LeSS), Agile |

## Selected Projects

### howdy-as-passkey
Virtual FIDO2/CTAP2 authenticator that turns Howdy face recognition into a WebAuthn passkey on Linux, the platform authenticator Linux never had. TPM-sealed vault and in-chip P-256 signing, runs fully unprivileged, IR-liveness gated. Go, USB/IP, TPM 2.0, PAM.

### Kvæk
Grocery price-comparison app running in production. NestJS, Prisma, PostgreSQL, and Valkey backend behind a Caddy and Cloudflare edge, a Cloudflare Worker (Hono) proxying retailer APIs, and an Expo React Native client with live price streaming over SSE. Includes a shopping-list route optimizer (exact subset search with a greedy fallback) and a self-hosted GitHub Actions deploy pipeline.

### AAU Concierge
Modular RAG framework unifying 35+ Aalborg University subdomains. Dual-path hybrid retrieval (Pinecone + BM25), semantic chunking, 97% response integrity measured with Ragas.

### NHTAi Pipeline (Bachelor's)
Serverless extraction pipeline for Danish Medicines Council reports. Azure Durable Functions, LlamaParse, strict Pydantic schemas. Lifted F1 from 0.475 to 0.923 and cut processing time by 84%.

### Numatix
WebAssembly compiler for a custom imperative language, written in OCaml. Full lexer, parser, and code generation.

### Educado
Large-Scale Scrum full-stack platform built across multiple coordinated teams.

## Connect

- LinkedIn: https://www.linkedin.com/in/nicklasvistoftkleemann/
- GitHub: https://github.com/NicklasKleemann
