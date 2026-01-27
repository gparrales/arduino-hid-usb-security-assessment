# arduino-hid-usb-security-assessment

## Descripción general

Este proyecto analiza el riesgo de seguridad asociado a dispositivos USB que se identifican como Human Interface Devices (HID) —como teclados— utilizando una placa Arduino Leonardo capaz de emular dicho comportamiento, los scripts utilizados se desarrollaron bajo la plataforma Arduino IDE 2.2.1.

Durante las pruebas se evaluó la foma en la cual un dispositivo malicioso puede:

- Ser reconocido automáticamente por el sistema operativo como teclado legítimo
- Ejecutar comandos sin interacción del usuario
- Evadir controles básicos de seguridad basados en confianza en dispositivos HID
- El objetivo es demostrar el impacto potencial de estos ataques y proponer contramedidas aplicables en entornos corporativos.

### Visión general del proyecto 

![Project Overview](https://github.com/gparrales/arduino-hid-usb-security-assessment/blob/main/diagrams/Overview.jpg)

---

## Objetivos del proyecto

- Evaluar el impacto de dispositivos HID maliciosos conectados vía USB.
- Analizar vectores de ataque básicos ejecutados sin interacción del usuario.
- Identificar riesgos reales y medir el nivel de exposición de un sistema ante este tipo de amenazas.
- Identificar controles de seguridad que mitiguen el riesgo.

---

## Alcance

* Entorno de pruebas **controlado**.
* Sistema operativo Windows 10 con configuraciones comunes.
* Emulación HID mediante Arduino Leonardo.
* Evaluación de **cuatro vectores de ataque** a nivel demostrativo.

---

## Metodología

1. Análisis teórico del riesgo USB/HID.
2. Configuración del laboratorio.
3. Emulación de dispositivo HID.
4. Ejecución controlada de vectores de ataque.
5. Análisis de resultados y riesgos.
6. Definición de contramedidas.

### Diagrama — Flujo metodológico

![Methodology Flow](https://github.com/gparrales/arduino-hid-usb-security-assessment/blob/main/diagrams/methodology-flow.jpeg)

---

## Vectores de ataque evaluados 

* Deshabilitación del antivirus.
* Deshabilitación del firewall.
* Extracción de credenciales Wi‑Fi almacenadas.
* Exfiltración de información por correo electrónico.

> **Nota:** Se documentan flujos e impacto, no scripts completos.

---

## Resultados observados

* Ejecución en segundos tras la conexión USB.
* Sin interacción del usuario.
* Reconocimiento como teclado legítimo por el sistema.
* Impacto potencial **alto** sobre la confidencialidad e integridad.

### Resultados medidos:

![Resultados medidos](https://github.com/gparrales/arduino-hid-usb-security-assessment/blob/main/diagrams/resultados-ataque-arduino.png)

### Diagrama impacto tríada CIA / Diagram — CIA triad impact

![CIA Impact](https://github.com/gparrales/arduino-hid-usb-security-assessment/blob/main/diagrams/cia-impact.jpg)

---

## Contramedidas propuestas

A partir del análisis, se identifican las siguientes medidas de mitigación:

* Políticas de bloqueo de sesión y control de puestos.
* Concientización del usuario sobre riesgos de dispositivos USB desconocidos.
* Endpoints con controles reforzados.
* Restricción y monitoreo de dispositivos USB.
* Controles alineados con ISO/IEC 27002.

### Diagramas Capas de defensa / Diagram — Defense layers

![Defense Layers](https://github.com/gparrales/arduino-hid-usb-security-assessment/blob/main/diagrams/defense-layers.png)

---

## Capturas

Se muestran algunas capturas del Arduino IDE con la implementación parcial del código utilizado en el presente proyecto:

https://github.com/gparrales/arduino-hid-usb-security-assessment/blob/main/diagrams/antivirus-firewall.png
https://github.com/gparrales/arduino-hid-usb-security-assessment/blob/main/diagrams/attack-chain.png
https://github.com/gparrales/arduino-hid-usb-security-assessment/blob/main/diagrams/enviar-email.png

---

## Consideraciones legales y éticas

Proyecto desarrollado con fines **educativos y de concientización** en ciberseguridad, respetando la legislación vigente y principios de hacking ético. El uso indebido de estas técnicas puede constituir un delito.

---

## Estructura del repositorio / Repository structure

```
arduino-hid-security-assessment/
│
├── README.md
├── docs/
│   ├── 01_introduccion.md
│   ├── 02_marco_teorico.md
│   ├── 03_metodologia.md
│   ├── 04_vectores_ataque.md
│   ├── 05_analisis_riesgos.md
│   ├── 06_controles_y_mitigaciones.md
│   └── 07_conclusiones.md
│
├── diagrams/
└── scripts/
```

---

## Autor / Author

**Gabriel Parrales Gutiérrez**

Cybersecurity | Risk Analysis | Security Awareness

---

## Licencia / License

Uso educativo. No autorizado para actividades ilícitas. / Educational use. Not authorized for illegal activities.
