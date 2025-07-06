# Arch installieren

#Linux #KubeCraft

- Secure Boot muss aus sein (das Arch-Installations-Image unterstützt Secure Boot nicht)

1. Tastatur auf Deutsch stellen: `loadkeys de-latin1`
2. Schrift (genauer Konsolen-Font) vergrößern: `setfont ter-132b`
3. Den Boot-Modus prüfen: `cat /sys/firmware/efi/fw_platform_size`
   - Wenn `64` ausgegeben wird, ist alles gut (das System wurde im UEFI-Modus gebootet und hat einen 64-bit x64 UEFI)
4. LAN-Kabel einstecken oder mit WLAN verbinden (s. unten)
   - Verbindung testen: `ping archlinux.org`
5. Die System-Uhr aktualisieren: `timedatectl`
   - Dies synchronisiert die aktuelle Zeit mit der UTC-Zeit
6. [[Arch_Festplatte_partitionieren|Festplatte partitionieren]]
7. [[Arch_Verschlüsselung|Die Festplatte verschlüsseln]]

## Boot-Modus

- Es gibt zwei Boot-Modi: BIOS und UEFI
- Neuere Systeme (ab ca. 2015) nutzen UEFI
- BIOS wird von älteren Windows-Systemen genutzt

## WLAN

1. `iwctl` um den interaktiven Prompt anzuzeigen
2. `station list` um alle WLAN-Geräte (Karten) anzuzeigen
   - Wenn nichts angezeigt wird, Computer neustarten
3. `station _Name_des_Geräts_ get-networks` um alle verfügbaren Netzwerke anzuzeigen
4. `station _Name_ scan`
5. `station _Name_ show`
6. `station _name_ connect _name_des_netzwerks` um dich mit deinem Netzwerk zu verbinden
7. `exit`
- [Quelle](https://wiki.archlinux.org/title/Iwd#iwctl)
