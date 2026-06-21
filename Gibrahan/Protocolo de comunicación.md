### Protocolos de Comunicación

* ### Comunicación USB (Universal Serial Bus) Nativa:
El microcontrolador PIC integra un módulo de comunicación USB nativo, permitiendo la conexión directa con la computadora sin requerir circuitos de conversión externos. Este entorno soporta la Clase CDC (emulación de puerto serie virtual) para transmisión de datos, la Clase HID para el reconocimiento automático del hardware sin instalación de controladores, y transferencias masivas (Bulk Transfers) para bloques de datos de alta velocidad.

* ### Protocolo UART (Comunicación Serial Asíncrona):
Implementado para garantizar la interconexión de la tarjeta de desarrollo con módulos de expansión industriales y de automatización (como GPS, GSM o Bluetooth). Utiliza líneas independientes de transmisión (TX) y recepción (RX), operando de manera asíncrona mediante la configuración de velocidades de transmisión (Baud rate) estandarizadas.

* ### Protocolos Síncronos para Periféricos (I2C y SPI):
Habilitados en el hardware para facilitar la integración de un banco de pruebas con diversos sensores y actuadores. Se dispone del bus I2C (líneas SDA y SCL) para la conexión de múltiples dispositivos mediante direccionamiento en el mismo canal, y el protocolo SPI de cuatro hilos (MOSI, MISO, SCK, CS) diseñado para periféricos que exigen una alta tasa de transferencia de datos, como módulos de memoria SD o pantallas de interfaz.
