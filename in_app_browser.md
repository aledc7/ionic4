![ionic 4](https://raw.githubusercontent.com/aledc7/ionic4/master/resources/ionic.jpg)


[![aledc.tk](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/aledc.com.svg)](https://aledc.tk)
[![ingenea.com.ar](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/ingenea.svg)](http://ingenea.com.ar)
[![License](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/mit-license.svg)](https://aledc.com)
[![GitHub release](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/release.svg)](https://aledc.com)
[![Dependencies](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/dependencias-none.svg)](https://aledc.com)

# In App Browser


Se trata de un Plugin que permite encapsular una página web y convertirla facilmente en una APP, siempre que la página web que se vaya a incluír sea responsive.  

1. Primeramente crear un nuevo proyecto en Blanco:   
```php
ionic start nombre_app blank
````

2. luego, se creará una carpeta con el nombre, que le hayamos dado a la App,  entrar a esta e instalar el plugin en cuestion:
```php
# primero instalar el plugin via ionic
ionic cordova plugin add cordova-plugin-inappbrowser

# Luego instalar este via npm
npm install @ionic-native/in-app-browser
````

3. Una vez instalado el plugin, editar el archivo __/src/app/home/home.page.ts__   y agregar lo siguiente:  
```php

import { Component } from '@angular/core';

# Aca hago la importación del plugin
import { InAppBrowser } from '@ionic-native/in-app-browser/ngx';

# Esto se deja tal cual
@Component({
  selector: 'app-home',
  templateUrl: 'home.page.html',
  styleUrls: ['home.page.scss'],
})

export class HomePage {

  # Meto el plugin en el constructor
  constructor(private InAppBrowser : InAppBrowser) {}

  subscription: any

  # Instancio el plugin en este ciclo de vida, asi se ejecuta cuando ya está todo cargado.  
  ionViewDidEnter(){
  
  # Opcionalmente, puede que quiera ocultar la barra con la url que viene por defecto, y el zoom.
  # Para esto, hay que pasar estas opciones: `location=no,toolbar=no,zoom=no`
  
   this.InAppBrowser.create(`http://mipaginaweb.com/`,`_blank`,`location=no,toolbar=no,zoom=no`);

    }



}
````

4. Por último hay que editar el archivo __/src/app/app.module.ts__ y agregar lo siguiente
```php
import { NgModule } from '@angular/core';
import { BrowserModule } from '@angular/platform-browser';
import { RouteReuseStrategy } from '@angular/router';

import { IonicModule, IonicRouteStrategy } from '@ionic/angular';
import { SplashScreen } from '@ionic-native/splash-screen/ngx';
import { StatusBar } from '@ionic-native/status-bar/ngx';

import { AppComponent } from './app.component';
import { AppRoutingModule } from './app-routing.module';

# Agrego In App Browser
import { InAppBrowser} from '@ionic-native/in-app-browser/ngx';


@NgModule({
  declarations: [AppComponent],
  entryComponents: [],
  imports: [BrowserModule, IonicModule.forRoot(), AppRoutingModule],
  providers: [
    StatusBar,
    SplashScreen,
    { provide: RouteReuseStrategy, useClass: IonicRouteStrategy },
    
    # Agrego In App Browser al array de Providers.  
    InAppBrowser
  ],
  bootstrap: [AppComponent]
})
export class AppModule {}
````

Si todo fue bien, con estos pasos se tendrá una página web Responsive, encapsulada en una App Mobile, que luego podrá compilarse para subir al __Play Store__ de Android y al __App Store__ de Mac.

Eso es todo.








