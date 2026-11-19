# Asistente de soporte RAG — CloudOps Client Hub

Servicio de IA generativa de texto para el proyecto **CloudOps Client Hub** (diplomado CloudForge AI 5.0, Unicomfacauca).
Actividad 2 del módulo 6: un asistente de **soporte y PQRS** para los clientes de la agencia Forja Digital que responde
**solo** con la base de conocimiento del proyecto (planes, SLA, prioridades, estados, glosario y procedimientos).

Todo corre en local (Ollama + Open WebUI). Ningún dato sale a servicios de IA externos.

## Estructura

| Carpeta | Qué contiene |
|---|---|
| `conocimiento/` | Documentos de la base de conocimiento (Markdown) |
| `modelo/` | Prompt system, políticas y configuración RAG (chunk, overlap, top-k, hiperparámetros) |
| `golden-dataset/` | `golden_dataset.jsonl` con 50+ casos (prompt / comportamiento esperado) |
| `evaluacion/` | `evaluate_rag.py`, `test_openwebui_api.py` y `resultados/` de cada corrida |
| `evidencias/` | Capturas de la interfaz (`interfaz/`) y de la API (`api/`) |
| `informe/` | `Informe-modelo-rag-CloudOps-Client-Hub.pdf` |

## Cómo correrlo

```bash
docker compose up -d                       # Ollama en :11434 y Open WebUI en :3000
docker exec -it ollama-rag-lab ollama pull qwen2.5:3b
docker exec -it ollama-rag-lab ollama pull qwen2.5:7b-instruct   # modelo juez
cp .env.example .env                       # poner la API key de Open WebUI
pip install -r requirements.txt
python evaluacion/test_openwebui_api.py    # prueba unitaria por API
RUN_TAG="v1_chunk500_ov50" python evaluacion/evaluate_rag.py
```

Configuración del modelo en Open WebUI: ver [`modelo/README.md`](modelo/README.md).

## Cómo trabajamos

Ver [CONTRIBUTING.md](CONTRIBUTING.md): un issue por tarea, una rama por issue, PR con revisión de otro integrante.

## Aportes del equipo

<!-- Cada integrante agrega SU línea en un PR propio. -->

| Integrante | Usuario GitHub | Aporte |
|---|---|---|
| | | |
