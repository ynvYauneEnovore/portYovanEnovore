---
title: 'Instalación en Arch Linux WiFi'
description: 'Reseteo e instalción nativa por línea de comando.'
pubDate: 'Apr 28 2024'
image: 'https://w.wallhaven.cc/full/42/wallhaven-42m73g.jpg'
tags:
  - Linux
badge: Arch Linux
---

En caso de que se cuelgue, tendrías que reiniciar el servicio en Arch para poder abrir "iwctl", el gestor de redes wifi por consola. Puedes hacerlo con el siguiente comando:

```bash
$ systemctl restart iwd.service
```
Luego de eso, ya podrías entrar al programa administrador de redes wifi con:
```bash
$ iwctl
```

Con la conexión exitosa, puedes ver qué estaciones tienes disponibles con:
```bash
$ device list
```

Luego de ver los dispositivos, puedes escanear las redes con:
```bash
$ station wlan0 scan
```

Y para poder ver los resultados del escaneo:
```bash
$ station wlan0 get-networks
```

Luego de ver las listas, puedes conectarte con:
```bash
$ station wlan0 connect [nombre_de_la_red]
```
Recuerda reemplazar <mark>[nombre_de_la_red]</mark> con el nombre de la red a la que deseas conectarte, si es nesario te pedira la contraceña.
