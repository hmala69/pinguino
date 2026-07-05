 ## 🎯 Objetivo de la Fase de Planeación
Definir claramente los límites, entregables y requisitos técnicos de la **Tarjeta de Desarrollo Pinguino**, garantizando un entorno estable tanto a nivel de hardware (PIC18F4550) como de software (Pinguino IDE).

## 📋 Alcance Técnico 

### 🔌 Hardware
- **Microcontrolador base:** PIC18F4550.
- **Alimentación y Regulación:** Entrada externa de 7 a 12 V con regulación a 5 V (regulador L7805). Deberá incluir protección contra polaridad inversa, capacitores de filtrado y opción de alimentación por USB.
- **Componentes periféricos:** Conector USB, cristal externo, circuito de reset y un LED indicador.
- **Conectividad:** Pines de expansión 100% disponibles para realizar prácticas con sensores, módulos y dispositivos externos.

### 💻 Software (Pinguino IDE)
- **Compatibilidad:** Windows 10 o superior (32/64 bits).
- **Stack Tecnológico:** Python 2.7.10 (base), pyparsing (análisis de sintaxis), PySide (motor gráfico para la interfaz) y pyusb (comunicación directa PC-placa).

## ✅ Checklist de Prioridades
- [ ] Consolidar la investigación de misión y plataformas similares.
- [ ] Aprobar el diseño de la fuente de alimentación y regulación de voltaje.
- [ ] Cerrar la selección de componentes accesibles y económicos para el hardware final.
- [ ] Finalizar el Diagrama Esquemático del Pinguino.
- [ ] Generar y validar los archivos Gerber y Drill para la manufactura de la PCB.
- [ ] Integrar el reporte final de Costos y Manufactura.

## 🔗 Dependencias y Sub-tareas
* **Diseño e Ingeniería:** Diseño de hardware, fuentes de alimentación y diseño esquemático.
* **Fabricación:** PCB e investigación de fabricación de PCB's.
* **Gestión:** Costos, manufactura y misión.

## 🛑 Fuera del Alcance 
> *Elementos que NO se abordarán en esta primera fase para evitar retrasos.*
* Diseño de módulos de expansión propietarios (se usarán componentes comerciales genéricos).
* Migración del IDE a versiones de Python 3.x (se garantizará la estabilidad sobre Python 2.7 con dependencias como `six` y `wheel`).
