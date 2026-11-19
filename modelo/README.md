# Definición del modelo

## Modelo base

| Campo | Valor | Por qué |
|---|---|---|
| Modelo | `qwen2.5:3b` (por confirmar) | Corre en CPU, buen español |
| Embeddings | por definir | |
| Modelo juez | `qwen2.5:7b-instruct` | Mayor capacidad que el modelo evaluado |

## Estrategia RAG (Admin Panel → Settings → Documents)

| Parámetro | v1 | v2 | Elegido |
|---|---|---|---|
| Chunk size (tokens) | 500 | 400 | |
| Chunk overlap (tokens) | 50 | 40 | |
| Top K | 4 | 4 | |

## Hiperparámetros del modelo personalizado (Workspace → Models)

| Parámetro | Valor | Por qué |
|---|---|---|
| Temperature | 0.2 | Respuestas consistentes y fieles al contexto |
| Top P | | |
| Max tokens | | |
| Context length | | |

Prompt system: [`system-prompt.md`](system-prompt.md). Capturas de cada pantalla en `../evidencias/interfaz/`.
