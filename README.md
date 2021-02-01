# Cheat Sheet par Zyrfex

## Enumération

### Découverte des machines sur le réseau
```bash
sudo nmap -sn 192.168.1.0/24 | awk '/^(Nmap scan|MAC Address)/{ORS=(f+=sub(/^.*(for|:..) /,""))%2?OFS:RS; print}END{printf "<<= Mon IP\n"}'
```
```bash
sudo netdiscover
```

### Analyse d'une machine sur le réseau (système d'exploitation, principaux ports => programme et version)
```bash
sudo nmap -p1-65535 -A -T4 192.168.1.1
```

## Cryptographie

### CyberChef - The Cyber Swiss Army Knife
Cette application Web permet d'effectuer une opération ou une série d’opérations sur un texte ou un fichier.  
Elle est accessible ici : [CyberChef - The Cyber Swiss Army Knife](https://gchq.github.io/CyberChef/)

### Morse
[Convertisseur audio](https://morsecode.world/international/decoder/audio-decoder-adaptive.html)  
[Convertisseur textuel](https://www.dcode.fr/code-morse)

### Nombre des moines Cisterciens
Description : [Wikipedia](https://fr.wikipedia.org/wiki/Syst%C3%A8me_cistercien_de_notation_num%C3%A9rique)  
Convertisseur : [DCODE](https://www.dcode.fr/nombres-cisterciens)

### RsaCtfTool
Cette application Python permet d'effectuer plusieurs types d'attaques sur du RSA.  
Elle est accessible ici : [RsaCtfTool](https://github.com/Ganapati/RsaCtfTool)  
Installation :
```bash
git clone https://github.com/Ganapati/RsaCtfTool.git
sudo apt-get install libgmp3-dev libmpc-dev
pip3 install -r "requirements.txt"
```
Utilisation :
```bash
python3 RsaCtfTool.py -n <n> -e <e> --uncipher <c>
```

### Rune
Description : [Wikipedia](https://fr.wikipedia.org/wiki/Rune)

## Stéganographie

### exiftool
Cette application Perl permet de consulter les métadonnées contenues dans un fichier.  
  
Installation :
```bash
sudo apt install libimage-exiftool-perl
```
Utilisation :
```bash
exiftool fichier.ext
```

### file
Cette commande Linux permet de connaître le type de fichier même si l'extension a été changée, en effet, elle se base sur les premiers octets du fichier qui sont appellés _magic numbers_.  
  
Utilisation :
```bash
file fichier.ext
```

### stegsolve
Cette application Java permet l'analyse d'un fichier image en profondeur avec notamment différentes vues possibles en fonction des couches de couleur.  
Elle est téléchargeable ici : [Stegsolve v1.3](https://github.com/Zyrfex/CheatSheet/raw/main/Outils/Stegsolve%20v1.3.jar)

### strings
Cette commande Linux permet d'afficher toutes les chaînes de caractères dédoublonnées d'au moins 10 caractères qui se trouvent dans un fichier.  
  
Utilisation :
```bash
strings fichier.ext | awk 'length($0)>9' | sort -u
```

### zsteg
Cette application Ruby permet de détecter des métadonnées contenues dans un fichier PNG ou BMP.  
  
Installation :
```bash
sudo gem install zsteg
```
Utilisation :
```bash
zsteg -a fichier.ext
```

## Divers

### Connaître son adresse IP publique
```bash
echo $(curl -s https://api.ipify.org)
```
