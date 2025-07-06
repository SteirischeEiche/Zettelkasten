# Verschlüsselung in Arch

#Linux #Arch #KubeCraft

- Wenn du deine Festplatte nicht verschlüsselst, bist du nicht bereit Arch zu verwenden!
- Im professionellen Kontext (Firmen-Daten) muss alles verschlüsselt werden
- Wenn deine Festplatte verschlüsselt ist, und jemand deinen Laptop klaut, kann er nicht auf die Festplatte zugreifen

---

- Wir werden die große LVM-Partition im Ganzen verschlüsseln
- Das ist deutlich komfortabler als die Volumes einzeln mit einzelnen Passphrasen zu verschlüsseln

## Verschlüsseln mit Dm-crypt

1. Einen verschlüsselten LUKS-Container erstellen: `cryptsetup luksFormat /dev/nvme0n1p2`
2. Den Container öffnen: `cryptsetup open /dev/nvme0n1p2 cryptlvm`
3. In dem Container ein physisches Volumes erstellen: `pvcreate /dev/mapper/cryptlvm`
4. Eine Volume-Gruppe erstellen: `vgcreate Gruppenname /dev/mapper/cryptlvm`
5. Die logischen Volumes erstellen:
   1. Swap erstellen: `lvcreate -L 4G -n swap Gruppenname`
      - Die Größe des Swap hängt von der Größe der RAM ab
      - Swap kann vom Computer genutzt werden, wenn RAM voll ist
   2. Root-Volume: `lvcreate -L 32G -n root Gruppenname`
   3. Home-Volume: `lvcreate -l 100%FREE -n home Gruppenname`
6. Auf den Partitionen muss ein Dateisystem sein, sonst kann das OS nichts damit anfangen
   1. `mkfs.ext4 /dev/Gruppenname/root`
      - Wie verwenden Ext4
      - Eine Alternative, die Schnappschüsse ermöglicht ist Btrfs
   2. `mkfs.ext4 /dev/Gruppenname/home`
   3. `mkswap /dev/Gruppenname/swap`
   4. `mkfs.fat -F32 /dev/nvme0n1p1`
7. Die Partitionen einhängen (wenn etwas nicht eingehängt ist, hat das OS keinen Zugriff darauf)
   1. `mount --mkdir /dev/nvme0n1p1 /mnt/boot`
