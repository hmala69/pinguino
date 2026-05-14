### ¿Qué es la tarjeta de desarrollo Pinguino?
El Proyecto Pinguino es una plataforma de hardware y software de código abierto (open-source) para la creación de prototipos electrónicos. Nació como una alternativa inspirada en la filosofía de Arduino, pero con una diferencia fundamental: utiliza microcontroladores PIC de la empresa Microchip Technology en lugar de los microcontroladores AVR de Atmel que usa tradicionalmente Arduino.

### Características Principales.
Microcontrolador: Originalmente está basada en el PIC18F2550 (de 8 bits), aunque las versiones más recientes (Pinguino 32) soportan microcontroladores de 32 bits de la familia PIC32 (como el PIC32MX250F128B).

### USB Nativo.
Es una de sus mayores ventajas. El microcontrolador PIC18F2550 tiene un módulo USB integrado. Esto significa que la tarjeta Pinguino no requiere un chip conversor externo (como el FTDI que usan muchas placas Arduino) para comunicarse con la computadora, lo que reduce costos y simplifica el diseño.

### Entorno de Desarrollo (IDE).
Cuenta con su propio IDE (Entorno de Desarrollo Integrado) que es multiplataforma (funciona en Windows, Linux y macOS). El IDE está escrito en Python y utiliza el compilador SDCC (Small Device C Compiler) para compilar el código.

### Lenguaje de Programación.
Se programa utilizando el lenguaje C/C++, con una sintaxis y librerías que son extremadamente similares a las de Arduino, lo que facilita mucho la transición si ya se conoce ese entorno.

### Hardware "Hazlo tú mismo" (DIY).
El diseño de la placa Pinguino de 8 bits está pensado para que cualquier estudiante o aficionado pueda fabricarla en casa utilizando una placa fenólica de una sola cara y componentes "Through-Hole" (de inserción), lo que la hace muy accesible.

### Principales diferencias con Arduino
Arquitectura: Pinguino usa arquitectura PIC, mientras que Arduino clásico usa AVR.

### Costo de ensamble.
Al no necesitar un chip adaptador de USB a Serial, armar una placa Pinguino desde cero suele ser más económico.

### Longitud de código.
En algunos casos, el código compilado (el archivo .hex) generado por SDCC para Pinguino puede ser un poco más pequeño y optimizado para el PIC en comparación con ciertas librerías estándar de Arduino.

### Aplicaciones.
Al igual que otras tarjetas de desarrollo, Pinguino es ideal para:

*Proyectos académicos de electrónica y programación.

*Robótica educativa (control de motores, lectura de sensores).

*Sistemas de adquisición de datos para computadoras (aprovechando su puerto USB nativo).

*Domótica y automatización de bajo costo.
