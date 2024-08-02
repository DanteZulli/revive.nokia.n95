# Revive tu Nokia N95! (RM-159/RM-160/RM-320)

![Nokia N95](https://user-images.githubusercontent.com/27629528/111556514-1a841600-878b-11eb-8063-5d8cac57c0eb.jpg)

> Nota: Tanto el teléfono de la foto, como la base de este repositorio, son atribuídas a [@domib97](https://github.com/domib97)

### **_Descripción:_**

Este repositorio contiene una guía detallada de cómo revivir tu Nokia N95. El principal objetivo es proporcionar un paso a paso para actualizar el firmware, instalar aplicaciones y herramientas esenciales, y finalmente, hackear el sistema operativo Symbian S60 para evitar errores de firma. <br>
También deseo mantener viva la comunidad del N95, así que voy a usar este repositorio como un lugar para compartir aplicaciones, herramientas y recursos útiles, no solo para el desarrollo de aplicaciones, sino también para el uso diario del teléfono y disfrute del mismo.<br>
Las contribuciones son bienvenidas!

### **_Enlaces:_**

Documentación y lectura:
- https://en.wikipedia.org/wiki/Nokia_N95 (wiki)
- https://en.wikipedia.org/wiki/S60_(software_platform) (wiki)

Desarrollo:
- https://mrrosset.github.io/Symbian-Archive/index.html (SDKs)
- https://www.mediafire.com/folder/79jhy594xb3uk/Symbian_Development#79jhy594xb3uk (symbian dev tools)

Comunidad:
- https://www.gsmarena.com/nokia_n95-1716.php (still active community)
- https://www.reddit.com/r/symbian/ (reddit)

Apps:
- http://www.freeware-symbian.com (apps)
- https://de.phoneky.com/applications/?v=0#gsc.tab=0 (apps)

### **_Firmware:_**

Los últimos versiones de los firmwares para el Nokia N95 son:
- N95-1 (RM-159) : 35.0.002 ([link](https://www.frendx.com/firmware/download-nokia-n95-rm-159-v35-0-002-stock-firmware-flash-file/))
- N95-2 8GB (RM-320): 35.0.001 ([link](https://www.frendx.com/firmware/download-nokia-n95-rm-320-v35-0-001-stock-firmware-flash-file/))
- N95-3 (RM-160): 35.2.001 ([link](https://www.frendx.com/firmware/download-nokia-n95-3-rm-160-v35-2-001-stock-firmware-flash-file/))
- N95-4 8GB (RM-421) 35.2.002 ([link](https://www.frendx.com/firmware/download-nokia-n95-rm-421-v20-2-005-stock-firmware-flash-file/))

> Nota: Asegúrate de que el código de producto de tu teléfono coincida con el firmware que estás intentando instalar. Puedes encontrar el código de producto en la parte trasera de la batería, o con el teléfono mismo, marcando `*#0000#`. <br> Si los links de descarga no funcionan, puedes buscar en Google el firmware correspondiente a tu modelo (Aunque en este repositorio voy a adjuntar el firmware para el N95-3, la versión latinoamericana, que es la que yo pude comprobar que funciona).

### **_Prerrequisitos:_**

- Nokia N95 (RM-159/RM-160/RM-320 fueron los modelos en los que encontré reportes de éxito)
- Cable Mini-USB o computadora con conexión Bluetooth (Para enviarle archivos al teléfono)
- Phoenix Service Software ([link](https://mega.nz/file/tpkEVIhT) - Clave: fjsWdcfrlbc4wA3BLqB4H6MNm1Jvyvu0RlO6fLmdg0c - Contraseña: 1234)
- Némesis Service Suite ([link](https://archive.org/details/nemesis-service-nss))
- Una computadora con Windows XP/7/8/10/11 (Yo usé Windows 7, más abajo explico el por qué)

### **_Pasos para flashear el firmware más reciente:_**

> Aclaración: Yo realicé el flasheo del firmware con un Nokia N95-3 (RM-160) en Windows 7. El proceso puede ser similar con otros modelos, pero no puedo garantizarlo. Es prueba y error. Por si acaso, adjunto [acá](https://www.youtube.com/watch?v=BOEaSA_fgTw&t=213s) un video de [@Retrophonesstuff](https://www.youtube.com/@Retrophonesstuff) que detalla el mismo proceso (similar) pero con un Nokia N95-2 8GB (RM-320).

1. Si tenés información importante, respaldala con Nokia Suite. El instalador está ubicado en `/dev/Nokia_Suite_webinstaller_ALL.exe`. El flasheo del firmware va a borrar todo el contenido del teléfono.
2. Descargá Phoenix Service Software, **pausá la protección en tiempo real de tu antivirus**, descomprimilo (Contraseña: 1234) e instalalo.
3. Conectá tu Nokia N95 a la computadora mediante el cable USB (Modo PC Suite) y seleccioná en "Connections" el puerto COM correspondiente.
4. En File -> Open Product, seleccioná tu modelo de teléfono (RM-159, RM-160 o RM-320).
5. Colocá el firmware descargado en la carpeta `C:\Program Files (x86)\Nokia\Phoenix\Products\RM-159` (o la carpeta correspondiente a tu modelo).
6. En Flashing -> Firmware Update, seleccioná el firmware y hacé click en "Update Software".

> Notas sobre el flasheo (Paso 6):
> - Si Phoenix no logra detectar el teléfono, probá con otro cable USB o puerto USB, o instalando el Nokia Connectivity Cable Drivers (ubicado en `/dev/sdk/Connectivity_Cable_Driver.exe`).
> - Si te pasa como a mí, que el flasheo dispara una pantalla azúl de la muerte al intentar reconocer el dispositivo durante el proceso ([literalmente](/readme_images/bsod.jpg)) por checkeos de seguridad del Kernel con el modo de carga ADL, probá con una computadora con Windows 7, o con una versión más antigua de Windows 10. En mi caso, no pude flashear el teléfono con Windows 10 ni 11, pero sí con Windows 7 (Aclaración: en W7 tuve que instalar obligatoriamente el Nokia Suite, el Nokia Connectivity Cable Drivers y cancelar la revisión de de drivers vía Windows Update, en ese orden).
> - Si te encontrás con algún error durante el flasheo, y nada de lo anterior funciona, podés probar editando el código de producto del teléfono con Némesis Service Suite (NSS). En `/docs` adjunto algunos códigos útiles, aunque podés encontrarlos en internet. **¡Usá NSS con precaución! Solo cambiá el código del producto, y asegurate de que el nuevo sea compatible con tu modelo**







7. Hack S60 Symbian singing error with:
8. Norton Hack (for example)
    - copy folder "hack" to phone via usb
    - Set Date year to 2009
    - install NortonSymbianHack.sisx
    - Open Norton - options - quarantine - restore all
    - install RomPatcherPlus_3.1.sisx
    - open RomPatcher - tick both checkboxes - options - auto install for both
    - delete Norton from App-Man
    - reset date
9. install Py for S60
10. install x-plore (filemanager)
11. explore my "apps" folder for essential apps and tools
12. install SDK for programming your own apps in **C++ (native)**, **Java ME (native)**, **QT (native)**, **Python for S60 (PyS60)**
