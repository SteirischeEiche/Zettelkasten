# LibreWolf

#Browser #Privacy #Dotfiles

- Niemals LibreWolf mit [[Tor]] benutzen (das Tor-Netzwerk funktioniert nicht, wenn du nicht den Tor-Browser benutzt)
- Es wird empfohlen, DRM nicht zu aktivieren

## Installation
- LibreWolf wird unter macOS als beschädigt markiert, weil das Team keine Apple Developer License hat (man kann dies mit `brew install librewolf --no-quarantine` verhindern)

## KeePassXC-Addon
- Laut FAQ muss man Native Messaging aktivieren damit das Addon funktioniert

## Probleme auf Webseiten
- Wenn auf einer Webseite Bilder nicht richtig angezeigt werden, musst du vielleicht Canvas aktivieren
- Manche Video-Telefonie-Dienste brauchen WebGL oder Autoplay

## Fingerabdruck
- Jede Einstellung, die du veränderst, kann deinen Fingerabdruck vergrößern
- Das gilt auch für jedes Addon, das du installierst
- Wegen RFP (Resist Fingerprinting) ist überall Light Theme aktiviert
- Das LibreWolf-Team empfiehlt, keine RFP-Einstellungen zu verändern

## Updates
- LibreWolf basiert immer auf der aktuellen (stabilen) Version von Firefox
- Updates kommen i.d.R. innerhalb von 3 Tagen nach dem Upstream-Release raus
- Wenn du LibreWolf per `.dmg` installierst, muss du es manuell aktualisieren
- Denn LibreWolf hat keine Auto-Update-Funktion und verlässt sich dafür auf Paket-Manager

## Was wegen [[Fingerprinting]] aus ist
- Webseiten wird die Sprache als `en-US` angezeigt
- WebGL ist ausgeschaltet

---

- Letterboxing verbessert den Datenschutz, weil die Fenstergröße dann nicht mehr in deinem Fingerabdruck ist
