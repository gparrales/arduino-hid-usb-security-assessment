# Metodología

### Enfoque metodológico

Este proyecto se desarrolla bajo un enfoque **práctico y demostrativo**, orientado a la evaluación de riesgos en ciberseguridad y no a la explotación activa de sistemas. La metodología aplicada busca reproducir escenarios realistas de forma **controlada**, permitiendo analizar el impacto y las implicaciones de seguridad asociadas al uso de dispositivos USB que emulan HID.

El enfoque combina:

* Análisis de riesgos
* Pruebas controladas
* Observación de comportamiento del sistema
* Documentación técnica estructurada

### Entorno de evaluación

Las pruebas se realizaron en un entorno aislado, diseñado para minimizar riesgos y evitar impactos no autorizados. El entorno de evaluación incluye:

* Equipo objetivo dedicado exclusivamente a pruebas
* Sistema operativo de escritorio actualizado
* Acceso físico autorizado al dispositivo

Este entorno permite evaluar el comportamiento del sistema ante la inserción de un dispositivo HID sin interferir con sistemas productivos.

### Supuestos y limitaciones

Para mantener la evaluación dentro de un marco ético y realista, se establecen los siguientes supuestos:

* El atacante cuenta con **acceso físico previo** al equipo
* No se utilizan exploits de software ni vulnerabilidades conocidas
* El dispositivo HID es reconocido correctamente por el sistema operativo

Limitaciones del estudio:

* No se evalúan escenarios de persistencia avanzada
* No se consideran mecanismos de evasión sofisticados
* No se incluyen ataques remotos o combinados

### Flujo general de la evaluación

La metodología se estructura en las siguientes fases:

1. Preparación del entorno de pruebas
2. Configuración del dispositivo Arduino como HID
3. Inserción del dispositivo en el sistema objetivo
4. Observación y registro del comportamiento del sistema
5. Análisis del impacto potencial
6. Identificación de contramedidas

Cada fase es documentada de forma independiente para facilitar la trazabilidad y la reproducibilidad del análisis.

### Registro y documentación

Durante cada fase se registran:

* Acciones ejecutadas
* Respuestas del sistema
* Evidencias observables (mensajes, ventanas, logs)
* Tiempo estimado de ejecución

### Diagrama de referencia

![Flujo metodológico de la evaluación](https://github.com/gparrales/arduino-hid-usb-security-assessment/blob/main/diagrams/methodology-flow.jpeg)

---

# Methodology

### Methodological approach

This project follows a **practical and demonstrative approach**, focused on cybersecurity risk assessment rather than active system exploitation. The applied methodology aims to reproduce realistic scenarios in a **controlled environment**, allowing the impact and security implications of USB devices that emulate HID behavior to be analyzed.

The approach combines:

* Risk analysis
* Controlled testing
* System behavior observation
* Structured technical documentation

### Evaluation environment

All tests were conducted in an isolated environment designed to minimize risk and prevent unauthorized impact. The evaluation environment includes:

* A dedicated test workstation
* An up-to-date desktop operating system
* Authorized physical access to the device

This setup enables observation of system behavior when a HID device is connected, without affecting production systems.

### Assumptions and limitations

To maintain the evaluation within an ethical and realistic framework, the following assumptions apply:

* The attacker has **prior physical access** to the target system
* No software exploits or known vulnerabilities are used
* The HID device is correctly recognized by the operating system

Study limitations include:

* No evaluation of advanced persistence techniques
* No sophisticated evasion mechanisms
* No remote or combined attack scenarios

### Evaluation workflow

The methodology is structured into the following phases:

1. Test environment preparation
2. Arduino device configuration as HID
3. Device insertion into the target system
4. Observation and logging of system behavior
5. Impact analysis
6. Identification of countermeasures

Each phase is documented independently to ensure traceability and reproducibility of the assessment.

### Logging and documentation

For each phase, the following elements are recorded:

* Executed actions
* System responses
* Observable evidence (messages, windows, logs)
* Estimated execution time

### Reference diagram

![Methodology workflow](https://github.com/gparrales/arduino-hid-usb-security-assessment/blob/main/diagrams/methodology-flow.jpeg)
