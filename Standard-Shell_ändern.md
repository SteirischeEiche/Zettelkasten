# Standard-Shell ändern

#Terminal

- Mit `chsh -s /bin/bash` stellst du zB Bash als Shell ein
- Dafür muss die Shell allerdings eine Standard-Shell sein
- Um eine Shell zur Standard-Shell zu machen, musst du sie in die `/etc/shells`-Datei schreiben
- Dafür musst du `sudo tee -a` benutzen, weil die Datei `root` gehört
- `sudo tee -a` ist sicherer als `sudo sh -c 'echo /bin/bash >> /etc/shells`, weil du nicht der ganzen Shell `root`-Rechte geben musst
