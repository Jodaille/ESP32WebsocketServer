# ESP32WebsocketServer

## Based on tuto from Shawn Hymel
https://shawnhymel.com/1882/how-to-create-a-web-server-with-websockets-using-an-esp32-in-arduino/

## Utilisation

### Configuration wifi

éditer le fichier config.h pour ajouter le SSID et le mot de passe du réseau wifi

Une fois connecté l'adresse IP s'affiche dans le moniteur série

Modifié ensuite dans le fichier: Websocket/data/index.html

l'adresse IP 192.168.1.148 par celle obtenue dans le port série.

### Envoyer les fichiers de la page web dans la mémoire SPIFFS

#### Installer le plugin suivant :

https://github.com/me-no-dev/arduino-esp32fs-plugin

#### Envoyer les fichiers du répertoire data

depuis le menu "Outils" de l'éditeur Arduino > "ESP32 Sketch data upload"

### Accéder à l'interface web

si 192.168.1.148 est l'adresse de votre ESP32, alors vous pouvez ouvrir
votre navigateur préféré à l'adresse : http://192.168.1.148