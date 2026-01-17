# Marco teórico 

---

## Marco teórico

### Seguridad física y ciberseguridad

La seguridad informática no se limita a controles lógicos o digitales. La **seguridad física** forma parte integral de la protección de los activos de información, ya que el acceso directo a un dispositivo puede anular múltiples controles de seguridad implementados a nivel de software.

En escenarios donde un atacante obtiene acceso físico, vectores como puertos USB, teclados externos o dispositivos aparentemente inofensivos pueden convertirse en mecanismos eficaces para comprometer un sistema sin necesidad de explotar vulnerabilidades tradicionales.

### Dispositivos HID (Human Interface Devices)

Los **Human Interface Devices (HID)** son una clase de dispositivos USB diseñados para permitir la interacción directa entre humanos y sistemas informáticos. Ejemplos comunes incluyen teclados, ratones, lectores de códigos de barras y controladores de juegos.

Una característica clave de los HID es que los sistemas operativos los consideran **dispositivos confiables por defecto**, lo que implica:

* Reconocimiento automático sin instalación de drivers adicionales.
* Capacidad de enviar eventos de entrada (teclas, clics) al sistema.
* Ejecución de acciones sin requerir privilegios elevados.

Este modelo de confianza implícita representa un riesgo cuando un dispositivo HID es utilizado con fines maliciosos.

### Emulación HID como vector de ataque

La **emulación HID** consiste en simular el comportamiento de un teclado o ratón para enviar comandos predefinidos al sistema objetivo. A diferencia de otros ataques, este enfoque no explota fallos del sistema operativo, sino que **abusa de funcionalidades legítimas**.

Mediante secuencias automatizadas de pulsaciones de teclado, es posible:

* Ejecutar comandos del sistema.
* Modificar configuraciones de seguridad.
* Extraer información almacenada localmente.
* Iniciar procesos de exfiltración de datos.

### Arduino como plataforma de hardware open source

Arduino es una plataforma de hardware y software de código abierto que permite desarrollar prototipos electrónicos de forma rápida y económica. Algunas placas, como **Arduino Leonardo**, están basadas en microcontroladores que incorporan comunicación USB nativa.

Esta capacidad permite que el dispositivo sea reconocido por el sistema operativo como un HID legítimo, habilitando la ejecución de acciones automatizadas sin levantar alertas inmediatas.

Desde un punto de vista defensivo, Arduino resulta especialmente útil como **plataforma de evaluación**, ya que permite reproducir ataques reales de forma controlada y comprender su impacto.

### Relación con herramientas tipo USB Rubber Ducky

Dispositivos comerciales como **USB Rubber Ducky** operan bajo el mismo principio de emulación HID. La diferencia principal radica en que Arduino:

* Es más accesible económicamente.
* Utiliza hardware y software open source.
* Requiere mayor conocimiento técnico para su configuración.

Esto demuestra que la amenaza no está limitada a herramientas especializadas, sino que puede materializarse con componentes ampliamente disponibles.

### Conceptos clave

* **Payload**: Conjunto de instrucciones que se ejecutan una vez que el dispositivo HID es reconocido por el sistema.
* **Vulnerabilidad**: Debilidad que puede ser explotada para comprometer un activo; en este contexto, la confianza implícita en dispositivos HID.
* **Superficie de ataque**: Conjunto de puntos a través de los cuales un sistema puede ser atacado; los puertos USB forman parte de esta superficie.

### Diagrama de referencia

![Cadena de ataque HID](https://github.com/gparrales/arduino-hid-usb-security-assessment/blob/main/diagrams/attack-chain.png)

---

## Theoretical framework

### Physical security and cybersecurity

Cybersecurity is not limited to logical or digital controls. **Physical security** is a fundamental component of information protection, as direct access to a device can bypass multiple software-based security mechanisms.

When physical access is obtained, vectors such as USB ports or external peripherals can be leveraged to compromise systems without exploiting traditional software vulnerabilities.

### Human Interface Devices (HID)

**Human Interface Devices (HID)** are a class of USB devices designed to enable direct interaction between users and computer systems. Common examples include keyboards, mice, barcode scanners, and game controllers.

HID devices are inherently **trusted by operating systems**, which means:

* Automatic recognition without additional drivers.
* Ability to send input events to the system.
* Execution of actions without elevated privileges.

This implicit trust model introduces risk when HID devices are abused for malicious purposes.

### HID emulation as an attack vector

**HID emulation** involves simulating the behavior of a keyboard or mouse to deliver predefined commands to a target system. Rather than exploiting software flaws, this technique **abuses legitimate system functionality**.

Through automated keystroke sequences, an attacker may:

* Execute system commands.
* Alter security configurations.
* Extract locally stored information.
* Initiate data exfiltration processes.

### Arduino as an open-source hardware platform

Arduino is an open-source hardware and software platform that enables rapid and cost-effective electronic prototyping. Certain boards, such as **Arduino Leonardo**, feature native USB communication capabilities.

This allows the device to be recognized as a legitimate HID by the operating system, enabling automated actions without immediate detection.

From a defensive standpoint, Arduino serves as an effective **risk assessment platform**, allowing realistic attack scenarios to be reproduced in controlled environments.

### Relationship with USB Rubber Ducky–type tools

Commercial tools such as **USB Rubber Ducky** rely on the same HID emulation principle. Arduino differs in that it is:

* More economically accessible.
* Fully open source.
* More configurable, requiring higher technical expertise.

This highlights that the threat is not limited to specialized devices, but can be realized using widely available components.

### Key concepts

* **Payload**: A set of instructions executed once the HID device is recognized by the system.
* **Vulnerability**: A weakness that can be exploited to compromise an asset; in this context, implicit trust in HID devices.
* **Attack surface**: The collection of points through which a system can be attacked; USB ports are part of this surface.

### Reference diagram

![HID attack chain](https://github.com/gparrales/arduino-hid-usb-security-assessment/blob/main/diagrams/attack-chain.png)
