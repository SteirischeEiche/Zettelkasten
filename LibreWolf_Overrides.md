# LibreWolf Overrides

#Browser #Privacy #Dotfiles

- Alle Änderungen, die du im GUI machen kannst, kannst du auch in der `librewolf.overrides.cfg` machen
- Diese Datei wird bei jedem Start von Firefox gelesen

## `pref()` vs. `defaultPref()`
- Lieber `pref()` statt `defaultPref()` verwenden?
- Dadurch werden diese Einstellungen bei jedem Neustart zurückgesetzt, wenn der User sie per GUI verändert hat

---

- Die `cfg`-Datei wird wie ein Javascript behandelt
- Also gilt die Javascript-Syntax
