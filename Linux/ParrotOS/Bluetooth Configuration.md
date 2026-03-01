El primer paso es verificar que el servicio se encuentre activo:
```bash
sudo systemctl status bluetooth
```

En caso de que no este activo ejecutar los siguientes commandos:
```bash
sudo systemctl enable bluetooth
sudo systemctl start bluetooth
```

Una ves el servicio de el Bluetooth ya este activo ejecutar el siguiente commando para habilitar el prompt interactivo de el Bluetooth:
```bash
bluetoothctl
```

Ejecutar los siguientes commandos posteriormente:
```bash
power on
agent on
default-agent
scan on
```

El comando de `scan on` comenzara con el escaneo de dispositivos mostrando sus MAC addresses. Una ves encontrada la MAC address del dispositivo al que uno se quiera conecta ejecutar los siguientes commandos: 
```bash
pair AA:BB:CC:DD:EE:FF
trust AA:BB:CC:DD:EE:FF
connect AA:BB:CC:DD:EE:FF
```

Posterior a eso:
```bash
scan off  
exit
```

