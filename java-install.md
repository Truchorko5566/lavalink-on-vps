## Instalar Java 11 desde APT
```
apt install openjdk-11-jre-headless
```

### Instalar Java 11 desde la fuente
```
wget https://download.java.net/openjdk/jdk11/ri/openjdk-11+28_linux-x64_bin.tar.gz
sudo mkdir -p /usr/lib/jvm
sudo tar zxvf openjdk-11+28_linux-x64_bin.tar.gz -C /usr/lib/jvm
sudo update-alternatives --install "/usr/bin/java" "java" "/usr/lib/jvm/jdk-11/bin/java" 1
sudo update-alternatives --set java /usr/lib/jvm/jdk-11/bin/java
java -version
```
## Versiones y enlaces de descarga [Haga clic aquí para ver todas las versiones disponibles](https://jdk.java.net/)

### OPCIONAL PARA CAMBIAR LA VERSIÓN:
```
sudo update-alternatives --config java
```
