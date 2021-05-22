# ESP32WebsocketServer

## Based on tuto from Shawn Hymel
https://shawnhymel.com/1882/how-to-create-a-web-server-with-websockets-using-an-esp32-in-arduino/

## Utilisation

### Librairies requises

- [x] ESPAsyncWebServer.h git@github.com:me-no-dev/ESPAsyncWebServer.git
- [x] + git@github.com:me-no-dev/AsyncTCP.git

- [x] WebSocketsServer.h git@github.com:Links2004/arduinoWebSockets.git

- [x] Arduino_JSON.h git@github.com:arduino-libraries/Arduino_JSON.git

### Configuration wifi

éditer le fichier config.h pour ajouter le SSID et le mot de passe du réseau wifi

```
#define WIFI_SSID "YOURSSID"
#define WIFI_PASSWORD "YOURPASSWORD"
```

Une fois connecté l'adresse IP s'affiche dans le moniteur série

```
....
My IP address: 192.168.1.148
```

Modifiez ensuite dans le fichier: data/index.html

l'adresse IP 192.168.1.148 par celle obtenue dans le port série.

```
var url = "ws://192.168.1.148:1337/";
```
Nb: ici :1337 permet d'indiquer le port d'écoute du Websocket

### Envoyer les fichiers de la page web dans la mémoire SPIFFS

#### Installer le plugin suivant :

https://github.com/me-no-dev/arduino-esp32fs-plugin

#### Envoyer les fichiers du répertoire data

depuis le menu "Outils" de l'éditeur Arduino > "ESP32 Sketch data upload"

### Accéder à l'interface web

si 192.168.1.148 est l'adresse de votre ESP32, alors vous pouvez ouvrir
votre navigateur préféré à l'adresse : http://192.168.1.148