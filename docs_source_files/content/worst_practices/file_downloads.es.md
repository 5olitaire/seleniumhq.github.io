---
title: "Descarga de archivos"
weight: 2
---

Mientras que es posible empezar una descarga haciendo clic en el enlace, con el
navegador que este siendo controlado por Selenium, el API no expone el progreso 
de la descarga, haciéndolo poco ideal para probar la descarga de archivos.
Esto es debido a que descargar archivos no es considerado un aspecto importante 
de la emulación de las interacciones de los usuarios con las plataformas web.
En lugar de ello, se recomienda encontrar el enlace con Selenium (y cualquier
Cookie requerida) y pasarselo a una librería que permita hacer peticiones HTTP 
como [libcurl](//curl.haxx.se/libcurl/).

{{% notice info %}}
<i class="fas fa-language"></i> Page being translated from 
English to Spanish. Do you speak Spanish? Help us to translate
it by sending us pull requests!
{{% /notice %}}

The [HtmlUnit driver](https://github.com/SeleniumHQ/htmlunit-driver) can download attachments by accessing them as input streams by implementing the [AttachmentHandler](https://htmlunit.sourceforge.io/apidocs/com/gargoylesoftware/htmlunit/attachment/AttachmentHandler.html) interface. The AttachmentHandler can the be added to the [HtmlUnit](https://htmlunit.sourceforge.io/) WebClient.
