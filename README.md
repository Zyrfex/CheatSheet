# Cheat Sheet pour les Capture The Flag (CTF) par Zyrfex

## Cryptographie

### CyberChef - The Cyber Swiss Army Knife
Cette application Web permet d'effectuer une opération ou une série d’opérations sur un texte ou un fichier : 
https://gchq.github.io/CyberChef/

## Stéganographie

### Exiftool
Cette application Linux permet de consulter les métadonnées contenues dans le fichier : 
```
exiftool fichier.ext
```

### File
Cette commande Linux permet de connaître le type de fichier même si l'extension a été changée, en effet, elle se base sur les premiers octets du fichier qui sont appellés _magic numbers_ : 
```
file fichier.ext
```

### Stegsolve
Cette application Java permet l'analyse d'une image en profondeur avec notamment différentes vues possibles en fonction des couches de couleur : 
[Stegsolve v1.3](https://github.com/Zyrfex/CheatSheet/raw/main/Outils/Stegsolve%20v1.3.jar)

### Strings
Cette commande Linux permet d'afficher toutes les chaînes de caractères dédoublonnées d'au moins 10 caractères qui se trouvent dans le fichier : 
```
strings fichier.ext | awk 'length($0)>9' | sort -u
```
