# Espurna_Mqtt_Serial

- Se descargo el proyecto desde "https://github.com/xoseperez/espurna"
- Se modifico "espurna\code\espurna\config\arduino.h", para activar o desactivar opciones.

### Compilar el codigo (PlatformIO)
```
platformio -c clion run
```

### Compilar y Programar el microcontrolador (PlatformIO)
```
platformio -c clion run --target upload

o

pio run -t upload
```




### Permiso para acceder a ttyUSB0 en Linux
```
sudo chmod a+rw /dev/ttyUSB0
```



-------------------------------------------------------------------------------------------

# ESPURNA - 1.15.0-dev.git79157645.
## Se compila manualmente, ya que se requiere crear un perfil para hacerlo desde CLion, pero esto es temporal

### Compilar el codigo
```
Tools >> PlatformIO >> Build Production
```

### Borrar el microcontrolador
```
esptool --chip esp8266 --port COM10 erase_flash
```

### Programar el microcontrolador
```
esptool --chip esp8266 --port COM10 write_flash --flash_mode dio --flash_size detect 0x0 .pio/build/nodemcu-lolin/firmware.bin
```

En caso de no tener instalado **esptool**
```
pip install esptool
```
