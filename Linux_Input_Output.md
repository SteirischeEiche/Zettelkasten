# Linux: Input/Output

#Terminal #boot.dev

- Der "help"-Output ist i.d.R. eine Kurzfassung des Manuals

## Exit Codes
- Über Exit Codes kommunizieren Programme, ob sie erfolgreich ausgeführt wurden oder nicht
- `0` steht für Erfolg, alles andere für einen Fehler
- Programme, die ein anderes Programm aufrufen, checken mithilfe von Exit Codes, ob alles glatt gelaufen ist
- `echo $?` gibt den Exit Code des letzten Programms aus

## Datenströme
- Stdin, Stdout und Stderr sind __Datenströme__
- Stdout ist der Standardort an dem Programme ihre Outputs drucken
- In Python kann man Stdout mit der `print`-Funktion drucken (in der Shell mit `echo`)
- Stderr ist ein anderer Datenstrom als Stdout, damit er an einen anderen Ort umgeleitet werden kann (standardmäßig druckt er im Terminal)
- Datenströme umleiten: Mit `>` kannst du Stdout umleiten, mit `2>` Stderr und mit `<` Stdin
- Dateien im `/tmp/`-Verzeichnis werden regelmäßig vom System gelöscht
- Stdin ist der Standardort an dem Programme ihren Input _lesen_
- In Python kann man mit der `input`-Funktion aus dem Stdin lesen
- `|` leitet Stdout eines Programms an Stdin eines anderen Programms weiter

## Prozesse
- Wenn ein Programm gerade ausgeführt wird, nennt man das einen Prozess
- Mit `Ctrl+C` kannst du ein "SIGINT"-Signal an einen Prozess senden, das diesen beendet
- Wenn der Prozess darauf nicht reagiert, öffne ein neues Terminal und töte ihn mit: `kill PID`
- `top` zeigt an, welche Programme am meisten Ressourcen verbrauchen
- `top` sortiert Programme nach CPU-Nutzung
- Mit `M` (`o mem <Enter>` unter macOS) kannst du nach RAM-Nutzung sortieren
