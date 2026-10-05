# app

Repositorio de demostración para [Symphony](https://linear.app/ayhungry), el flujo en el que un agente toma issues de Linear, hace el cambio en una rama, abre un pull request y lo deja en revisión.

## Qué es

Por ahora el repositorio no contiene código de aplicación: sirve como sandbox para probar el flujo de trabajo de Symphony de punta a punta (issue → rama → commit → pull request → revisión).

## Cómo se usa

1. Crea un issue en Linear con la etiqueta `ready for agent`.
2. El agente trabaja en una rama `feat/ayh-<n>-<slug>` y hace commits con [Conventional Commits](https://www.conventionalcommits.org/).
3. El agente abre un pull request contra `main` y mueve el issue a **In Review**.
4. Una persona revisa y hace el merge; el agente nunca fusiona pull requests.

## Estructura

- `README.md`: este archivo.
- `.gitignore`: ignora `.DS_Store`, `node_modules`, `dist` y archivos `.env` (excepto `.env.example`).

## Contribuir

- Usa Conventional Commits (`feat:`, `fix:`, `docs:`, `chore:`…).
- No subas secretos: los archivos `.env*` están ignorados.
