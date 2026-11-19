# Checklist de Auditoría — `$dialogue:audit`

- [ ] Scripts en `snake_case` con tipado estático GDScript 2.0.
- [ ] Cero referencias rígidas (`get_node('/root/Player')`) dentro del globo de diálogo.
- [ ] Señales desconectadas en `_exit_tree()`.
- [ ] Input del jugador restaurado garantizadamente al terminar el diálogo.
- [ ] Flags y variables sincronizadas con `docs/lore/`.
