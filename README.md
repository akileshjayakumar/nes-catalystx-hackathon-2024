# CatalystX 2024 Hackathon

AI learning prototypes for tutoring and curriculum-aware chat:
- `edu-x-app`: Streamlit multimodal tutor with speech support.
- `neo4j-draft-app`: Next.js + FastAPI chat app with Neo4j-backed conversation memory.

## Quick Start

### Prerequisites
- Python 3.10+
- Node.js 18+
- Docker Desktop

### 1) Run EduX
```bash
cd edu-x-app
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
export NVIDIA_API_KEY="nvapi-..."
streamlit run app.py
```

### 2) Run Neo4j Draft App
Set required server variables in your shell before starting:
```bash
export OPENAI_API_KEY="sk-..."
export NEO4J_URL="neo4j+s://<instance>"
export NEO4J_USERNAME="<username>"
export NEO4J_PASSWORD="<password>"
```

Then start both services:
```bash
cd neo4j-draft-app
docker compose up --build
```

Endpoints:
- Client: `http://localhost:3000`
- API: `http://localhost:8000`

## Core Capabilities
- Multimodal tutoring from text, files, and images.
- Speech interaction in EduX (speech-to-text and text-to-speech).
- Curriculum-aware chat with persisted Neo4j conversation history.
- Supporting experimentation material in `research/`.

## Configuration
Required environment variables:
- `NVIDIA_API_KEY` (`edu-x-app`)
- `OPENAI_API_KEY` (`neo4j-draft-app/server`)
- `NEO4J_URL` (`neo4j-draft-app/server`)
- `NEO4J_USERNAME` (`neo4j-draft-app/server`)
- `NEO4J_PASSWORD` (`neo4j-draft-app/server`)

## Usage
Run EduX:
```bash
cd edu-x-app
source .venv/bin/activate
streamlit run app.py
```

Run Neo4j Draft App:
```bash
cd neo4j-draft-app
docker compose up
```

## Contributing And Testing
- Keep pull requests focused and scoped to one change set.
- Run frontend lint before opening a PR:
```bash
cd neo4j-draft-app/client
npm install
npm run lint
```
- No committed automated test suite currently exists for Python services.

## License
Licensed under the `MIT` license. See [LICENSE](./LICENSE) for full text.
