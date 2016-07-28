#Zend Framework 3 Album Module

Este es un módulo del álbum de la muestra para el uso con [zend-mvc](https://docs.zendframework.com/zend-mvc) aplicaciones.

##Instalación

En primer lugar, decidir sobre un espacio de nombres para su nuevo módulo.

Clonar este repositorio en su aplicación:
```bash
$ Cd módulo
$ Git clone this Repository
$ Cd del álbum
```
Eliminar los residuos de GitHub:
```bash
$ Rm -rf .git .gitignore
$ Git eliminar remoto origen
```
El siguiente paso será cambiar el espacio de nombres en los diferentes archivos. Abra cada uno de config/module.config.php, src/Module.phpy src/Controller/AlbumController.php, y reemplazar cualquier aparición de Album su nuevo espacio de nombres.

##encontrar y remplazar

>remplace el nombre del Modulo "Album"
>El nombre del controlador AlbumController
>Remplazar el Nombre del Controlador, la vista (View), Nombre del NAMESPACE,
>La carpeta del modulo.
>A continuación, tenemos que la carga automática de configuración de la aplicación. Abra el composer.json archivo en la >raíz de la aplicación, y añadir una entrada bajo la autoload.psr-4clave:
```bash
" Auto-carga " : {
     " PSR-4 " : {
         "Album\\" : "Módulo/Album/src/"
    }
}
```
Recargando la Autocarga:

```bash
$ composer dump-autoload
```

Por último, notificar a la aplicación del módulo. Abrir config/modules.config.php, y añadirlo a la parte inferior de la lista:
```bash
return [ 
    / * ... * /,
    'Album' , 
]    
```
##application.config.php

>modules.config.phparchivo añadir su módulo:
>
> ```bash
>     php
> 'modules' => [
>     /* ... */
>     'Album',
> ],
>```    
