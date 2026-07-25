#  Guía Rápida: Bootloader en PIC18F4550

> 📌 **Objetivo:** Preparar el microcontrolador **PIC18F4550** para que pueda ser programado directamente desde **Pinguino IDE** mediante un cable USB, eliminando la necesidad de utilizar un programador externo para futuras cargas de código.

---

## 🛠️ Requisitos Previos

| Categoría | Elemento Requerido | Detalle / Especificación |
| :--- | :--- | :--- |
| **Hardware** | 🔌 **Programador Universal** | Familia TL866II Plus, T48 o T56. |
| **Hardware** | 🧩 **Microcontrolador** | PIC18F4550 en encapsulado DIP40. |
| **Software** | 💻 **Software Xgpro / XGecu Pro** | Instalado y ejecutándose con permisos de administrador. |
| **Firmware** | 📦 **Archivo `.hex`** | Bootloader de Pinguino correspondiente a tu cristal. |

---

## 🔌 Fase 1: Preparación del Hardware y Entorno

* [ ] **Conexión física:** Conecta el programador universal a tu computadora mediante el cable USB.
* [ ] **Posición del chip:** Coloca el **PIC18F4550** dentro del zócalo ZIF (DIP40), asegurándote de alinear correctamente el **Pin 1** (fíjate en la palanca y el esquema de la herramienta).
* [ ] **Apertura de la herramienta:** Abre el programa desde tu escritorio haciendo doble clic en el icono correspondiente.

> 🖼️ **IMAGEN 1: XGPRO**
> *Software.*
![Accesos directos de Xgpro](https://github.com/hmala69/pinguino/blob/51e7c8426065f54bf366de2e933b743c5ab7ab1a/Gibrahan/Project_images/Xgpro.jpeg)

---

## 📁 Fase 2: Selección del Firmware (`.hex`)

> ⚠️ **PUNTO CRÍTICO:** El repositorio contiene múltiples versiones. Debes elegir obligatoriamente la que coincida con la **frecuencia en MHz del cristal de cuarzo físico** soldado en tu placa pinguino.

* [ ] **Iniciar carga:** En el menú superior del software Xgpro, presiona el botón **`LOAD`** (Cargar).
* [ ] **Ubicar directorio:** Abre la carpeta donde descargaste los archivos del Bootloader.
* [ ] **Seleccionar el archivo correcto:**
  * 🔸 *Si tu circuito usa cristal de 20 MHz* ➡️ `Bootloader_v4.14_18f4550_X20MHz.hex`
  * 🔸 *Si tu circuito usa cristal de 8 MHz* ➡️ `Bootloader_v4.14_18f4550_X8MHz.hex`
  * 🔸 *Si tu circuito usa cristal de 48 MHz* ➡️ `Bootloader_v4.14_18f4550_X48MHz.hex`

> 🖼️ **[ INSERTA AQUÍ IMAGEN 2: ARCHIVOS .HEX ]**
> *Muestra la lista de archivos de bootloader disponibles en tu carpeta.*
![Lista de archivos .hex del Bootloader](ruta/a/tu/repositorio/image_015f45.jpg)

---

## ⚙️ Fase 3: Configuración y Grabación (XGecu Pro)

* [ ] **1. Identificar el Chip (`Select IC`):**
  * Busca en la lista y selecciona estrictamente: **`PIC18F4550 @DIP40`**.
  * 👁️ *Verificación visual:* Confirma en el recuadro superior que el tamaño (`IC Size`) indique `32768 Bytes` (`0x8000 Bytes`).
* [ ] **2. Verificar Fuses (`Config`):**
  * Entra a la pestaña inferior **`Device.Info / Config`**.
  * Asegúrate de que los valores (*Fuses*) se hayan cargado automáticamente al abrir el `.hex` (configuración del oscilador USB y Watchdog).
* [ ] **3. Quemar la memoria (`PROG.`):**
  * Presiona el botón rojo **`PROG.`** en la barra superior de herramientas.
  * Confirma en la ventana emergente para iniciar la escritura en la memoria Flash y EEPROM.
* [ ] **4. Validación final:**
  * Espera a que la barra de progreso llegue al 100%.
  * Verifica que la consola devuelva el texto verde de éxito: **`Verify OK`** (Verificación correcta).

> 🖼️ **[ INSERTA AQUÍ IMAGEN 3: INTERFAZ PRINCIPAL DE XGPRO ]**
> *Muestra la interfaz del programa con el chip cargado y listo para programar.*
![Interfaz XGecu Pro con PIC18F4550 seleccionado](ruta/a/tu/repositorio/image_015f66.jpg)

---

## 🏁 ¿Qué sigue? (Prueba en Pinguino IDE)

Una vez completados todos los pasos con éxito:
1. **Retira** el PIC18F4550 con cuidado del zócalo ZIF.
2. **Insértalo** en el zócalo de tu placa Pinguino.
3. **Conecta** tu placa por USB a la computadora.
4. 🐧 **Abre Pinguino IDE**, selecciona un ejemplo básico (como `Blink.pde`) y presiona el botón **Compilar y Cargar** para comprobar que tu placa está 100% viva.
