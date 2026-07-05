# 🧪 Programas Demo para el IDE Pingüino

# 💡 1. Parpadeo de un LED (Blink)

 Consiste en encender y apagar un LED de forma repetitiva con un intervalo de tiempo determinado.

### Materiales

- 1 LED
- 1 Resistencia de 220 Ω
- Protoboard
- Cables de conexión

### ¿Cómo armarlo?

Conecta el ánodo del LED a un pin digital del microcontrolador mediante una resistencia de 220 Ω. El cátodo debe conectarse al pin GND de la placa.

### Funciones que demuestra

- Configuración de un pin como salida digital.
- Encendido y apagado de dispositivos electrónicos.
- Uso de retardos mediante la función `delay()`.
- Compilación y carga de un programa al microcontrolador.

---

# 🚦 2. Semáforo con tres LEDs

Este programa simula el funcionamiento de un semáforo controlando tres LEDs de diferentes colores mediante una secuencia de tiempos.

### Materiales

- 1 LED rojo
- 1 LED amarillo
- 1 LED verde
- 3 Resistencias de 220 Ω
- Protoboard
- Cables

### ¿Cómo armarlo?

Cada LED debe conectarse a un pin digital diferente utilizando una resistencia de 220 Ω. Los terminales negativos de los LEDs se conectan a tierra (GND).

### Funciones que demuestra

- Control de múltiples salidas digitales.
- Programación secuencial.
- Manejo de tiempos mediante retardos.
- Organización de procesos repetitivos.

---

# 🔘 3. Encender un LED con un botón

El LED únicamente permanecerá encendido mientras el usuario presione un pulsador.

### Materiales

- 1 LED
- 1 Pulsador
- 2 Resistencias
- Protoboard
- Cables

### ¿Cómo armarlo?

Conecta el LED a un pin de salida utilizando una resistencia. El pulsador debe conectarse a un pin de entrada digital junto con una resistencia pull-down o utilizando la resistencia pull-up interna del microcontrolador.

### Funciones que demuestra

- Lectura de entradas digitales.
- Control de salidas mediante condiciones.
- Uso de estructuras `if`.
- Interacción entre el usuario y el microcontrolador.

---

# 🔔 4. Activación de un buzzer

El programa activa y desactiva un buzzer para generar sonidos en diferentes intervalos de tiempo.

### Materiales

- 1 Buzzer activo
- Protoboard
- Cables

### ¿Cómo armarlo?

Conecta el terminal positivo del buzzer a un pin digital del microcontrolador y el terminal negativo a GND.

### Funciones que demuestra

- Activación de dispositivos externos.
- Manejo de salidas digitales.
- Control de tiempos.
- Generación de señales acústicas.

---

# 🌈 5. Efecto Knight Rider

En este proyecto varios LEDs se encienden uno tras otro simulando el efecto de iluminación utilizado en la serie *Knight Rider*.

### Materiales

- 6 u 8 LEDs
- Resistencias de 220 Ω
- Protoboard
- Cables

### ¿Cómo armarlo?

Cada LED debe conectarse a un pin digital diferente mediante una resistencia. Todos los cátodos se conectan a GND.

### Funciones que demuestra

- Control simultáneo de varias salidas.
- Uso de ciclos `for`.
- Programación de secuencias.
- Manejo de arreglos de pines.

---

# 🎲 6. Dado electrónico

Cada vez que se presiona un botón, el microcontrolador genera un número aleatorio representado mediante LEDs.

### Materiales

- 6 LEDs
- 1 Pulsador
- Resistencias
- Protoboard

### ¿Cómo armarlo?

Conecta cada LED a una salida digital y el botón a una entrada. El programa se encargará de encender la combinación correspondiente al número generado.

### Funciones que demuestra

- Generación de números aleatorios.
- Lectura de botones.
- Uso de estructuras condicionales.
- Control de múltiples LEDs.

---

# 🔢 7. Contador binario

Representa una cuenta en sistema binario utilizando varios LEDs.

### Materiales

- 8 LEDs
- Resistencias
- Protoboard
- Cables

### ¿Cómo armarlo?

Conecta cada LED a un pin digital diferente. Cada LED representará un bit del número binario generado por el programa.

### Funciones que demuestra

- Operaciones binarias.
- Incremento de variables.
- Manipulación de bits.
- Uso de ciclos repetitivos.

---

# 📺 8. Mensaje en una pantalla LCD

El programa muestra mensajes o información en una pantalla LCD de 16x2 caracteres.

### Materiales

- Pantalla LCD 16x2
- Potenciómetro de 10 kΩ (para el contraste)
- Protoboard
- Cables

### ¿Cómo armarlo?

Conecta la pantalla LCD siguiendo el modo de comunicación paralelo o mediante un módulo I2C, dependiendo del modelo disponible. El potenciómetro se utiliza para ajustar el contraste de la pantalla.

### Funciones que demuestra

- Comunicación con periféricos.
- Uso de librerías.
- Visualización de datos.
- Manejo de texto.

---

# ⏱️ 9. Cronómetro sencillo

Realiza el conteo del tiempo transcurrido mostrando el resultado mediante LEDs o una pantalla LCD.

### Materiales

- LEDs o pantalla LCD
- Pulsador
- Protoboard

### ¿Cómo armarlo?

Conecta el sistema de visualización elegido y un botón para iniciar o reiniciar el conteo del tiempo.

### Funciones que demuestra

- Uso de temporizadores.
- Contadores.
- Variables.
- Control mediante botones.

---

# 🎵 10. Reproducción de una melodía

El microcontrolador reproduce una pequeña secuencia de notas utilizando un buzzer pasivo.

### Materiales

- Buzzer pasivo
- Protoboard
- Cables

### ¿Cómo armarlo?

Conecta el buzzer a un pin digital capaz de generar señales PWM y a GND.

### Funciones que demuestra

- Generación de frecuencias.
- Uso de la función `tone()`.
- Temporización.
- Reproducción de secuencias musicales.
