# Nicklas Vistoft Kleemann

> MSc Software Engineering @ Aalborg University CPH  ·  Associate Software Engineer @ NHTA

I build LLM document-extraction pipelines and the systems around them: crawlers that feed them, data platforms and cloud infrastructure that run them, and apps that put the results in front of people. On the side I write Linux tooling, mostly around authentication and browser automation.

---

## Status

- **Education:** MSc Computer Software Engineering (2025 to June 2027), now on the thesis
- **Role:** Associate Software Engineer at NHTA (Aug 2024 to present), building Qori with Quantitative, a joint venture between NHTA and IT Minds
- **Working on:** agentic extraction from EU regulatory dossiers (thesis), Qori (work), burrow-browser (side project)

---

## Technical Toolbox

| Category | Tools and technologies |
| :--- | :--- |
| Languages | Python, TypeScript, JavaScript, Go, Java, C / C++, OCaml, Dart, SQL, Bash, HCL, LaTeX, Processing |
| LLM and agents | OpenAI, Anthropic, Gemini, LiteLLM, Ollama, vLLM, Hugging Face Transformers, sentence-transformers, LangChain, LlamaIndex, Pydantic AI, PageIndex, tool-calling agents, MCP servers |
| Document extraction | LlamaParse, Docling, PyMuPDF, pymupdf4llm, Pydantic schemas with source traceability, json-repair |
| Retrieval and search | Pinecone, BM25 and hybrid retrieval, parent-child chunking, Typesense, Algolia, rapidfuzz, entity resolution |
| LLM evaluation and observability | Ragas, extract-bench, Langfuse, OpenTelemetry / OpenInference |
| Scraping and browsers | Scrapy, Playwright, Camoufox, Scrapling, crawl4ai, Firecrawl, curl_cffi, BeautifulSoup, Cheerio |
| Data engineering | Dagster (medallion pipelines), PyIceberg lakehouse, SeaweedFS (S3), pandas, NumPy, Matplotlib, Plotly |
| Backend | FastAPI, Django REST, Flask, NestJS, Express, Hono, Spring Boot (Security, JPA), Azure (Durable) Functions, SSE, cron and event-driven jobs, circuit breakers, JWT / OAuth (Apple, Google, MSAL) |
| Frontend and mobile | React, Next.js, Vite, React Native, Expo, Flutter, Redux Toolkit, Zustand, TanStack Query, Mantine, shadcn/ui, Tailwind, NativeWind, MapLibre, Leaflet, Skia, Storybook, Astro, SolidJS, JavaFX |
| Data and storage | PostgreSQL, TiDB, MongoDB, MySQL, SQLite, Redis / Valkey, Prisma, Mongoose, SQLAlchemy, Alembic, Azure Blob / Table / Queue Storage, Google Cloud Storage |
| ML | PyTorch, TensorFlow / Keras, scikit-learn, statsmodels, gensim, NLTK; regression, feed-forward and recurrent nets for NER |
| Systems and Linux | PAM, TPM 2.0, FIDO2 / CTAP2, WebAuthn, USB/IP, D-Bus, bubblewrap sandboxing, systemd, udev, firewalld, WebAssembly, compiler construction (OCamllex, Menhir) |
| Infra and ops | Docker, Terraform (azurerm, azapi), Azure (Functions, Container Apps, Web Apps, Static Web Apps, PostgreSQL Flexible Server, DNS), Cloudflare Workers, Vercel, Caddy, nginx, Azurite, Sentry, Prometheus, GitHub Actions (staging/prod pipelines, self-hosted runners) |
| Tooling | uv, Ruff, pnpm, Turborepo, Biome, Maven, Git |
| Testing | TDD, pytest, Hypothesis, Testcontainers, Vitest (browser mode), Jest, Supertest, Cypress, JUnit, OUnit2, CUnit, Go testing |
| Practices | Large-Scale Scrum (LeSS), Agile, Jira, Confluence, Lean Startup |

---

## Selected Projects

### EFSA Data Extraction (MSc thesis)
Extraction pipeline that turns EFSA pesticide assessment PDFs into OECD OFT3 / IUCLID-shaped records. Source adapters fetch the conclusion and its supporting files (Wiley, Europe PMC), converters produce per-page markdown, and the model finds evidence either by walking a PageIndex heading tree or by running grep in a bubblewrap/Docker sandbox. Every row keeps a citation to the page it came from. Provider-agnostic (OpenAI, Anthropic, Gemini via LiteLLM), with a shared TiDB store so runs and gold files can be compared across the team.
**Stack:** Python · Pydantic · LiteLLM · PageIndex · bubblewrap · TiDB · PostgreSQL

### Qori (work, NHTA and Quantitative)
Nordic health technology assessment intelligence platform covering Denmark, Sweden and Norway. It started as NHTAi on Django REST, was rebuilt as serverless Azure Function Apps, and now runs a FastAPI backend with a React frontend. I built most of the Azure Durable Functions PDF processor that extracts Danish Medicines Council reports into strict Pydantic schemas with source traceability (my bachelor's project lifted F1 from 0.475 to 0.923 and cut processing time by 84%), the HTA scrapers and Nordic source crawlers, and the staging/production deploy pipeline. Crawled sources feed a Dagster medallion pipeline on an Iceberg lakehouse, with Typesense search and Terraform-managed Azure Container Apps.
**Stack:** Django REST → Azure Durable Functions → FastAPI · LlamaParse · Pydantic · Pinecone · Scrapy · Dagster · React · Terraform

### [burrow-browser](https://github.com/NicklasKleemann/burrow-browser)
MCP server that gives AI agents a real headless browser. Agents can read JavaScript-heavy pages, drive forms, inspect network traffic and HAR recordings, mock API failures, and audit a site's headers, CORS, TLS and leaked keys.
**Stack:** Python · MCP · Camoufox · Playwright

### [howdy-as-passkey](https://github.com/NicklasKleemann/howdy-as-passkey)
Virtual FIDO2/CTAP2 authenticator that turns Howdy face recognition into a WebAuthn passkey on Linux, the platform authenticator Linux never had. TPM-sealed vault and in-chip P-256 signing, runs fully unprivileged, IR-liveness gated.
**Stack:** Go · USB/IP · TPM 2.0 · PAM

### Kvæk
Grocery price-comparison app running in production. NestJS backend with a mobile client in Expo React Native, live price updates, price alerts with push notifications, product search, and a shopping-list optimizer that finds the cheapest way to shop a list.
**Stack:** NestJS · Prisma · PostgreSQL · Valkey · Typesense · Cloudflare Workers · Expo · Next.js

### [AAU Concierge](https://github.com/SW7-AAU-Concierge-Project)
Modular RAG framework unifying 35+ Aalborg University subdomains. Dual-path hybrid retrieval (Pinecone + BM25), semantic chunking, local models served through Ollama and vLLM, 97% response integrity measured with Ragas.
**Stack:** FastAPI · LangChain · Pinecone · BM25 · Ollama · vLLM · Ragas

### [Numatix](https://github.com/SW4-GR1/Numatix)
WebAssembly compiler for a custom imperative language, written in OCaml. Full lexer, parser, and code generation.
**Stack:** OCaml · OCamllex · Menhir · WebAssembly

### [Educado](https://github.com/ErasmusEgalitarian/educado-frontend)
Joined an existing Large-Scale Scrum platform for one semester. I built the course manager in the content-creator web app and the media upload routes in the backend.
**Stack:** React · TypeScript · Express · MongoDB · Google Cloud Storage · LeSS

### Timetracking (3rd semester)
Time-tracking web app with a Spring Boot backend, Spring Security JWT auth, JPA on MySQL, and a React and Redux Toolkit frontend deployed to Azure Web Apps.
**Stack:** Spring Boot · MySQL · React · Redux Toolkit · Azure

---

## Connect

- LinkedIn: https://www.linkedin.com/in/nicklasvistoftkleemann/
- GitHub: https://github.com/NicklasKleemann
