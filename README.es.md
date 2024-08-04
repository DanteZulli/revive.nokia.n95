# Revive tu Nokia N95 ![Nokia](https://img.shields.io/badge/Nokia-%23124191.svg?style=for-the-badge&logo=nokia&logoColor=white)

Revive tu viejo S60v3 FP1 Symbian Nokia N95 (RM-159/RM-160/RM-320) con esta guía del _~~2021~~_ 2024!

[![Read in English](https://img.shields.io/badge/Read%20in-English-red)](README.md)
[![Leer en Español](https://img.shields.io/badge/Leer%20en-Español-yellow)](README.es.md)

![Nokia N95](https://user-images.githubusercontent.com/27629528/111556514-1a841600-878b-11eb-8063-5d8cac57c0eb.jpg)

> Tanto el teléfono de la foto, como la base de este repositorio, son atribuídas a [@domib97](https://github.com/domib97)

### **_Descripción:_**

Este repositorio contiene una guía detallada de cómo revivir tu Nokia N95. El principal objetivo es proporcionar un paso a paso para actualizar el firmware, instalar aplicaciones y herramientas esenciales, y finalmente, hackear el sistema operativo Symbian S60 para evitar errores de firma. <br>
También deseo mantener viva la comunidad del N95, así que voy a usar este lugar para compartir aplicaciones, herramientas y recursos útiles, no solo para el desarrollo de aplicaciones, sino también para el uso diario del teléfono y disfrute del mismo.<br>
Las contribuciones son bienvenidas!

> [!WARNING]
> No puedo garantizar que los links provistos en este repositorio estén siempre disponibles (ya son cosas bastante viejas). De todas formas voy a intentar que los componentes escenciales, tanto para el flasheo del firmware como para el hackeo del sistema operativo, están adjuntos en el repositorio.

### **_Enlaces:_**

Documentación y lectura:
- https://en.wikipedia.org/wiki/Nokia_N95 (wiki)
- https://en.wikipedia.org/wiki/S60_(software_platform) (wiki)
- http://www.allaboutsymbian.com/ (noticias/foro)

Desarrollo:
- https://mrrosset.github.io/Symbian-Archive/index.html (SDKs)
- https://www.mediafire.com/folder/79jhy594xb3uk/Symbian_Development#79jhy594xb3uk (symbian dev tools)

Comunidad:
- https://www.gsmarena.com/nokia_n95-1716.php (comunidad aún activa)
- https://www.reddit.com/r/symbian/ (comunidad Symbian)
- https://www.reddit.com/r/ngage/ (comunidad N-Gage)

Apps:
- http://www.freeware-symbian.com (apps)
- https://de.phoneky.com/applications/?v=0#gsc.tab=0 (apps)
- https://archive.org/download/symbian-games (juegos)
- https://archive.org/details/nokia-n-gage-the-force-unleashed-2008 (juegos)

Otros:
- http://m.opera.com/?region&act=lp&tag=mini5s60&vid=0x9c7f9c859a2dd90a&cert=all&ua=NokiaN95 (Opera Mini)

### **_Firmware:_**

Las últimas versiones de los firmwares para el Nokia N95 son:
- N95-1 (RM-159) : 35.0.002 ([link](https://www.frendx.com/firmware/download-nokia-n95-rm-159-v35-0-002-stock-firmware-flash-file/))
- N95-2 8GB (RM-320): 35.0.001 ([link](https://www.frendx.com/firmware/download-nokia-n95-rm-320-v35-0-001-stock-firmware-flash-file/))
- N95-3 (RM-160): 35.2.001 ([link](https://www.frendx.com/firmware/download-nokia-n95-3-rm-160-v35-2-001-stock-firmware-flash-file/))
- N95-4 8GB (RM-421) 35.2.002 ([link](https://www.frendx.com/firmware/download-nokia-n95-rm-421-v20-2-005-stock-firmware-flash-file/))

> [!CAUTION]
> Asegúrate de que el código de tu teléfono coincida con el del firmware que estás intentando instalar. Puedes encontrar el código de producto en la parte trasera, debajo de la batería, o con el teléfono mismo, marcando `*#0000#`. <br> Si los links de descarga no funcionan, puedes buscar en Google el firmware correspondiente a tu modelo.

### **_Prerrequisitos:_**

- Nokia N95 (RM-159/RM-160/RM-320 fueron los modelos en los que encontré reportes de éxito)
- Cable Mini-USB o computadora con conexión Bluetooth (Para enviarle archivos al teléfono)
- Phoenix Service Software ([link](https://mega.nz/file/tpkEVIhT) - Clave: fjsWdcfrlbc4wA3BLqB4H6MNm1Jvyvu0RlO6fLmdg0c - Contraseña: 1234)
- Némesis Service Suite ([link](https://archive.org/details/nemesis-service-nss))
- Una computadora con Windows XP/7/8/10/11

### **_Pasos para flashear el firmware más reciente:_**

> [!NOTE]
> Yo realicé el flasheo del firmware con un Nokia N95-3 (RM-160) en Windows 7. El proceso puede ser similar con otros modelos, pero no puedo garantizarlo. Es prueba y error. Por si acaso, adjunto [acá](https://www.youtube.com/watch?v=BOEaSA_fgTw&t=213s) un video de [@Retrophonesstuff](https://www.youtube.com/@Retrophonesstuff) que detalla el mismo proceso (similar) pero con un Nokia N95-2 8GB (RM-320).

1. Si tenés información importante, respaldala con Nokia Suite. El instalador está ubicado en `/dev/Nokia_Suite_webinstaller_ALL.exe`. El flasheo del firmware va a borrar todo el contenido del teléfono.
2. Descargá Phoenix Service Software, **pausá la protección en tiempo real de tu antivirus**, descomprimilo (Contraseña: 1234) e instalalo.
3. Conectá tu Nokia N95 a la computadora mediante el cable USB (Modo PC Suite) y seleccioná en "Connections" el puerto COM correspondiente.
4. En File -> Open Product, seleccioná tu modelo de teléfono (RM-159, RM-160 o RM-320).
5. Colocá el firmware descargado en la carpeta `C:\Program Files (x86)\Nokia\Phoenix\Products\RM-159` (o la carpeta correspondiente a tu modelo).
6. En Flashing -> Firmware Update, seleccioná el firmware y hacé click en "Update Software".

> [!NOTE]
> Notas sobre el flasheo (Paso 6):
> - Si Phoenix no logra detectar el teléfono, probá con otro cable USB o puerto USB, o instalando el Nokia Connectivity Cable Drivers (ubicado en `/dev/sdk/Connectivity_Cable_Driver.exe`).
> - Si te pasa como a mí, que el flasheo dispara una pantalla azul de la muerte al intentar reconocer el dispositivo durante el proceso ([literalmente](/images/bsod.jpg)) por chequeos de seguridad del Kernel con el modo de carga ADL, probá con una computadora con Windows 7, o con una versión más antigua de Windows 10. En mi caso, no pude flashear el teléfono con Windows 10 ni 11, pero sí con Windows 7 (Aclaración: en W7 tuve que instalar obligatoriamente el Nokia Suite, el Nokia Connectivity Cable Drivers y cancelar la revisión de de drivers vía Windows Update, en ese orden).
> - Si te encontrás con algún error durante el flasheo, y nada de lo anterior funciona, podés probar editando el código de producto del teléfono con Némesis Service Suite (NSS). En `/docs` adjunto algunos códigos útiles, aunque podés encontrarlos en internet. **¡Usá NSS con precaución! Solo cambiá el código del producto, y asegurate de que el nuevo sea compatible con tu modelo** ([imagen de muestra](/images/nss.png))



### **_Pasos para hackear S60 Symbian V3:_**

Para evitar errores de firma y poder instalar aplicaciones no firmadas, es necesario hackear el sistema operativo.

> [!WARNING]
> No todos los métodos de hackeo funcionan para todos los modelos de Nokia N95, ni tampoco para todas las versiones de firmware, así que voy a detallar varios métodos que podés probar:


#### **_Método 1 (Norton Hack):_**

**Video tutorial**: [link](https://www.youtube.com/watch?v=rttethei6xg)<br>
Créditos a [@tsle805](https://www.youtube.com/@tsle805)

1. Descargá los archivos necesarios de `/norton_hack` y copialos a tu teléfono mediante USB/Bluetooth.
2. Cambiá la fecha del teléfono a 2009.
3. Instalá `NortonSymbianHack.sisx`.
4. Abrí Norton -> Options -> Antivirus -> Quarantine -> Restore All.
5. Instalá `RomPatcherPlus_3.1.sisx`.
6. Abrí RomPatcher -> Tildá ambas opciones.
7. Eliminá Norton desde el Administrador de Aplicaciones.
8. Restaurá la fecha del teléfono.

#### **_Método 2 (Mobile Security Hack):_**

**Video tutorial**: [link](https://www.youtube.com/watch?v=UJJICzbk3TA)<br>
Créditos a [@Mr_symbian](https://www.youtube.com/@Mr_symbian)

1. Hacé un hard reset al teléfono (opcional) marcando `*#7370#` (Código: 12345).
2. En el teléfono (Settings > Applications > App. Manager), asegurate que el apartado de "Software Installation" se encuentre en "All".
3. Cambiá la fecha del teléfono a 01/01/2012.
4. Descargá los archivos necesarios de `/mobile_security_hack` y copialos a tu teléfono mediante USB/Bluetooth.
5. Instalá `x-plore v1.30.sisx`.
6. Abrí X-Plore y navegá hasta la carpeta donde copiaste los archivos (Files).
7. Abrí el tmquarantine.zip y extraé la carpeta tmquarantine a `C:\`.
8. Instalá `mobile-security.sisx`. Cuando te solicite reiniciar, no lo hagas.
9. Abrí mobile-security, poné "Yes" al primer mensaje.
10. Seleccioná Options -> Antivirus -> Quarantine list -> Options -> Mark -> Mark all -> Options -> Restore -> Yes.
11. Abrí X-Plore y navegá hasta la carpeta donde copiaste los archivos (Files).
12. Instalá `RomPatcherPlus_3.1_LiteVersion.sisx` o alguna versión alternativa si esa no funciona.
13. Abrí RomPatcher -> Tildá ambas opciones.
14. Abrí X-Plore, Tools -> Configuration -> Marcá las 4 opciones; "Show hidden files", "Show ROM drives", "Show RAM drives" y "Show system files/folders".
15. Abrí la carpeta Hacker69 y elegí la carpeta de acuerdo a tu modelo de teléfono.
16. Copiá el archivo `installserver.exe` a `C:\sys\bin`.
17. Eliminá Mobile Security desde el Administrador de Aplicaciones.

#### **_Alternativas:_**

Si los métodos anteriores no funcionan, podés probar con alguna aplicación para "firmar" aplicaciones. A mí no me funcionaron, pero dejé los archivos en `/signing_apps` por si querés probarlos.
