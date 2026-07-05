# 🛠️ Integración: Ensamblaje de Componentes

## 📋 Objetivo
Realizar la integración física y el ensamblaje de los componentes electrónicos sobre la placa de circuito impreso (PCB) del **Proyecto Pingüino**, aplicando técnicas adecuadas de soldadura y verificando la correcta alimentación y funcionamiento del circuito regulador y del microcontrolador.

## 🧰 Lista de Materiales

A continuación se detalla el listado del material requerido para el proyecto:

<div align="center">

| Concepto / Componente | Cantidad | Función Principal en la Placa |
| :--- | :---: | :--- |
| **Placa PCB** | 1 | Sustrato y pistas del circuito |
| **Cristal de Cuarzo de 20 MHz** | 2 | Reloj oscilador del microcontrolador |
| **Capacitor Cerámico 22 pF** | 4 | Desacoplo para el cristal oscilador |
| **Capacitor Cerámico 101 (100 pF)** | 6 | Filtrado de ruido de alta frecuencia |
| **Capacitor Electrolítico 0.22 µF** | 2 | Estabilización a la entrada/salida |
| **Capacitor Electrolítico 3.3 µF** | 2 | Filtrado general |
| **Capacitor Electrolítico 10 µF** | 2 | Filtrado en la etapa de regulación |
| **Regulador de Voltaje L7805** | 2 | Regulación de alimentación a 5V DC |
| **Puerto de Alimentación (Jack DC)** | 2 | Entrada de voltaje externo (7V - 12V) |
| **Puerto USB** | 2 | Conexión de datos/carga con la PC |
| **Resistencia de 220 Ω** | 2 | Limitadora de corriente para LEDs |
| **Resistencia de 10 kΩ** | 2 | Resistencia Pull-Up para botón Reset |
| **Luz LED** | 2 | Indicadores de encendido (PWR/Test) |
| **Botón Pulsador (Push button)** | 2 | Botón de Reset / Modo Bootloader |
| **Interruptor (Switch)** | 2 | Encendido y apagado general |
| **Borneras o Conectores** | 4 | Interfaz para entradas y salidas |
| **Tubo de Soldadura de Estaño** | 1 | Insumo de soldadura |
| **Pasta para Soldar (Flux)** | 1 | Mejorar adherencia y disipación térmica |

</div>

## ⚙️ Metodología de Ensamblaje

Para garantizar una soldadura limpia y evitar dañar los componentes térmicamente sensibles, se siguió el principio de **montaje por perfil de altura (de menor a mayor tamaño)**:

- [x] **Fase 1: Preparación e Inspección**
  - **1.** Limpieza profunda de las pistas de la PCB con alcohol isopropílico para eliminar grasa o residuos de polvo.
  - **2.** Aplicación precisa de la pasta para soldar (*flux*) en los pads para mejorar la distribución de calor.

- [x] **Fase 2: Componentes de Perfil Bajo**
  - **1.** Soldadura de las resistencias de precisión ($220\,\Omega$ y $10\,\text{k}\Omega$).
  - **2.** Instalación del cristal de cuarzo de $20\,\text{MHz}$ junto a sus dos capacitores cerámicos de acoplo de $22\,\text{pF}$.
  - **3.** Colocación de los capacitores cerámicos restantes de alta frecuencia ($100\,\text{pF}$).

- [x] **Fase 3: Componentes de Perfil Medio**
  - **1.** Montaje e inserción de los botones pulsadores (*Push buttons*) y el interruptor general (*Switch*).
  - **2.** Soldadura del zócalo (base) de protección para el microcontrolador PIC, evitando soldar el chip directamente.
  - **3.** Alineación e instalación de los LEDs indicadores respetando estrictamente su polaridad (ánodo/cátodo).

- [x] **Fase 4: Componentes de Mayor Volumen**
  - **1.** Soldadura de los capacitores electrolíticos, verificando la orientación correcta de la banda del polo negativo.
  - **2.** Montaje y fijación del regulador de voltaje **L7805**.
  - **3.** Soldadura de los conectores robustos: Jack de alimentación externa, Puerto USB y las Borneras de conexión.

## 📸 Evidencia Visual (Antes vs. Después)

### Placa sin ensamblar (Antes)
<p align="center">
  <img src="ruta/a/tu/imagen_antes.jpg" alt="PCB sin ensamblar" width="600"/>
  <br>
  <em>Figura 1: PCB fabricada antes de la colocación de componentes.</em>
</p>

### Placa terminada (Después)
<p align="center">
  <img src="ruta/a/tu/imagen_despues.jpg" alt="PCB ensamblada" width="600"/>
  <br>
  <em>Figura 2: Ensamblaje finalizado con todos los componentes soldados.</em>
</p>

## 🔍 Pruebas de Calidad y Continuidad

Una vez culminada la soldadura, se realizaron las siguientes verificaciones antes de insertar el microcontrolador PIC:

1. **Prueba en frío (Multímetro en continuidad):** Se verificó la ausencia de cortocircuitos entre las pistas de alimentación ($V_{CC}$ / $5\text{V}$) y Tierra ($\text{GND}$).
2. **Inspección visual:** Se revisó que los puntos de soldadura tuvieran forma cónica brillante, descartando soldaduras frías o puentes de estaño entre pines cercanos.
3. **Prueba de voltaje en caliente:** Se suministró alimentación al Jack DC y se midió la salida del regulador **L7805**, comprobando una entrega estable de $5\text{V}$ y el encendido del LED indicador de poder.

## ✅ Conclusión
El ensamblaje físico de la placa **Pingüino** se completó satisfactoriamente. La distribución por alturas facilitó el proceso de soldadura y las pruebas eléctricas confirmaron que la etapa de alimentación y filtrado opera dentro de los parámetros esperados, dejando el hardware listo para la inserción del microcontrolador y las pruebas de programación/bootloader.
