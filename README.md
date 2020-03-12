# Guía de instalación

## Java

### Linux

Para instalar en Linux, lo primero es descargar el JDK, en este caso utilizaremos 
*OpenJDK*, primero deben descargar el binario apropiado para 
[OpenJDK](https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jdk_x64_linux_hotspot_13.0.2_8.tar.gz), 
pero puede ser cualquier otra distribución.

Luego, desde el directorio donde hayan guardado el JDK:

```bash
tar -xf OpenJDK13U-jdk_x64_linux_hotspot_13.0.2_8.tar.gz
export PATH=$PWD/jdk-13.0.2+8/bin:$PATH
java -version
```

Si java se instaló correctamente entonces el último comando debiera imprimir en consola
la versión del JDK.

### Windows

#### Chocolatey

Existen varias maneras de instalar Java en Windows, pero recomendamos utilizar el gestor
de paquetes *Chocolatey* que se encargará de descargar y configurar el JDK.
Para obtener el gestor de paquetes, abran una ventana de PowerShell como administrador e
ingresen los comandos:

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Force
Invoke-WebRequest https://chocolatey.org/install.ps1 -UseBasicParsing | Invoke-Expression
```

#### JDK

Asumiendo que hayan instalado Chocolatey, el JDK se puede obtener ejecutando los 
siguientes comandos en una terminal de *PowerShell* con permisos de administrador:

```powershell
cinst openjdk -y
refreshenv
java -version
```

Si se puede ejecutar el último comando es que el JDK se instaló correctamente.

### MacOS

Instalar Java en Mac es similar a Linux, lo primero es descargar 
[OpenJDK](https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jdk_x64_mac_hotspot_13.0.2_8.tar.gz).

Una vez descargado, desde la carpeta donde se guardó el JDK:

```bash
tar -xf OpenJDK13U-jdk_x64_mac_hotspot_13.0.2_8.tar.gz
export PATH=$PWD/jdk-13.0.2+8/Contents/Home/bin:$PATH
java -version
```

El último comando debiera imprimir en consola la versión de Java que hayan instalado.

## Git

### Linux

Para sistemas basados en Debian (como Ubuntu), deben ejecutar:

```bash
sudo apt install git-all
```

En el caso de sistemas basados en Arch (como Manjaro), el comando necesario es:

```bash
sudo pacman -S git
```

### Windows

Asumiendo que tienen *Chocolatey* instalado, desde *PowerShell* como administrador 
ejecuten:

```
cinst git.install -y
```

### MacOS

Pueden descargar el instalador de 
[Git for Mac](https://sourceforge.net/projects/git-osx-installer/files/), o si tienen 
*Homebrew*:

```bash
brew install git
```

## IntelliJ IDEA

Lo primero que necesitarán para instalar IntelliJ es una licencia de estudiante, para 
obtenerla deben solicitar el beneficio desde el 
[sitio de JetBrains](https://www.jetbrains.com/community/education/#students).

Para que la solicitud sea aceptada deben registrarse con su correo de la universidad.

Una vez que tengan la licencia podrán descargar y utilizar **IntelliJ Ultimate**, si aún 
no tienen la licencia pueden descargar la versión *Comunity* que es completamente 
gratuita.
Para fines del curso, cualquiera de las 2 versiones basta, pero se les recomienda la 
primera opción ya que es más poderosa y provee de más funcionalidades.

IntelliJ se puede descargar desde [aquí](https://www.jetbrains.com/idea/download).

## (Opcional) ``cmder`` para Windows

``cmder`` es un emulador de consola para Windows mucho más flexible y personalizable que
la consola por defecto del SO.
El emulador puede ejecutar *PowerShell*, *Command Promt* (``cmd``), *Windows Subsystem* 
*for Linux* (WSL), y otros.

Una guía bastante completa de como instalar y configurar ``cmder`` se puede encontrar 
[aquí](https://gist.github.com/jchandra74/5b0c94385175c7a8d1cb39bc5157365e)
