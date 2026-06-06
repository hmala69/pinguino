# Elección del modelo de PIC más adecuado considerando costos y accesibilidad

## Objetivo

Elegir el microcontrolador PIC más adecuado para el proyecto de una placa de desarrollo tipo Pinguino, considerando costo, disponibilidad, facilidad de uso y características técnicas.

## Modelos comparados

Se analizaron tres modelos principales:

- PIC16F84A
- PIC16F877A
- PIC18F4550

## Análisis de costos y accesibilidad

El PIC16F84A es un microcontrolador sencillo y muy usado en educación. Tiene 18 pines, 13 entradas/salidas, memoria Flash de 1.75 kB, 68 bytes de SRAM y 64 bytes de EEPROM. Su ventaja es que es fácil de usar, pero actualmente resulta limitado para una placa de desarrollo moderna porque no cuenta con ADC ni USB integrado. :contentReference[oaicite:0]{index=0}

El PIC16F877A es más completo que el PIC16F84A, ya que pertenece a la familia PIC16F87XA de 28/40/44 pines y ofrece más entradas/salidas y periféricos internos. Es una buena opción educativa porque permite trabajar con sensores analógicos, comunicación serial y más módulos externos. :contentReference[oaicite:1]{index=1}

El PIC18F4550 es el modelo más adecuado para este proyecto porque incluye USB 2.0, 32 KB de memoria Flash, 2048 bytes de RAM y está pensado para aplicaciones más completas. Microchip lo mantiene con estado “In Production”, aunque también indica que existe un dispositivo más nuevo disponible, el PIC18F45K50. :contentReference[oaicite:2]{index=2}

En tiendas de componentes, el PIC18F4550 aparece disponible en versiones comerciales; por ejemplo, DigiKey México muestra el PIC18F4550-I/ML con precio unitario de aproximadamente 7.19 USD, y AElectronics México muestra el PIC18F4550-I/P en stock con precio de $269 MXN. :contentReference[oaicite:3]{index=3}

## Comparación general

| Modelo | Ventaja | Desventaja | Recomendación |
|---|---|---|---|
| PIC16F84A | Fácil de aprender | Muy limitado, sin ADC ni USB | Solo para prácticas básicas |
| PIC16F877A | Más pines y ADC | No tiene USB integrado | Bueno para aprendizaje general |
| PIC18F4550 | Tiene USB, más memoria y mejores periféricos | Puede ser un poco más caro | Mejor opción para la placa Pinguino |

## Modelo elegido

El modelo más adecuado para el proyecto es el **PIC18F4550**.

## Justificación

Se eligió el PIC18F4550 porque ofrece una mejor relación entre costo, accesibilidad y características técnicas. Aunque puede ser más caro que modelos básicos como el PIC16F84A, incluye USB integrado, mayor memoria y más capacidad para conectar sensores, pantallas, módulos de comunicación y otros periféricos.

Además, al tener USB, permite que la placa Pinguino pueda conectarse directamente a una computadora, lo cual facilita su uso como tarjeta de desarrollo educativa. Esto es importante porque el objetivo del proyecto es crear una placa accesible, útil para estudiantes y fácil de utilizar en comunidades pequeñas.

## Conclusión

Considerando precio, disponibilidad y características, el PIC18F4550 es la mejor opción para continuar el proyecto. El PIC16F84A es útil para aprender lo básico, y el PIC16F877A es una opción intermedia, pero el PIC18F4550 permite desarrollar una placa más completa y moderna.

Por lo tanto, el proyecto continuará tomando como base el microcontrolador **PIC18F4550**.
