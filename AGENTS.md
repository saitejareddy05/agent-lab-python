# AGENTS

Purpose: fast onboarding for coding agents in this repository.

## Mandatory Dev Checklist

Run all three before finishing significant changes:

- Lint: uv run ruff check .
- Build (syntax compile): uv run python -m compileall app tests
- Test: uv run pytest

## Core Map

- app/main.py: FastAPI routes and Jinja/HTMX rendering.
- app/game_service.py: session lifecycle and game orchestration.
- app/game_logic.py: pure board logic and bingo detection.
- app/models.py: immutable game models and enums.
- tests/test_game_logic.py: logic unit tests.
- tests/test_api.py: route integration tests.

## Editing Rules

- Keep game rules in app/game_logic.py; keep web/session wiring in app/main.py and app/game_service.py.
- For UI updates, preserve the existing Jinja partial + HTMX flow.
- Update tests with every behavior change (logic -> test_game_logic, routes/templates -> test_api).

## Existing Guidance

- .github/instructions/general.instructions.md
- .github/instructions/frontend-design.instructions.md
- .github/instructions/css-utilities.instructions.md
- .github/prompts/setup.prompt.md
- workshop/01-setup.md
- workshop/GUIDE.md
