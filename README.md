## Instalacion

# Paso 1
* Primero tiene que crear una carpeta con el nombre que quiera esto es para que todos los archivos que va a instalar esten juntos
* Despues de hacer lo anterior tiene que instalar **Lavalink.jar** precione aca para que vea como hacerlo [Click](https://github.com/Truchorko5566/lavalink-on-vps/blob/vps-linux/Lavalink.jar.md)

# Paso 2
* Primero tiene que instalar **Java11** precione aca para que vea como hacerlo [Click](https://github.com/Truchorko5566/lavalink-on-vps/blob/vps-linux/java-install.md) 
+ Segundo dentro de la **Carpeta anterior mente mencionada** cree un archivo llamado **application.yml** para que dentro copie esto:
```yml
server: # Servidor REST y WS
  port: 2333
  address: 0.0.0.0
lavalink:
  server:
    password: "youshallnotpass" # puede ser cualquier cosa debe ser la misma contraseña para conectarse!
    sources:
      youtube: true # permitir que youtube funcione (scraping)
      bandcamp: true # permitir el raspado de bandcamp
      soundcloud: true # permitir el raspado de soundcloud
      twitch: true # permitir el raspado de contracción
      vimeo: true # permitir el raspado de vimeo
      mixer: true # permitir el raspado del mezclador
      http: true # permitir el raspado de http, por ejemplo, transmisiones de estaciones de radio
      local: false # permitir la reproducción de archivos almacenados localmente (en el mismo host/pc) (.mp3, etc.)
    bufferDurationMs: 150 # Con qué frecuencia se envía una actualización en milisegundos
    youtubePlaylistLoadLimit: 3 # 3 medios... 300 canciones máximo/lista de reproducción
    youtubeSearchEnabled: true # Si se le permite buscar a través de youtube
    soundcloudSearchEnabled: true # Si se le permite buscar a través de SoundCloud
    gc-warnings: true 

    #ratelimit: # Si tiene un ipv6, habilite esto, para que pueda alojar lavalink por mucho más tiempo
      #ipBlocks: ["Ipv6/48", "Andere_Ipv6/48"] # lista de bloques de ip
      #strategy: "RotateOnBan" # RotateOnBan | LoadBalance | NanoSwitch | RotatingNanoSwitch
metrics:
  prometheus:
    enabled: false
    endpoint: /metrics
sentry:
  dsn: ""
logging:
  file:
    max-history: 5
    max-size: 100MB
  path: ./logs/
  level:
    root: INFO
    lavalink: INFO
```

# Paso 3
* Recuerda que todo lo instalado tiene que estar dentro de una sola carpeta para que inicie correctamente

# Paso 4
* Para esta parte solo tienes que iniciar todo con este comando ` java -jar Lavalink.jar ` pero como esto es para una vps puedes iniciarlo en segundo plano con **PM2** para instalar **PM2** solo ejecute ` npm i -g pm2 ` y ya estara en su sistema **(para iniciar lavalink en segundo plano ejecute ` pm2 start java -- -jar Lavalink.jar ` **OJO TIENE QUE INICIARLO DENTRO DE LA CARPETA CON TODO LOS CONPONENTES LAVALINK)**



