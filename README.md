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


