# TFG-ELASTEST-SUT
Aplicación MEAN para realizar los test sobre ella.

## Objetivos
En este repositorio se encuentran los módulos necesarios para desplegar una aplicación
MEAN.
Esta aplicación es híbrida por lo que existe tanto una versión web como móvil.
Se necesitan desplegar todos los módiulos de este repositorio para que funcione
correctamente.

La aplicación móvil hecha con Cordova tiene limitaciones que deben de ser consultados
en el [README.md][tfg-elastest-cordova]
de su repositorio. 

## Componentes
Los componentes de la aplicación se encuentran cada uno en su repositorio. Esta
aplicación se compone fundamentalmente de 3 componentes.

### Front end Angular
Aplicación Angular que hace uso de back end por la URL `localhost:3000`. 
Para acceder a esta aplicación acceder a `localhost:4200` con el navegador.

Se explica más en profundidad del funcionamiento y componenetes en el [README.md][tfg-elastest-front]
 del repositorio.

### Back end NodeJS y Express
Aplicación de servidor desarrollado con NodeJS y Express que gestiona la lógica de
la aplicación y gestiona la base de datos MongoDB.

Se explica más en profundidad del funcionamiento y componenetes en el [README.md][tfg-elastest-back]
 del repositorio.

### Base de datos MongoDB
Se despliega junto al back end y almacena el contenido de la aplicación, menos las 
imagenes que se almacenan en el sistema de ficheros de la máquina donde se despliegue
el servidor NodeJS.

### Aplicación móvil (Con Cordova)
Aplicación Android hecha a partir de el front end realizado con Angular. Se ha 
construido mediante el framework Cordova.

Esta aplicación tiene limitaciones en cuanto su conectividad al back end, que se
explican en el [README.md][tfg-elastest-cordova] de su repositorio.


## Despliegue
Esta aplicación cuenta con submodulos por lo que la forma de clonarlo debe ser:
```git clone --recurse-submodules https://github.com/DavidCorreas/tfg-elastest-sut.git```

### Despliegue de la aplicación web
Para desplegar la aplicación situarse en la carpeta raíz del proyecto y ejecutar ```docker-compose up```

### Despliegue aplicación móvil
Para desplegar la apliación móvil se necesitan de más modulos, como el emulador dockerizado. Para saber
más acerca del despliegue de la aplciación móvil se debe consultar el repositorio raíz del proyecto 
[tfg-elastest][tfg-elastest].

[tfg-elastest-cordova]: https://github.com/DavidCorreas/tfg-elastest-sut-cordova_app/blob/master/README.md
[tfg-elastest-front]: https://github.com/DavidCorreas/tfg-elastest-sut-front/blob/master/README.md
[tfg-elastest-back]: https://github.com/DavidCorreas/tfg-elastest-sut-back/blob/master/README.md
[tfg-elastest]: https://github.com/DavidCorreas/tfg-elastest
