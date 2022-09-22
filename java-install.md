## Install Java 11 from APT
```
apt install openjdk-11-jre-headless
```

### Install Java 11 from source
```
wget https://download.java.net/openjdk/jdk11/ri/openjdk-11+28_linux-x64_bin.tar.gz
sudo mkdir -p /usr/lib/jvm
sudo tar zxvf openjdk-11+28_linux-x64_bin.tar.gz -C /usr/lib/jvm
sudo update-alternatives --install "/usr/bin/java" "java" "/usr/lib/jvm/jdk-11/bin/java" 1
sudo update-alternatives --set java /usr/lib/jvm/jdk-11/bin/java
java -version
```
## Versions and Download Links [Click here to see all available versions](https://jdk.java.net/)

### OPTIONAL TO SWAP THE VERSION:
```
sudo update-alternatives --config java
```
