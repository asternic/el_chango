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

### Como crear un destino en IssabelPBX?

En Configuración de PBX cree un *Destino Personalizado* con el siguiente contenido:

_chango,talk,1_

En descripción ponga _Chango_, y guarde los cambios.

Con eso tendrá dentro de Destinos Personalizados una entrada para poder derivar llamadas desde un IVR o desde cualquier otra aplicación de IssabelPBX.
