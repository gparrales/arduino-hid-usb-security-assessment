# Introducción

---

## Introducción

### Contexto

En la mayoría de organizaciones y entornos domésticos, los esfuerzos de ciberseguridad se concentran en amenazas **lógicas** como malware, phishing o ataques de red. Sin embargo, la **seguridad física** de los dispositivos continúa siendo un factor subestimado, a pesar de su impacto directo sobre la confidencialidad, integridad y disponibilidad de la información.

Uno de los vectores físicos más ignorados es el **puerto USB**. Comúnmente se asocia el riesgo únicamente a dispositivos de almacenamiento, cuando en realidad existen dispositivos capaces de **emular interfaces humanas (HID)** —como teclados o ratones— que gozan de un alto nivel de confianza por parte del sistema operativo.

### Dispositivos HID como amenaza

Los dispositivos HID son reconocidos automáticamente como periféricos legítimos, lo que permite que ejecuten acciones sin requerir privilegios elevados ni confirmación del usuario. Este comportamiento puede ser explotado por un atacante con acceso físico, posibilitando la ejecución de comandos mediante pulsaciones de teclado simuladas.

Herramientas comerciales como *USB Rubber Ducky* han demostrado la efectividad de este tipo de ataques. No obstante, el uso de **hardware open source y de bajo costo**, como Arduino, amplía significativamente la superficie de ataque y reduce la barrera técnica y económica para su implementación.

### Arduino como plataforma de evaluación

Arduino es una plataforma de hardware y software de código abierto ampliamente utilizada con fines educativos y de prototipado. Algunas placas, como **Arduino Leonardo**, incorporan controladores USB que permiten la emulación nativa de dispositivos HID.

Desde una perspectiva de seguridad informática, esta característica convierte a Arduino en una **plataforma ideal para evaluar riesgos**, ya que permite reproducir escenarios reales de ataque en entornos controlados sin recurrir a herramientas cerradas o propietarias.

### Propósito del proyecto

El propósito de este proyecto es **evaluar y documentar** los riesgos asociados a dispositivos USB que emulan HID, demostrando cómo pueden comprometer un equipo en cuestión de segundos y qué **contramedidas prácticas** pueden aplicarse para mitigar estos escenarios.

Este repositorio no pretende servir como guía de explotación, sino como un **caso de estudio técnico** orientado a la concienciación, el análisis de riesgos y la mejora de las estrategias defensivas.

### Enfoque y alcance

La evaluación se desarrolla bajo un enfoque:

* Ético y educativo
* En entorno controlado
* Con acceso físico previo al dispositivo
* Utilizando vectores de ataque básicos con fines demostrativos

Los detalles técnicos, metodología, análisis de riesgos y contramedidas se documentan progresivamente en las siguientes secciones del proyecto.

### Diagrama de referencia

![Visión general del ataque HID](https://github.com/gparrales/arduino-hid-usb-security-assessment/blob/main/diagrams/Overview.jpg)

---

## Introduction

### Context

In most organizational and home environments, cybersecurity efforts focus primarily on **logical threats** such as malware, phishing, or network-based attacks. However, **physical security** remains one of the most underestimated aspects, despite its direct impact on the confidentiality, integrity, and availability of information.

One of the most overlooked physical vectors is the **USB port**. Risk is often associated only with removable storage devices, while devices capable of **emulating Human Interface Devices (HID)**—such as keyboards or mice—are implicitly trusted by operating systems.

### HID devices as a threat

HID devices are automatically recognized as legitimate peripherals, allowing them to execute actions without elevated privileges or user confirmation. This behavior can be abused by an attacker with physical access, enabling command execution through simulated keystrokes.

Commercial tools like *USB Rubber Ducky* have long demonstrated the effectiveness of these attacks. However, the availability of **low-cost, open-source hardware** such as Arduino significantly expands the attack surface and lowers the barrier to entry.

### Arduino as an assessment platform

Arduino is an open-source hardware and software platform widely used for education and prototyping. Certain boards, such as **Arduino Leonardo**, include native USB controllers that support HID emulation.

From a cybersecurity perspective, this capability makes Arduino an **ideal risk assessment platform**, enabling the reproduction of realistic attack scenarios in controlled environments without relying on proprietary tools.

### Project purpose

The purpose of this project is to **assess and document** the risks associated with USB devices that emulate HID behavior, demonstrating how they can compromise a system within seconds and which **practical countermeasures** can mitigate such scenarios.

This repository is not intended as an exploitation guide, but as a **technical case study** focused on risk analysis, awareness, and defensive improvement.

### Approach and scope

The evaluation follows an approach that is:

* Ethical and educational
* Conducted in a controlled environment
* Based on prior physical access
* Limited to basic, demonstrative attack vectors

Technical details, methodology, risk analysis, and countermeasures are documented in the subsequent sections of this project.
