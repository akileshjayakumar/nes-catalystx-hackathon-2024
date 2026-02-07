# CatalystX 2024 Hackathon

Two AI learning prototypes in one repo: `edu-x-app` (multimodal Streamlit tutor) and `neo4j-draft-app` (Next.js + FastAPI curriculum chat with Neo4j-backed memory).

## Quick Start

### Prerequisites
- Python 3.10+
- Node.js 18+
- Docker Desktop (for `neo4j-draft-app` compose stack)

### Run EduX (`edu-x-app`)
```bash
cd edu-x-app
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
export NVIDIA_API_KEY="nvapi-..."
streamlit run app.py
```

### Run Neo4j Draft App (`neo4j-draft-app`)
```bash
cd neo4j-draft-app
docker compose up --build
```
- Client: `http://localhost:3000`
- API: `http://localhost:8000`

## Core Capabilities
- Multimodal tutoring from uploaded files and images.
- Speech-enabled interaction (speech-to-text and text-to-speech) in EduX.
- Curriculum-aware chat API with Neo4j conversation memory.
- Research notebooks and sample assets in `/research`.

## Configuration
Required environment variables:
- `NVIDIA_API_KEY` for `edu-x-app`
- `OPENAI_API_KEY` for `neo4j-draft-app/server`
- `NEO4J_URL` for `neo4j-draft-app/server`
- `NEO4J_USERNAME` for `neo4j-draft-app/server`
- `NEO4J_PASSWORD` for `neo4j-draft-app/server`

## Usage Examples
Start EduX:
```bash
cd edu-x-app
source .venv/bin/activate
streamlit run app.py
```

Start the Neo4j draft stack:
```bash
cd neo4j-draft-app
docker compose up
```

## Contributing And Testing
- Create a feature branch and keep changes scoped.
- Open a pull request with a clear summary of behavior changes.
- Run frontend lint checks:
```bash
cd neo4j-draft-app/client
npm install
npm run lint
```
- Python apps currently do not include committed automated tests.

## License
Proprietary. See [LICENSE](./LICENSE) for usage terms.
