# Patrones — Diálogos en Godot 4

## 1. Separación Datos vs Presentación
Los archivos `.dialogue` (o `.tres`) definen flujo, condiciones y mutaciones; la escena `CanvasLayer` solo renderiza texto, retratos y botones de respuesta.

## 2. Manejo Seguro de Input y Pausa
Deshabilitar el input de gameplay mediante señal `dialogue_started` y restaurarlo siempre en `dialogue_finished` (incluso si el diálogo se cancela).

## 3. Localización
Exportar claves `.csv`/`.po` con IDs estables para evitar romper traducciones al editar redacción.
