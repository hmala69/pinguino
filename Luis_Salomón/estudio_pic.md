# Estudio de especificaciones del PIC y análisis de documentación oficial

## Objetivo de la actividad

El objetivo de esta actividad fue estudiar las especificaciones técnicas de microcontroladores PIC y analizar la documentación oficial del fabricante Microchip, con el fin de seleccionar un dispositivo adecuado para el desarrollo de una placa tipo Pinguino orientada al aprendizaje de programación y electrónica.

## Microcontroladores PIC analizados

Para el proyecto se revisaron principalmente los siguientes microcontroladores:

- PIC16F84A
- PIC16F877A
- PIC18F4550

Estos dispositivos pertenecen a la familia de microcontroladores PIC de Microchip y son utilizados comúnmente en proyectos educativos, sistemas embebidos y tarjetas de desarrollo.

## Análisis del PIC16F84A

El PIC16F84A es un microcontrolador de 8 bits muy utilizado en aplicaciones educativas por su arquitectura sencilla. Cuenta con memoria Flash, memoria RAM, memoria EEPROM y 13 pines de entrada/salida configurables. Según la documentación oficial de Microchip, este dispositivo tiene 68 bytes de RAM, 64 bytes de EEPROM y trabaja con un encapsulado de 18 pines. :contentReference[oaicite:0]{index=0}

Su principal ventaja es que es fácil de entender y programar, por lo que resulta útil para aprender conceptos básicos como manejo de puertos, entradas digitales, salidas digitales, temporizadores e interrupciones.

Sin embargo, para una placa de desarrollo más completa, el PIC16F84A tiene limitaciones importantes, ya que no cuenta con ADC interno, comunicación USB, PWM avanzado, SPI o I2C integrado.

## Análisis del PIC16F877A

El PIC16F877A es un microcontrolador más completo que el PIC16F84A. Es de 8 bits, cuenta con más memoria, más pines de entrada/salida y periféricos internos como ADC, temporizadores, comunicación serial, SPI e I2C. Microchip lo describe como un microcontrolador CMOS Flash de 8 bits, fácil de programar, con 35 instrucciones y ejecución de instrucciones de hasta 200 ns. :contentReference[oaicite:1]{index=1}

Este PIC es una mejor opción para proyectos educativos más avanzados, ya que permite trabajar con sensores analógicos, pantallas, comunicación serial y control de actuadores.

Para una placa de desarrollo, el PIC16F877A es una opción más completa porque permite conectar más módulos externos y trabajar con más prácticas de electrónica.

## Análisis del PIC18F4550

El PIC18F4550 es un microcontrolador más avanzado dentro de la familia PIC. Su característica más importante es que incluye comunicación USB 2.0, lo que permite crear tarjetas que se comuniquen directamente con una computadora. La documentación oficial de Microchip lo clasifica como un microcontrolador USB de alto rendimiento con tecnología nanoWatt. :contentReference[oaicite:2]{index=2}

Este microcontrolador es una opción fuerte para una placa tipo Pinguino, ya que puede funcionar como una tarjeta de desarrollo más moderna y con comunicación USB integrada. Esto facilita la programación, la comunicación con software de computadora y el desarrollo de proyectos más completos.

## Comparación general

| Característica | PIC16F84A | PIC16F877A | PIC18F4550 |
|---|---|---|---|
| Arquitectura | 8 bits | 8 bits | 8 bits |
| Uso principal | Aprendizaje básico | Proyectos intermedios | Proyectos avanzados con USB |
| Pines | 18 pines | 40/44 pines | 28/40/44 pines |
| ADC | No | Sí | Sí |
| USB | No | No | Sí |
| Comunicación serial | Limitada | Sí | Sí |
| Facilidad de aprendizaje | Alta | Media | Media |
| Recomendado para placa Pinguino | Básico | Bueno | Muy bueno |

## Conclusión

Después de revisar las especificaciones y la documentación oficial de Microchip, se concluye que el PIC16F84A es útil para aprender los fundamentos de programación de microcontroladores, pero resulta limitado para una placa de desarrollo moderna.

El PIC16F877A representa una mejor opción para prácticas educativas porque ofrece más pines, ADC y comunicación serial. Sin embargo, el PIC18F4550 es el más adecuado para el proyecto Pinguino, ya que integra comunicación USB, mayor capacidad y mejores posibilidades para crear una placa de desarrollo enfocada al aprendizaje.

Por esta razón, para continuar el proyecto se considera más conveniente trabajar con el PIC18F4550, ya que permite desarrollar una placa más completa, fácil de conectar a una computadora y con mayor potencial educativo.

## Referencias

- Microchip Technology. PIC16F84A Data Sheet.
- Microchip Technology. PIC16F87XA Data Sheet.
- Microchip Technology. PIC18F2455/2550/4455/4550 Data Sheet.
.
