![ionic 4](https://raw.githubusercontent.com/aledc7/ionic4/master/resources/ionic.jpg)


[![aledc.tk](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/aledc.com.svg)](https://aledc.tk)
[![ingenea.com.ar](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/ingenea.svg)](http://ingenea.com.ar)
[![License](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/mit-license.svg)](https://aledc.com)
[![GitHub release](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/release.svg)](https://aledc.com)
[![Dependencies](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/dependencias-none.svg)](https://aledc.com)

# Generando los Iconos de nuestra App y las imágenes de Splash Screen.


1. Primeramente se debe tener instalado el paquete de recursos
```php
npm i -g cordova-res
````
2. Luego debemos tener en la caropeta __/resources__ de nuestro proyecto, dos archivos.   
Uno será el logo de nuestra App, en formato PNG, y otro será la imágen que querramos usar como Splash Screen: 

- [x] icon.png  (con la medida  __1024x1024__ px) 
- [x] splash.png  (con la medida __2732x2732__ px)git 

3. Por último solo resta generar los recursos para las dos plataformas, android y iOS

```php
# Generamos los recursos para android
ionic cordova resources android

# Generamos los recursos para iOS
ionic cordova resources ios
````

Eso es todo, ahora si revisamos la carpeta __/resources/plataforma/icon/__ y __/resources/plataforma/splash/__  veremos todas las imagenes generadas.



