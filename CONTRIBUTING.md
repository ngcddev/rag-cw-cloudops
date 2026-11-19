# Cómo trabajamos

1. **Cada quien hace commits desde su propia cuenta y su propio PC.** Revisar que `git config user.email`
   sea un correo verificado en su cuenta de GitHub; si no, el commit no cuenta como suyo.
2. Tomar un issue del tablero y asignárselo.
3. Crear rama: `git checkout -b <tipo>/<issue>-<slug>` (ej. `feat/7-golden-fuera-de-alcance`).
4. Commits pequeños en español con Conventional Commits: `feat(golden): 15 casos de PQRS`.
5. Abrir PR con `Closes #N` y pedir revisión a otro integrante. `main` está protegida: no se sube directo.
6. Fusionar con **Create a merge commit** (conserva el historial de cada autor).

Commits y PR sin atribución a asistentes de IA (nada de `Co-Authored-By` ni "Generated with").

## Reglas

- Nada de secretos en el repo: la API key va en `.env` (ignorado por git).
- La base de conocimiento usa los datos ficticios de la demo; nunca datos reales de clientes.
