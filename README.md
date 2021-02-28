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

## Divers

### Connaître son adresse IP publique
```bash
echo $(curl -s https://api.ipify.org)
```
