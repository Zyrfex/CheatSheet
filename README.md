# Cheat Sheet pour les Catch The Flag (CTF) par Zyrfex

## Stéganographie

### Strings
Cette commande permet d'afficher toutes les chaînes de caractères dédoublonnées d'au moins 10 caractères qui se trouvent dans le fichier :
```
strings fichier.ext | awk 'length($0)>9' | sort -u
```

### Stegsolve
Téléchargez ici [Stegsolve v1.3](https://github.com/Zyrfex/CheatSheet/raw/main/Outils/Stegsolve%20v1.3.jar)
