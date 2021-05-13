# El Chango

Bot conversacional para Asterisk para hacerles perder el tiempo a los telemarketers, y de paso divertirse un poco.

Esta es una versión Codobesa de "Lenny", un contexto de marcado para Asterisk y un conjunto de sonidos para transferir
a los telemarketers y que pierdan su tiempo conversando con el bot. De paso grabamos la llamada para ver que tal resulta.

## Instalación

Descargue o clone el repositorio y mueva el directorio *chango* dentro de /var/lib/asterisk/sounds

```
mv chango /var/lib/asterisk/sounds
```

Luego concatene el contenido de extensions_custom.conf dentro de /etc/asterisk/etensions_custom.conf (si utiliza IssabelPBX o
compatible).

```
cat extensions_custom.conf >>/etc/asterisk/extensions_custom.conf
```

## Integración con IssabelPBX


### Destino Personalizado

En Configuración de PBX cree un *Destino Personalizado* con el siguiente contenido:

_chango,talk,1_

En descripción ponga _Chango_, y guarde los cambios.

Con eso tendrá dentro de Destinos Personalizados una entrada para poder derivar llamadas desde un IVR o desde cualquier otra aplicación de IssabelPBX.

### Extensión Virtual

Luego puede crear una extensión virtual para poder transferir llamadas o marcar directamente la extensión para conversar con el Chango

En Extensiones elija *Añadir Extensión* y de la lista desplegable elija "Ninguno (extensión virtual)"

Complete un número de extensión, en el nombre ponga El Chango y finalmente al final del formulario en *Destinos Opcionales* complete a todos ellos como "Destinos Personalizados", *Chango*

Guarde y aplique cambios. Ya podrá marcar esa nueva extensión para conversar con él.
