# Implementaciones en IDE Pingüino

A continuación se detalla la información técnica recabada sobre la implementación de periféricos de hardware y gestión de software dentro del entorno **Pinguino IDE** para microcontroladores PIC.

## 1. Implementación de PWM (Pulse Width Modulation)
La modulación por ancho de pulsos en Pinguino se utiliza para simular salidas analógicas, controlar la velocidad de motores o atenuar LEDs.
* **Sintaxis principal:** Pinguino adopta la misma simplicidad que Arduino mediante la función `analogWrite(pin, valor)`.
* **Rango de valores:** El valor del ciclo de trabajo (duty cycle) generalmente va de **0 a 255** (para una resolución de 8 bits) o de **0 a 1023** (10 bits), dependiendo de la arquitectura del PIC utilizado.
* **Consideraciones de Hardware:** El PWM por hardware (módulo CCP/ECCP del PIC) solo está disponible en pines específicos marcados en el *pinout* del microcontrolador (usualmente pines que soportan funciones PWM nativas). Si se requiere en otros pines, debe implementarse por software.

## 2. Implementación de Timers
Los Timers son fundamentales para ejecutar tareas periódicas sin bloquear el flujo del programa (evitando el uso excesivo de la función `delay()`).
* **Temporización básica:** Se cuenta con las funciones estándar `millis()` y `micros()`, las cuales devuelven el tiempo transcurrido desde que el microcontrolador inició su ejecución.
* **Timers por Hardware (Interrupciones):** Los PICs cuentan con varios módulos de Timer (TMR0, TMR1, TMR2, etc.). En Pinguino, se pueden configurar usando macros o accediendo directamente a los registros del microcontrolador (ej. `T0CON`, `TMR0L`) si se requiere precisión absoluta o interrupciones de desbordamiento (Overflow Interrupts).
* **Uso típico:** Creación de rutinas de servicio de interrupción (ISR) para muestreo exacto o multiplexación.

## 3. Implementación de ADC (Convertidor Analógico-Digital)
El módulo ADC permite leer voltajes analógicos (como los provenientes de sensores de temperatura, luz, potenciómetros, etc.) y convertirlos en valores digitales.
* **Sintaxis principal:** Se utiliza la función `analogRead(pin)`.
* **Resolución:** En la mayoría de los microcontroladores PIC soportados por Pinguino (como el PIC18F2550), la resolución del ADC es de **10 bits**. Esto significa que un voltaje de 0V a 5V se mapea a valores enteros entre **0 y 1023**.
* **Pines analógicos:** Solo los pines con capacidad analógica (frecuentemente etiquetados como A0, A1, etc., o AN0, AN1 en el datasheet del PIC) pueden utilizar esta función.

## 4. Gestión de Librerías
Pinguino IDE soporta el uso de librerías para abstraer la complejidad de ciertos componentes (pantallas LCD, módulos I2C, tarjetas SD, etc.).
* **Librerías Core:** El IDE ya incluye librerías estándar listas para usarse. Se invocan al principio del código usando directivas de preprocesador de C, por ejemplo: `#include <lcd.h>` o `#include <Wire.h>`.
* **Librerías Externas/Propias:** Los usuarios pueden crear o importar sus propias librerías en C/C++ colocando los archivos `.c` y `.h` (o `.cpp`) en la carpeta `userlibs` o incluyéndolas en el mismo directorio del proyecto.
* **Ventaja:** Al estar basado en el compilador SDCC (para arquitecturas de 8 bits) o MIPS-GCC (para 32 bits), Pinguino es altamente compatible con el código estándar de C.
