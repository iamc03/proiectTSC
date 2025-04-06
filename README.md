## Descriere functionalitati hardware
**ESP32-C6**
Microcontroller-ul principal controlează toate componentele. Oferă conectivitate WiFi și BLE, GPIO-uri multiple, și interfețe I2C/SPI/UART.

**Memorie externă - W25Q512**
Interfață: SPI
Conectare la ESP: GPIO19 (CLK), GPIO20 (MISO), GPIO21 (MOSI), GPIO17 (CS)
Rol: memorie externă pentru stocare cod/config.

**Senzor baterie MAX17048**
Interfață: I2C
Conectare la ESP: GPIO3 (SDA), GPIO4 (SCL)
Funcție: monitorizare nivel baterie

**Expander GPIO - TCA9539**
Interfață: I2C
Adresă configurabilă: pin A0, A1
Funcție: extindere I/O (butoane, LED-uri)
Conectare la ESP: I2C comun (GPIO3, GPIO4)
