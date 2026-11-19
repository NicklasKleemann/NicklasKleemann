# Nicklas Vistoft Kleemann

> MSc Software Engineering @ Aalborg University CPH  ·  Associate Software Engineer @ NHTA

I build LLM document-extraction pipelines and the systems around them: crawlers that feed them, data platforms and cloud infrastructure that run them, and apps that put the results in front of people. On the side I write Linux tooling, mostly around authentication and browser automation.

---

## Toolbox

| Category | Tools and technologies |
| :--- | :--- |
| Languages | Python, TypeScript, JavaScript, Go, Java, C / C++, OCaml, Dart, SQL, Bash, LaTeX |
| LLM and agents | OpenAI, Anthropic, Gemini, LiteLLM, Ollama, vLLM, Hugging Face, LangChain, LlamaIndex, Pydantic AI, PageIndex, tool-calling agents, MCP servers |
| Extraction and retrieval | LlamaParse, Docling, PyMuPDF, Pydantic schemas, Pinecone, BM25 and hybrid retrieval, parent-child chunking, Typesense, Algolia |
| Evaluation and observability | Ragas, extract-bench, Langfuse, OpenTelemetry, Sentry, Prometheus |
| Scraping and data | Scrapy, Playwright, Camoufox, BeautifulSoup, Dagster, pandas, NumPy |
| Backend | FastAPI, Django REST, NestJS, Express, Hono, Spring Boot, Azure (Durable) Functions, SSE, JWT / OAuth |
| Frontend and mobile | React, Next.js, React Native, Expo, Flutter, Redux, Zustand, TanStack Query, Mantine, shadcn/ui, Tailwind, Storybook |
| Databases | PostgreSQL, MongoDB, MySQL, TiDB, Redis / Valkey, Prisma, SQLAlchemy, Mongoose |
| Infra and tooling | Docker, Azure, Cloudflare Workers, Vercel, Caddy, GitHub Actions, uv, pnpm, Turborepo |
| ML | PyTorch, TensorFlow / Keras, scikit-learn, Transformers, NLTK, gensim |
| Systems and Linux | PAM, TPM 2.0, FIDO2 / CTAP2, WebAuthn, USB/IP, D-Bus, bubblewrap, systemd, firewalld, WebAssembly, OCamllex / Menhir |
| Testing | TDD, pytest, Vitest, Jest, Supertest, Cypress, JUnit |
| Practices | Large-Scale Scrum (LeSS), Agile, Jira, Confluence, Lean Startup |

---

## Projects

### EFSA Data Extraction (MSc thesis)
Turns EFSA pesticide assessment PDFs into structured, IUCLID-shaped records. The model finds evidence either by walking a heading tree of the document or by grepping it inside a sandbox, and every extracted row cites the page it came from. Works with any major LLM provider.
**Stack:** Python · Pydantic · LiteLLM · PageIndex · bubblewrap · TiDB

### Qori (work, NHTA and Quantitative)
Nordic health technology assessment platform covering Denmark, Sweden and Norway. It started as NHTAi on Django REST, was rebuilt as serverless Azure Function Apps, and now runs on FastAPI. I built most of the PDF extraction pipeline for Danish Medicines Council reports, the HTA scrapers and crawlers, and the staging/production deploy setup.
**Stack:** FastAPI · Azure Durable Functions · LlamaParse · Pinecone · Scrapy · Dagster · React · Terraform

### [burrow-browser](https://github.com/NicklasKleemann/burrow-browser)
MCP server that gives AI agents a real headless browser. Agents can read JavaScript-heavy pages, fill in forms, inspect network traffic, mock failing APIs, and audit a site's security headers, CORS and TLS.
**Stack:** Python · MCP · Camoufox · Playwright

### [howdy-as-passkey](https://github.com/NicklasKleemann/howdy-as-passkey)
Virtual FIDO2/CTAP2 authenticator that turns Howdy face recognition into a WebAuthn passkey on Linux, the platform authenticator Linux never had. TPM-sealed vault and in-chip P-256 signing, runs fully unprivileged, IR-liveness gated.
**Stack:** Go · USB/IP · TPM 2.0 · PAM

### Kvæk
Grocery price-comparison app running in production. NestJS backend with a mobile client in Expo React Native, live price updates, price alerts with push notifications, product search, and a shopping-list optimizer that finds the cheapest way to shop a list.
**Stack:** NestJS · Prisma · PostgreSQL · Valkey · Typesense · Cloudflare Workers · Expo · Next.js

### [Educado](https://github.com/ErasmusEgalitarian/educado-frontend)
Education platform built by around 40 students in coordinated teams using Large-Scale Scrum. My team of six, Deadlocked, landed over a third of the semester's merged pull requests and around 40% of the commits to the web app and backend, and handled several of the dev → staging → main releases. I built the course manager in the content-creator app and the media upload routes in the backend.
**Stack:** React · TypeScript · Express · MongoDB · Google Cloud Storage · LeSS

### [AAU Concierge](https://github.com/SW7-AAU-Concierge-Project)
RAG system answering questions across 35+ Aalborg University sites. Hybrid retrieval (Pinecone + BM25) with semantic chunking and local models through Ollama and vLLM, reaching 97% response integrity measured with Ragas.
**Stack:** FastAPI · LangChain · Pinecone · BM25 · Ollama · Ragas

### [Numatix](https://github.com/SW4-GR1/Numatix)
WebAssembly compiler for a custom imperative language, written in OCaml. Full lexer, parser, and code generation.
**Stack:** OCaml · OCamllex · Menhir · WebAssembly

---

[LinkedIn](https://www.linkedin.com/in/nicklasvistoftkleemann/)
