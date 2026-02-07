# CatalystX 2024 Hackathon
AI learning prototypes for tutoring and curriculum-aware chat:

## Quick Start
```bash
cd edu-x-app
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
export NVIDIA_API_KEY="nvapi-..."
streamlit run app.py
```

## Capabilities
- `edu-x-app`: Streamlit multimodal tutor with speech support.
- `neo4j-draft-app`: Next.js + FastAPI chat app with Neo4j-backed conversation memory.
- Python 3.10+
- Node.js 18+

## Configuration
- `NVIDIA_API_KEY`: Required for related integrations/features.
- `OPENAI_API_KEY`: Required for related integrations/features.

## Usage
```bash
ls -la
```

## Contributing and Testing
- Contributions are welcome through pull requests with clear, scoped changes.
- No automated test suite is currently documented for this repository.

## License
Licensed under the `MIT` license. See [LICENSE](./LICENSE) for full text.
