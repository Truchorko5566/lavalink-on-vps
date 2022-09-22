### Instalacion

# Pasos
* Primero tiene que crear una carpeta con el nombre que quiera esto es para que todos los archivos que va a instalar esten juntos
* Despues de hacer lo anterior tiene que instalar **Lavalink.jar** precione aca para que vea como hacerlo [Click](https://github.com/Truchorko5566/lavalink-on-vps/blob/vps-linux/Lavalink.jar.md)

# Paso 2
* Primero tiene que instalar **Java11** precione aca para que vea como hacerlo [Click](https://github.com/Truchorko5566/lavalink-on-vps/blob/vps-linux/java-install.md) 
+ Segundo dentro de la **Carpeta anterior mente mencionada** cree un archivo llamado **application.yml** para que dentro copie esto:
```yml
server: # REST and WS server
  port: 2333
  address: 0.0.0.0
lavalink:
  server:
    password: "youshallnotpass" # can be anything must be the same password to connect to!
    sources:
      youtube: true # allow youtube to work (scraping)
      bandcamp: true # allow bandcamp scraping
      soundcloud: true # allow soundcloud scraping
      twitch: true # allow twitch scraping
      vimeo: true # allow vimeo scraping
      mixer: true # allow mixer scraping
      http: true # allow http scraping for example radio station streams
      local: false # allow playing local stored (on the same host/pc) files (.mp3, etc.)
    bufferDurationMs: 150 # How often a update is sent in milliseconds
    youtubePlaylistLoadLimit: 3 # 3 Means ... 300 Songs maximum / Playlist
    youtubeSearchEnabled: true # If u are allowed to search via youtube
    soundcloudSearchEnabled: true # If you are allowed to search via soundcloud
    gc-warnings: true 

    #ratelimit: # If you have an ipv6 enable this, so that you can host lavalink for way longer
      #ipBlocks: ["Ipv6/48", "Andere_Ipv6/48"] # list of ip blocks
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
