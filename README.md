# CatalystX 2024 Hackathon

Hackathon repository with two education-focused AI prototypes: a multimodal tutor (`edu-x-app`) and a curriculum chat app backed by Neo4j (`neo4j-draft-app`).

## Quick Start

### Prerequisites
- Python 3.10+
- Node.js 18+
- Docker (for the Neo4j draft app via Docker Compose)

### 1) Run EduX (Streamlit tutor)
```bash
cd edu-x-app
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
export NVIDIA_API_KEY="nvapi-..."
streamlit run app.py
```

### 2) Run Neo4j Draft App (Next.js + FastAPI)
```bash
cd neo4j-draft-app
docker compose up --build
```

Client runs on `http://localhost:3000`, server API on `http://localhost:8000`.

## Core Capabilities
- Multimodal document tutoring from PDFs, PPTX, and images.
- Voice-enabled interactions (speech-to-text and text-to-speech) in EduX.
- Curriculum-aware conversational tutoring service with persistent history in Neo4j.
- Separate research notebooks and sample images in `/research` for experimentation.

## Configuration
- `NVIDIA_API_KEY`: required by `edu-x-app` to call NVIDIA models.
- `OPENAI_API_KEY`: required by `neo4j-draft-app/server`.
- `NEO4J_URL`: Neo4j connection URL for `neo4j-draft-app/server`.
- `NEO4J_USERNAME`: Neo4j username for `neo4j-draft-app/server`.
- `NEO4J_PASSWORD`: Neo4j password for `neo4j-draft-app/server`.

## Usage
EduX:
```bash
cd edu-x-app
streamlit run app.py
```

Neo4j draft stack:
```bash
cd neo4j-draft-app
docker compose up
```

## Contributing and Testing
- Open a feature branch, keep changes scoped, and submit a PR.
- Frontend checks:
```bash
cd neo4j-draft-app/client
npm install
npm run lint
```
- Python services currently have no committed automated test suite.

## License
Proprietary. See [LICENSE](./LICENSE) for usage terms.
