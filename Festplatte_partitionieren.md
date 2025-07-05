# Festplatte partitionieren

#Linux #Arch #KubeCraft

- Eine Partition ist ein abgetrennter Bereich auf einer Festplatte
- Man braucht eine kleine Boot-Partition und eine große `root`-Partition (wo das System drauf ist)
- `lsblk` zeigt die Festplatten und Partitionen an
- Unter `/dev` gibt es für jede Festplatte und Partition eine Datei, die diese repräsentiert (_alles unter Unix ist eine Datei_)
- Deine Partitionierung hängt von deiner [[Verschlüsselung_Arch|Verschlüsselung]] ab
- Früher war es ziemlich schwer, die Partitionierung in Nachhinein zu verändern
- Zum Glück gibt es mittlerweile...

## LVM

- Bei LVM erstellst du nur eine große Partition (und eine Boot-Partition)
- Und in dieser Partition kannst du ganz einfach Logische Volumes kreieren
- Du kannst die Größe der Volumes im Nachhinein ändern
- Ein Volume kann sich sogar über mehrere physische Festplatten erstrecken

## Partitionieren mit `fdisk`

- `m` drücken für Hilfe

1. `fdisk /dev/nvme0n1` um die Festplatte zu öffnen (sie kann auch zB `sda` heißen)
2. `g` um eine neue GPT-Partitionstabelle zu erstellen und damit alle vorhandenen Partitionen zu löschen
3. `n` um eine neue Partition zu erstellen. Das wird die Boot-Partition. Zwei mal `Enter` drücken, um Standardwerte für Nummer und ersten Sektor zu akzeptieren. Bei `Last sector` +1G eingeben, um sie 1 GiB groß zu machen. 
4. Typ der Boot-Partition ändern:
   1. `t` drücken. Partition 1 wird automatisch ausgewählt.
   2. `1` eingeben  für EFI-System
5. LVM-Partition erstellen (`n`)
   - Standardwerte für Nummer und `First sector` akzeptieren
   - Und für `Last sector` auch. Damit nimmt die Partition den Rest der Festplatte ein.
   - Typ ändern (`t`): `44` für Linux LVM
6. `w` um die Änderungen zu speichern
