---
name: godot-dialogue-plugin-agent-skill
description: Godot 4 Dialogue Manager / Yarn Spinner integration, EventBus signals, story_flags mutations and .csv/.po localization.
---

# Godot 4 Dialogue Systems Agent Skill — Directiva de Habilidad

## Bootstrap de la Habilidad

Al detectar el trigger `$dialogue` o archivos del dominio, cargar en orden:
1. `.skill/godot-dialogue-plugin-agent-skill/SKILL.md`
2. `.skill/godot-dialogue-plugin-agent-skill/core/commands.md`
3. `.skill/godot-dialogue-plugin-agent-skill/core/brain.md`
4. `.skill/godot-dialogue-plugin-agent-skill/core/path_map.md`

## Reglas Canónicas

1. **Tipado estático GDScript 2.0 y `snake_case`**: Todos los scripts de diálogo (`dialogue_balloon.gd`, `dialogue_controller.gd`) usan tipado explícito.
2. **Desacoplamiento por EventBus / señales**: El globo de diálogo nunca referencia directamente al jugador o inventario; emite señales (`dialogue_started`, `dialogue_ended`, `flag_changed`).
3. **Desconectar señales en `_exit_tree()`**: Evitar referencias huérfanas al cambiar de escena.
4. **Estado narrativo centralizado**: Toda condición o mutación de diálogo consulta un Autoload dedicado (`StoryFlags` / `story_flags.gd`) alineado con `docs/lore/`.
5. **Textos localizables**: Cada línea debe portar clave de traducción estable (`[ID:...]`) compatible con `.csv`/`.po` de Godot.
6. **Inviolabilidad de `.skill/`**: Nunca editar archivos dentro de `.skill/godot-dialogue-plugin-agent-skill/` desde el proyecto cliente; registrar mejoras en `overview/learning.md` vía `$learnskill godot-dialogue-plugin-agent-skill [propuesta]`.
