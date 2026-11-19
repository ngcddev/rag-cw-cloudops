# Evaluación

- `test_openwebui_api.py`: prueba unitaria por API contra el modelo personalizado.
- `evaluate_rag.py`: corre el golden dataset; mide latencia, éxito, palabras clave y puntaje del juez (1 a 5).
  Basado en el script del ejemplo del docente.
- `resultados/`: un `.jsonl` por corrida (`eval_<RUN_TAG>_<fecha>.jsonl`). Meta: **≥ 70 % de eficiencia**.
