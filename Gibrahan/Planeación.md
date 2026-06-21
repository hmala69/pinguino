## 🎯 Objetivo de la Fase de Planeación
Definir claramente los límites, entregables y requisitos técnicos de la **Tarjeta de Desarrollo Pinguino**, garantizando un entorno estable tanto a nivel de hardware (PIC18F4550) como de software (Pinguino IDE).

## 📋 Alcance Técnico (Scope)

### 🔌 Hardware
- **Microcontrolador base:** PIC18F4550.
- **Alimentación y Regulación:** Entrada externa de 7 a 12 V con regulación a 5 V (regulador L7805)[cite: 176, 177]. [cite_start]Deberá incluir protección contra polaridad inversa, capacitores de filtrado y opción de alimentación por USB[cite: 176].
- **Componentes periféricos:** Conector USB, cristal externo, circuito de reset y un LED indicador.
- **Conectividad:** Pines de expansión 100% disponibles para realizar prácticas con sensores, módulos y dispositivos externos.

### 💻 Software (Pinguino IDE)
- **Compatibilidad:** Windows 10 o superior (32/64 bits).
- **Stack Tecnológico:** Python 2.7.10 (base), pyparsing (análisis de sintaxis), PySide (motor gráfico para la interfaz) y pyusb (comunicación directa PC-placa).

## ✅ Checklist de Entregables para la v1.0
- [ ] Consolidar la investigación de misión y plataformas similares[cite: 181, 182].
- [ ] Aprobar el diseño de la fuente de alimentación y regulación de voltaje[cite: 176].
- [ ] Cerrar la selección de componentes accesibles y económicos para el hardware final.
- [ ] Finalizar el Diagrama Esquemático del Pinguino[cite: 179].
- [ ] Generar y validar los archivos Gerber y Drill para la manufactura de la PCB[cite: 178].
- [ ] Integrar el reporte final de Costos y Manufactura[cite: 180].

## 🔗 Dependencias y Sub-tareas
* **Diseño e Ingeniería:** Vincular con #15 (Diseño de hardware), #16 (Fuentes de alimentación) y #17 (Diseño esquemático).
* **Fabricación:** Vincular con #2 (PCB) y #3 (Investigación de fabricación de PCB's).
* **Gestión:** Vincular con #25 (Costos y manufactura) y #5 (Misión)[cite: 180, 182].

## 🛑 Fuera del Alcance (Out of Scope)
> *Elementos que NO se abordarán en esta primera fase para evitar retrasos.*
* Diseño de módulos de expansión propietarios (se usarán componentes comerciales genéricos).
* Migración del IDE a versiones de Python 3.x (se garantizará la estabilidad sobre Python 2.7 con dependencias como `six` y `wheel`).
