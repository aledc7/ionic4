![ionic 4](https://raw.githubusercontent.com/aledc7/ionic4/master/resources/ionic.jpg)


[![aledc.tk](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/aledc.com.svg)](https://aledc.tk)
[![ingenea.com.ar](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/ingenea.svg)](http://ingenea.com.ar)
[![License](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/mit-license.svg)](https://aledc.com)
[![GitHub release](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/release.svg)](https://aledc.com)
[![Dependencies](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/dependencias-none.svg)](https://aledc.com)


# IONIC 4

## Documentación del curso de Ionic 4 que me encuentro realizando.

# Instalación

En esta seccion se encuentran todo el proceso necesario para montar todo el entorno de desarrollo.  

#### Pre requisitos:

Antes de poder comenzar la instalación del ambiente de desarrollo para usar Ionic 4, es requisito tener instaladas las siguientes aplicaciónes, en caso contrario obtendremos errores de diferente tipo.   

- [x] Node 10 o superior  
- [x] XCODE  
- [x] Android Studio  
- [x] VS Code  


#### Instalar ionic 4 desde la terminal  
```js
npm install -g ionic  
````

#### Luego instalar nuestro primer proyecto de ionic  
```js
ionic start

# Te da a elegir entre Angular y React

# Luego se debe seleccionar un template
````

### Instalar las dependencias de Capacitor
```js
npm install --save @capacitor/core @capacitor/cli
```
### verificar version de Capacitor
```js
npx cap --version
```
### Instalar Capacitor
```js
npx cap init
```

### Luego debo ejecutar Ionic Build para que se genere la carpeta 'www'
```js
ionic build
```

### Agrego compatibilidad con la plataforma Android
```js
npx cap add android
```
Luego podría abrir el proyecto de android con Android Studio con este comando:
```js
npx cap open android
```
### Luego Instalar la plataforma iOS
```js
npx cap add ios

# en caso que de este error '[error] cocoapods is not installed'. solucionarlo reinstalando:
brew reinstall cocoapods
```
Luego podría abrir el proyecto de ios con Xcode con este comando:
```js
npx cap open ios
```

###  Manteniendo sincronizado los proyectos

````
# Primero hacer un serve
ionic serve

# Luego hacer un build
ionic build

# Luego sincronizar
npx cap sync

# En caso de que las modificaciones no sean muy grandes, se puede usar el comando Copy, que se ejecutará mucho mas rápido.  
npx cap copy
````

Se puede hacer el build y el copy en un mismo comando:

````
ionic build && npx cap copy
````





