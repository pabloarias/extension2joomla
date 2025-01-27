# Extension2Joomla

## Cómo funciona

Te permite tener el código de tus extensiones organizado en una carpeta de tu equipo, realizando aquí las modificaciones necesarias para el desarrollo y actualizando en tiempo real este código hacia un sitio Joomla en local para comprobar los resultados.

## Estructura de carpetas de las extensiones

A tener en cuenta que los nombres de las extensiones deben respetarse tal y como se muestran a continuación (en inglés).

Solo en el caso de los módulos se deberá nombrar tanto el archivo de manifiesto, como el archivo de entrada con el prefijo "mod_".

El archivo de manifiesto de las plantillas es siempre "templateDetails.xml".

```
my-extensions
    |--components
    |   |
    |   '-- foo
    |       |-- admin
    |       |-- site
    |       |-- media
    |       '-- foo.xml
    |--libraries
    |   |
    |   '-- foo
    |       |-- language
    |       |-- src
    |       '-- foo.xml
    |--modules
    |   |
    |   '-- [ site|admin ]
    |       |
    |       '--foo
    |           |-- onefolder
    |           |-- language
    |           |-- anotherfolder
    |           |-- mod_foo.php
    |           '-- mod_foo.xml
    |--plugins
    |   |
    |   '-- [ system|user|content|... ]
    |       |
    |       '--foo
    |           |-- forms
    |           |-- language
    |           |-- anotherfolder
    |           |-- foo.php
    |           '-- foo.xml
    '--templates
        |
        '-- [ site|admin ]
            |
            '--foo
                |-- html
                |-- language
                |-- media
                |-- component.php
                |-- error.php
                |-- index.php
                |-- joomla.asset.json
                |-- offline.php
                |-- template_preview.png
                |-- template_thumbnail.png
                '-- templateDetails.xml
```

## Instalación

Debes tener instalado en el equipo Node.js.

Realizar un clone de este repositorio a local. Dentro del repositorio local instalar paquetes node con `npm install`.

Renombrar fichero config.json.dist a config.json. Dentro de este fichero añadir los valores de las variables (rutas absolutas a las carpetas).

Hacer una copia del fichero extensions-config.json.dist y pegar dentro de la carpeta origen de los ficheros de extensiones. Debe llamarse extensions-config.json y tener solo la estructura que tu extensión necesite.