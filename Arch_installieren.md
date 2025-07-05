# Arch installieren

#Linux #KubeCraft

- Secure Boot muss aus sein (das Arch-Installations-Image unterstützt Secure Boot nicht)

1. Tastatur auf Deutsch stellen: `loadkeys de-latin1`
2. Schrift (genauer Konsolen-Font) vergrößern: `setfont ter-132b`
3. Den Boot-Modus prüfen: `cat /sys/firmware/efi/fw_platform_size`
   - Wenn `64` ausgegeben wird, ist alles gut (das wurde im UEFI-Modus gebootet und hat einen 64-bit x64 UEFI)
4. LAN-Kabel einstecken
   - Verbindung testen: `ping archlinux.org`
5. Die System-Uhr aktualisieren: `timedatectl`
   - Dies synchronisiert die aktuelle Zeit mit der UTC-Zeit
6. [[Festplatte_partitionieren]]

## Boot-Modus

- Es gibt zwei Boot-Modi: BIOS und UEFI
- Neuere Systeme (ab ca. 2015) nutzen UEFI
- BIOS wird von älteren Windows-Systemen genutzt
