# PYnty-Mac - Hackintosh-Gigabyte-Z390-I-Aorus-Pro-Wifi
Esta es una guia para construir un hackintosh con una placa madre Gigabyte z390 I Aorus pro wifi, es el formato mini itx.

Esta es mi tercera build. Me alegro de que funcione bien, al principio, pensé en la adquisición de la i9-9900K o el i7-8700K. Pero, primero quería empezar con el i7-8700, y, luego actualizarlo como la placa base me permite.

> Actualizacion 04/01/2021: Incorpore una tarjeta de video AMD RADEON VEGA 56 Asrock Panthom Gaming funciono de maravilla, plug and play, tambien incorpore una disco nvme ssd wd blue de 1tb en la ranura detras del la placa madre, mantuve Mojave porque no tenia necesidad de actualizar
 
> Actualizacion 21/11/2022: Realice la actualizacion a Ventura v 13.0.1, funciono todo impecable, hice una instalacion limpia, es decir formatie primero el nvme samsung y luego instale ventura, no utlice clover utilice opencore, en la documentacion de opencore esta muy bien explicado el proceso y los problemas que puedan surgir

![Mi iMac](images/build.jpeg)

### Hardware que utilice
- Phanteks Enthoo Evolv ITX Tempered Glass
- Gigabyte Z390 I AORUS PRO WIFI Motherboard
- Intel Core i7-8700 Processor
- Corsair Vengeance Pack 32GB (2 x 16GB) DDR4 3000
- SAPPHIRE PULSE Radeon RX 580 8GB
- SAMSUNG 970 EVO M.2 2280 250GB SSD
- EVGA SuperNOVA 750 B1, 80+ BRONZE 750W, Semi Modular
- CORSAIR Hydro Series H100i v2 AIO Liquid CPU Cooler, 240mm
- Crucial MX500 250GB 3D NAND SATA 2.5 Inch Internal SSD

### Lo que funciona
- Aceleracion Grafica con RX 580, que es compatible de forma nativa.
- Intel UHD 630 (Aceleracion Grafica)
- Ethernet integrado
- Audio integrado
- Suspencion, Reactivación, reinicio y apagado. Despertar de la suspencion requiere una pulsación de una tecla.
- Quick Look y Vista Previa
- iMessage, FaceTime, App Store, ICloud, iTunes.
- TRIM está habilitado en NVMe Samsung sin parches (puedes ver las velocidades en la imagen a continuación realizadas con BlackmagicDesign)

![resultados nvme](images/nvme.jpg)

### Lo que no funciona
- Wifi y Bluetooth integrado (Esto no funciona de forma nativa, ya que Gigabyte incorporo el nuevo módulo WIFI con CVNi, cuando Apple lo actualice en sus nuevos MacBooks, seguramente aparecera un adaptador compatible para que podamos incorporar una placa Broadcom.)
- Handoff, Continuity, AirDrop: Estos no funcionan porque WiFi y Bluetooth son necesarios.

### Instrucciones paso por paso
Ver la seccion [instrucciones.md](instrucciones.md)

### Pruebas de Rendimiento (Benchmark)
Ver la seccion [benchmarks.md](benchmarks.md)

### Mapeo USB
El mapeo lo limite a 15 puertos usb, los usb 3.0 funcionan espectacular. Creo que fue la forma mas eficiente para deshacerme de las actualizaciones interminables del "parche de límite de puerto USB" cada vez que MacOS se actualiza. Ver la seccion [Mapeo_Puertos_USB.md](Mapeo_Puertos_USB.md) para más detalles.

### Importante
Eres bienvenido a utilizar mi carpeta EFI. Sin embargo, asegurate de cambiar los siguientes datos en tu config.plist con Clover Configurator:
- SerialNumber
- BoardSerialNumber
- SmUUID

(Al editar config.plist debes cambiar los valores mencionados anteriormente ya que estan vacios, si utilizas clover configurator puedes crearlos aleatoriamente)
