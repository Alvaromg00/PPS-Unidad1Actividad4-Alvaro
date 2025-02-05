# Actividad 4: Prueba de aplicaciones en entorno controlado: Sandbox

## Indice:

#### [1. Alternativas de Sandboxes](#alternativas-de-sandboxes)  
#### [2. Creando entorno controlado y probando la calculadora](#creando-entorno-controlado-y-probando-la-calculadora)

## Alternativas de Sandboxes

Algunas de las opciones mas comunes que nos permiten crear sandboxes son:

> -**Máquinas virtuales** --> Ejecutan un sistema operativo completo dentro de otro, permitiendo pruebas aisladas.  

> -**Contenedores** --> Crean entornos de ejecución ligeros y sin necesidad de un sistema operativo completo, aunque no proporciona un aislamiento total como una VM (dependen del kernel del anfitrión).  

> -**chroot (linux)**  --> Crea un entorno aislado con su propio sistema de archivos en el mismo sistema operativo, aunque también puede interactuar con el kernel.  

> -**Firejail** --> Herramienta de sandboxing que aísla procesos y aplicaciones en entornos restringidos, además es fácil de usar.  

> -**Windows Sandbox** --> Funcionalidad en Windows 10/11 Pro y Enterprise que permite ejecutar aplicaciones en un entorno completamente aislado.  

## Creando entorno controlado y probando la calculadora

Para esta prueba vamos a utilizar `Firejail` que es una herramienta de sandboxing fácil de usar, y vamos a probar nuestra calculadora creada en ejercicios anteriores:

1. Lo primero es descargarnos el paquete .deb del repositorio de Debian:

[wget http://ftp.us.debian.org/debian/pool/main/f/firejail/firejail_0.9.72-2_amd64.deb](./Imagenes/1.png)

2. Una vez descargado, lo instalamos manualmente con `dpkg -i` :

[sudo dpkg -i firejail_0.9.72-2_amd64.deb](./Imagenes/2.png)

3. Ahora vamos a hacer pruebas en la **calculadora.py** dentro del entorno de Firejail, para ello nos movemos a la ruta donde se encuentra nuestra **calculadora.py** y desde hay ejecutamos `firejail python3 calculadora.py` entonces comenzará a ejecutarse la calculadora.py en el entorno de Firejail:

[firejail python3 calculadora.py](./Imagenes/3.png)

4. Una vez echo esto ya podemos probar el programa en un entorno controlado:

[Pruebas calculadora.py 1](./Imagenes/4.png)
[Pruebas calculadora.py 2](./Imagenes/5.png)
