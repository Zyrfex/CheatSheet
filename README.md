# Cheat Sheet pour les Capture The Flag (CTF) par Zyrfex

## Enumération

### Découverte des machines sur le réseau
```
sudo nmap -sn 192.168.1.0/24
```
```
sudo netdiscover
```

## Cryptographie

### CyberChef - The Cyber Swiss Army Knife
Cette application Web permet d'effectuer une opération ou une série d’opérations sur un texte ou un fichier.  
Elle est accessible ici : https://gchq.github.io/CyberChef/

## Stéganographie

### exiftool
Cette application Perl permet de consulter les métadonnées contenues dans un fichier.  
  
Installation :
```
sudo apt install libimage-exiftool-perl
```
Utilisation :
```
exiftool fichier.ext
```

### file
Cette commande Linux permet de connaître le type de fichier même si l'extension a été changée, en effet, elle se base sur les premiers octets du fichier qui sont appellés _magic numbers_.  
  
Utilisation :
```
file fichier.ext
```

### stegsolve
Cette application Java permet l'analyse d'un fichier image en profondeur avec notamment différentes vues possibles en fonction des couches de couleur.  
Elle est téléchargeable ici : [Stegsolve v1.3](https://github.com/Zyrfex/CheatSheet/raw/main/Outils/Stegsolve%20v1.3.jar)

### strings
Cette commande Linux permet d'afficher toutes les chaînes de caractères dédoublonnées d'au moins 10 caractères qui se trouvent dans un fichier.  
  
Utilisation :
```
strings fichier.ext | awk 'length($0)>9' | sort -u
```

### zsteg
Cette application Ruby permet de détecter des métadonnées contenues dans un fichier PNG ou BMP.  
  
Installation :
```
sudo gem install zsteg
```
Utilisation :
```
zsteg -a fichier.ext
```

## Divers

### Connaître son adresse IP publique
```
echo $(curl -s https://api.ipify.org)
```
