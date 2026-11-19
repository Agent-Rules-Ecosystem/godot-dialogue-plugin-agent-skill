# Brain — Godot 4 Dialogue Systems

- **Arquitectura Godot**: Usar Autoload/EventBus + `Resource` (`.dialogue`/`.tres`) + escena `CanvasLayer` desacoplada para el globo de diálogo.
- **Sincronización con Lore**: Cada flag usada en condicionales debe existir en `docs/lore/narrative_tree.md`.
- **Auditoría**: `$dialogue:audit` inspecciona `scenes/dialogue/`, `scripts/dialogue/` y `assets/dialogue/`.
