# Plantilla Canónica — Escucha de Diálogo en Escena

```gdscript
extends Node

func _ready() -> void:
	EventBus.dialogue_started.connect(_on_dialogue_started)
	EventBus.dialogue_finished.connect(_on_dialogue_finished)

func _exit_tree() -> void:
	if EventBus.dialogue_started.is_connected(_on_dialogue_started):
		EventBus.dialogue_started.disconnect(_on_dialogue_started)
	if EventBus.dialogue_finished.is_connected(_on_dialogue_finished):
		EventBus.dialogue_finished.disconnect(_on_dialogue_finished)
```
