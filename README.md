# Proiect TSC
 ## Diagrama Bloc
 ![schema bloc](https://github.com/user-attachments/assets/080d4cf4-49cd-42ca-a2e4-edf26b8f4dea)

 ## Bill of Materials
 | Component       | Datasheet       | Link           |
 |-----------------|-----------------|----------------|
 | ESP32-C6-WROOM-1-N8 | - | https://www.snapeda.com/parts/ESP32-C6-WROOM-1-N8/Espressif+Systems/view-part/?ref=eda |
 | CPH3225A | - | https://www.snapeda.com/parts/CPH3225A/Seiko+Instruments/view-part/?ref=eda |
 | DS3231SN# | - | https://www.snapeda.com/parts/DS3231SN%23/Analog+Devices/view-part/?ref=eda |
 | MAX17048G+T10 | - | https://www.snapeda.com/parts/MAX17048G+T10/Analog+Devices/view-part/?ref=eda|
 | MBR0530 | - | https://www.snapeda.com/parts/MBR0530/Onsemi/view-part/?ref=eda |
 | PGB1010603MR | - | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda |
 | USBLC6-2SC6Y | - | https://www.snapeda.com/parts/USBLC6-2SC6Y/STMicroelectronics/view-part/?ref=eda |
 | W25Q512JVEIQ | - | https://www.snapeda.com/parts/W25Q512JVEIQ/Winbond+Electronics/view-part/?ref=eda |
 | 640-USB4110-GF-A | - | https://www.mouser.co.uk/ProductDetail/GCT/USB4110-GF-A?qs=KUoIvG%2F9IlYiZvIXQjyJeA%3D%3D |
 | PGB1010603MR | - | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=snap |
 | BUTTONS | - | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k |
 | C (1-10) | - | https://componentsearchengine.com/part-view/CC0402MRX5R5BB106/YAGEO |
 | LED | - | https://www.snapeda.com/parts/KP-1608SURCK/Kingbright/view-part/?ref=search&t=LED%200603 |
 | D (1-12) | - | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda |
 | R (1-15) | - | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL)/YAGEO |
 | Test Pads | - | - |
   
## Funcționalitate hardware
### Alimentare și încărcare
Conector USB + MCP73831: Permite încărcarea unei baterii LiPo prin USB.

LDO (ME6211 sau similar): Reglează tensiunea la 3.3V pentru alimentarea circuitului digital.

Condensatori de decuplare: Plasați strategic pentru stabilizarea alimentării.

### ESP32-C6
Modul WiFi/BLE cu capabilități de conectare și procesare date.

Flash: 4MB / RAM: 512KB.

GPIO multiple folosite pentru comunicații (SPI, I2C) și control periferice.

### E-Ink Display
Controlat prin SPI.

GPIO-uri adiționale pentru semnale de control (busy, reset).

### Protecții
Diodă Schottky (ex: MBR0530) pentru protecție polaritate inversă.

PTC resetabil pentru protecție curent.

### EEPROM / MEMS
EEPROM pentru păstrarea datelor între cicluri de alimentare (presupus U3).

MAX17048 pentru monitorizarea nivelului bateriei (comunicare I2C).

| Pin ESP32-C6 |	Funcție hardware |
|-------------|------------------|
| IO0 |	GPIO / Boot	|
| IO1 |	UART TX |
| IO2 |	UART RX	|
| IO3 |	GPIO	|
| IO4 | GPIO	|
| IO5 |	GPIO	|
| IO6 |	GPIO	|
| IO7 |	GPIO	|
| IO8 |	GPIO	|
| IO9 |	SPI Flash – IO2 |
| IO10 | 	SPI Flash – IO3 |
| IO11 |	SPI Flash – SCK |
| IO12 |	SPI Flash – CS |
| IO13 |	SPI Flash – IO1 |
| IO14 |	SPI Flash – IO0 |
| IO15 |	I2C SDA |
| IO16 |	I2C SCL |
| IO17 |	SPI Display – DC |
| IO18 |	SPI Display – RST |
| IO19 |	SPI Display – CS |
| IO20 |	SPI Display – CLK |
| IO21 |	SPI Display – MOSI |
| IO22 |	SPI Display – BUSY |
| IO23 |	SPI ESD / Qwiic |
