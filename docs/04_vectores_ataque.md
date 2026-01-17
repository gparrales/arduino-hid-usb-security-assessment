# Vectores de ataque

### Introducción basada en resultados

Se analizan cuatro tareas y su asociación con la superficie de ataque correspondiente, ejecutados mediante el uso de un **Arduino Leonardo** configurado como **HID**, detallando **las acciones realizadas**, **la interacción con el sistema**, **el resultado**, **el tiempo de ejecución** y **los requisitos** que permitieron el éxito.

La Imagen mostrada a continuación resume los resultados de las acciones ejecutadas .

![Resultados](https://github.com/gparrales/arduino-hid-usb-security-assessment/blob/main/diagrams/Resultados_Vetores_Ataque.png)

> Nota de alcance: las acciones se describen **a nivel conceptual** y con fines de **evaluación de riesgos**. Se muestran parte de los scripts utilizados.

---

### Vector de ataque 1: Reconocimiento automático del dispositivo HID y preparación del entorno

**Acciones ejecutadas**

* Conectar físicamente el Arduino al equipo víctima.

**Interacción con el sistema**

* Enumeración automática del dispositivo como dispositivo de entrada USB (como si fuera un teclado/mouse).
* El sistema acepta eventos de entrada sin validación adicional.

**Resultado**

* **Éxito**, el PC reconoce al arduino como un dispositivo HID.
* **Tiempo**: 1 segundo.

**Requisitos de éxito**

* Acceso físico.
* Puertos USB habilitados.
* Configuración por defecto y ausencia de controles restrictivos sobre HID.

---

### Vector 2: Inyección de pulsaciones 

**Acciones ejecutadas**

* Deshabilitar antivirus (Windows Defender).
* Deshabilitar firewall de Windows.
* Extracción de credenciales de las redes WI-Fi almacenadas en el PC.
* Exfiltración de las credenciales de las redes WI-Fi recopiladas.

**Interacción con el sistema**

* Inyección de pulsaciones indistinguibles de la entrada humana.
* Interacción con componentes de configuración accesibles al usuario.

**Resultado**

* **Éxito**, el equipo víctima, a través de pulsaciones pudo interactuar con el sistema, deshabilitar sistemas de seguridad y enviar información.
* **Tiempo**: total en tareas simultáneas fue de 75 segundos o menos.

**Requisitos de éxito**

* Sesión de usuario activa.
* Conocimiento previo de la seguridad básica del equipo.
* Políticas locales permisivas.

![Scripts utilizados](https://github.com/gparrales/arduino-hid-usb-security-assessment/blob/main/diagrams/antivirus-firewall.png)
---

### Vector 3: Acceso a información de conectividad almacenada

**Acciones ejecutadas**

* Extraer credenciales de redes Wi‑Fi almacenadas en el PC.

**Interacción con el sistema**

* Apertura de un intérprete (CLI) o herramienta accesible al usuario.
* Lectura/Escritura de información localmente.

**Resultado**

* **Éxito**, a través de la inserción de comandos se pudo extraer los SSID's y los respectivos passwords de las redes Wi-Fi a las que el equipo tuvo acceso.
* **Tiempo**: 14 segundos.

**Requisitos de éxito**

* Existencia previa de perfiles Wi‑Fi almacenados.

![Script utilizado](https://github.com/gparrales/arduino-hid-usb-security-assessment/blob/main/diagrams/Desactivar-WiFi.png)
---

### Vector 4: Exfiltración de información

**Acciones ejecutadas**

* Enviar un email con información sobre las redes Wi‑Fi recopiladas.

**Interacción con el sistema**

* Uso de capacidades de comunicación disponibles en el equipo (Internet).
* Envío de información recopilada sin generar alertas visibles.

**Resultado**

* **Éxito**, se redactó un correo en el equipo víctima que luego se envió a una cuenta de correo específica.
* **Tiempo**: 22 segundos.

**Requisitos de éxito**

* Conectividad a internet.
* Ausencia de controles de salida restrictivos.
* Confianza implícita del usuario en el dispositivo.

![Script utilizado](https://github.com/gparrales/arduino-hid-usb-security-assessment/blob/main/diagrams/enviar-email.png)
---

### Interpretación de resultados

Los resultados muestran que:

* Las **cuatro acciones** se ejecutaron con éxito bajo condiciones comunes.
* No se explotaron vulnerabilidades de software.
* El **acceso físico**, la **confianza en HID** y la **configuración por defecto** fueron determinantes.
* Los **tiempos reducidos** incrementan el riesgo operativo.

---

# Attack vectors

### Results-driven overview

It analyzes **four tasks** and their association with the corresponding attack surface, executed using **Arduino Leonardo** configured as a **Human Interface Device (HID)**.

For each attack vector, the following elements are detailed: **executed actions**, **system interaction**, **outcome**, **execution time**, and **enabling requirements** that allowed successful execution.

The image below summarizes the experimental results of the executed actions.

![Results](https://github.com/gparrales/arduino-hid-usb-security-assessment/blob/main/diagrams/Resultados_Vetores_Ataque.png)

> Scope note: all actions are described at a **conceptual level** and strictly for **risk assessment and awareness purposes**. Some of the scripts used are shown.

---

### Attack Vector 1: Automatic HID device recognition and environment preparation

**Executed actions**

* Physically connecting the Arduino Leonardo to the target system.

**System interaction**

* Automatic enumeration of the device as a USB input device (keyboard/mouse).
* The operating system accepts input events without additional validation.

**Outcome**

* **Successful**: the target PC recognizes the Arduino as a legitimate HID device.
* **Execution time**: approximately 1 second.

**Success requirements**

* Physical access to the device.
* Enabled USB ports.
* Default operating system configuration with no restrictive HID controls.

---

### Attack Vector 2: Keystroke injection

**Executed actions**

* Disabling the antivirus solution (Windows Defender).
* **Disabling the Windows firewall**.
* Extracting stored Wi‑Fi network credentials from the system.
* Exfiltrating the collected Wi‑Fi credentials.

**System interaction**

* Injection of keystrokes indistinguishable from legitimate human input.
* Interaction with user-accessible system configuration components.

**Outcome**

* **Successful**: through automated keystrokes, the target system was manipulated to disable security controls and transmit information.
* **Execution time**: the combined execution of tasks took **75 seconds or less**.

**Success requirements**

* An active user session.
* Prior knowledge of the system’s basic security configuration.
* Permissive local security policies.

![Scripts](https://github.com/gparrales/arduino-hid-usb-security-assessment/blob/main/diagrams/antivirus-firewall.png)
---

### Attack Vector 3: Access to stored connectivity information

**Executed actions**

* **Extraction of stored Wi‑Fi network credentials** from the target system.

**System interaction**

* Opening a command-line interface (CLI) or user-accessible tool.
* Reading and processing locally stored network configuration data.

**Outcome**

* **Successful**: SSIDs and their corresponding Wi‑Fi passwords were retrieved for networks previously accessed by the system.
* **Execution time**: approximately **14 seconds**.

**Success requirements**

* Pre-existing stored Wi‑Fi profiles on the target system.

![Script](https://github.com/gparrales/arduino-hid-usb-security-assessment/blob/main/diagrams/Desactivar-WiFi.png)
---

### Attack Vector 4: Information exfiltration

**Executed actions**

* **Sending an email containing the collected Wi‑Fi network information**.

**System interaction**

* Use of available communication capabilities on the system (Internet connectivity).
* Transmission of collected data without generating visible security alerts.

**Outcome**

* **Successful**: an email was composed on the target system and sent to a predefined external email account.
* **Execution time**: approximately **22 seconds**.

**Success requirements**

* Active Internet connectivity.
* Absence of restrictive outbound traffic controls.
* Implicit user trust in the connected device.

![Script](https://github.com/gparrales/arduino-hid-usb-security-assessment/blob/main/diagrams/enviar-email.png)
---

### Results interpretation

The results demonstrate that:

* All **four actions** were successfully executed under common, real-world conditions.
* No software vulnerabilities were exploited.
* **Physical access**, **implicit trust in HID devices**, and **default system configurations** were the key enabling factors.
* The **short execution times** significantly increase the operational risk associated with this attack vector.
