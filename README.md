![ionic 4](https://raw.githubusercontent.com/aledc7/ionic4/master/resources/ionic.jpg)


[![aledc.tk](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/aledc.com.svg)](https://aledc.tk)
[![ingenea.com.ar](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/ingenea.svg)](http://ingenea.com.ar)
[![License](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/mit-license.svg)](https://aledc.com)
[![GitHub release](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/release.svg)](https://aledc.com)
[![Dependencies](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/dependencias-none.svg)](https://aledc.com)


# IONIC 4

## Documentación del curso de Ionic 4 que me encuentro realizando.

# Get Started

En esta seccion se encuentran todo el proceso necesario para montar todo el entorno de desarrollo.  

#### Pre requisitos:

Antes de poder comenzar la instalación del ambiente de desarrollo para Ionic 4, es requisito tener instaladas las siguientes aplicaciónes.

- [x] Node 10 o mayor
- [x] XCODE
- [x] Android Studio
- [x] VS Code


#### Instalar ionic 4 desde la terminal
```js
npm install -g ionic
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
```


