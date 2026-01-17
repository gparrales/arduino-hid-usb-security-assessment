# Controles y Mitigaciones

## Controles por vector de ataque

#### Vector 1 – Reconocimiento automático de dispositivos HID

**Riesgo mitigado**
Confianza implícita en dispositivos HID conectados vía USB.

**Controles asociados**

* **Control de dispositivos y medios**

  * ISO/IEC 27002:2022 – **8.1 User endpoint devices**
  * ISO/IEC 27002:2022 – **7.10 Storage media**
  * NIST SP 800-53 – **CM-7 (Least Functionality)**
  * NIST SP 800-53 – **IA-3 (Device Identification and Authentication)**

* **Seguridad física**

  * ISO/IEC 27002:2022 – **7.4 Physical security monitoring**
  * NIST SP 800-53 – **PE-3 (Physical Access Control)**

**Aplicación práctica**

* Políticas de control de puertos USB.
* Listas blancas de dispositivos HID.
* Procedimientos de control de acceso físico.

---

#### Vector 2 – Inyección de pulsaciones y modificación de controles de seguridad

**Riesgo mitigado**
Deshabilitación de antivirus y firewall mediante automatización HID.

**Controles asociados**

* **Protección de configuraciones de seguridad**

  * ISO/IEC 27002:2022 – **8.9 Configuration management**
  * ISO/IEC 27002:2022 – **8.16 Monitoring activities**
  * NIST SP 800-53 – **CM-5 (Access Restrictions for Change)**
  * NIST SP 800-53 – **SI-7 (Integrity)**

* **Gestión de privilegios**

  * ISO/IEC 27002:2022 – **8.2 Privileged access rights**
  * NIST SP 800-53 – **AC-6 (Least Privilege)**

**Aplicación práctica**

* Restricción de cambios en controles de seguridad.
* Protección contra manipulaciones (tamper protection).
* Detección de cambios no autorizados.

---

#### Vector 3 – Acceso a credenciales Wi‑Fi almacenadas

**Riesgo mitigado**
Exposición de credenciales de conectividad de red.

**Controles asociados**

* **Protección de información sensible**

  * ISO/IEC 27002:2022 – **8.12 Data leakage prevention**
  * ISO/IEC 27002:2022 – **8.24 Use of cryptography**
  * NIST SP 800-53 – **IA-7 (Cryptographic Module Authentication)**
  * NIST SP 800-53 – **SC-12 (Cryptographic Key Establishment and Management)**

* **Gestión de información de autenticación**

  * ISO/IEC 27002:2022 – **5.17 Authentication information**
  * NIST SP 800-53 – **IA-5 (Authenticator Management)**

**Aplicación práctica**

* Minimización del almacenamiento de perfiles Wi‑Fi.
* Protección criptográfica de credenciales.
* Auditoría de accesos a configuraciones de red.

---

#### Vector 4 – Exfiltración lógica de información

**Riesgo mitigado**
Salida no detectada de información sensible.

**Controles asociados**

* **Control de flujo de información**

  * ISO/IEC 27002:2022 – **8.23 Information transfer**
  * ISO/IEC 27002:2022 – **8.12 Data leakage prevention**
  * NIST SP 800-53 – **SC-7 (Boundary Protection)**
  * NIST SP 800-53 – **SI-4 (System Monitoring)**

* **Monitoreo de comunicaciones**

  * ISO/IEC 27002:2022 – **8.16 Monitoring activities**
  * NIST SP 800-53 – **AU-6 (Audit Review, Analysis, and Reporting)**

**Aplicación práctica**

* Controles de salida (egress filtering).
* Políticas DLP.
* Alertas por tráfico o envíos anómalos.

---

### Controles transversales

Estos controles reducen simultáneamente múltiples vectores:

* **Gestión de activos**

  * ISO/IEC 27002:2022 – **5.9 Inventory of information and other associated assets**
  * NIST SP 800-53 – **CM-8 (System Component Inventory)**

* **Concienciación y formación**

  * ISO/IEC 27002:2022 – **6.3 Information security awareness, education and training**
  * NIST SP 800-53 – **AT-2 (Awareness Training)**

* **Gestión de configuraciones seguras**

  * ISO/IEC 27002:2022 – **8.9 Configuration management**
  * NIST SP 800-53 – **CM-2 (Baseline Configuration)**

---

### Conclusión

La asociación de los controles con **ISO/IEC 27002** y **NIST SP 800-53** demuestra que los riesgos identificados pueden mitigarse mediante **controles estandarizados y auditables.**

---

#  Controls and mitigations

### Controls by attack vector

#### Vector 1 – Automatic HID device recognition

**Mitigated risk**
Implicit trust in USB HID devices.

**Mapped controls**

* **Device and media control**

  * ISO/IEC 27002:2022 – **8.1 User endpoint devices**
  * ISO/IEC 27002:2022 – **7.10 Storage media**
  * NIST SP 800-53 – **CM-7 (Least Functionality)**
  * NIST SP 800-53 – **IA-3 (Device Identification and Authentication)**

* **Physical security**

  * ISO/IEC 27002:2022 – **7.4 Physical security monitoring**
  * NIST SP 800-53 – **PE-3 (Physical Access Control)**

---

#### Vector 2 – Keystroke injection and security control modification

**Mitigated risk**
Automated disabling of antivirus and firewall.

**Mapped controls**

* **Security configuration protection**

  * ISO/IEC 27002:2022 – **8.9 Configuration management**
  * ISO/IEC 27002:2022 – **8.16 Monitoring activities**
  * NIST SP 800-53 – **CM-5 (Access Restrictions for Change)**
  * NIST SP 800-53 – **SI-7 (Integrity)**

* **Privilege management**

  * ISO/IEC 27002:2022 – **8.2 Privileged access rights**
  * NIST SP 800-53 – **AC-6 (Least Privilege)**

---

#### Vector 3 – Access to stored Wi‑Fi credentials

**Mitigated risk**
Exposure of stored network credentials.

**Mapped controls**

* **Sensitive information protection**

  * ISO/IEC 27002:2022 – **8.12 Data leakage prevention**
  * ISO/IEC 27002:2022 – **8.24 Use of cryptography**
  * NIST SP 800-53 – **IA-7**
  * NIST SP 800-53 – **SC-12**

* **Authentication information management**

  * ISO/IEC 27002:2022 – **5.17 Authentication information**
  * NIST SP 800-53 – **IA-5 (Authenticator Management)**

---

#### Vector 4 – Logical information exfiltration

**Mitigated risk**
Undetected outbound data transfer.

**Mapped controls**

* **Information flow control**

  * ISO/IEC 27002:2022 – **8.23 Information transfer**
  * ISO/IEC 27002:2022 – **8.12 Data leakage prevention**
  * NIST SP 800-53 – **SC-7 (Boundary Protection)**
  * NIST SP 800-53 – **SI-4 (System Monitoring)**

* **Communications monitoring**

  * ISO/IEC 27002:2022 – **8.16 Monitoring activities**
  * NIST SP 800-53 – **AU-6 (Audit Review, Analysis, and Reporting)**

---

### Cross-cutting controls

* **Asset management**

  * ISO/IEC 27002:2022 – **5.9 Inventory of information and other associated assets**
  * NIST SP 800-53 – **CM-8 (System Component Inventory)**

* **Awareness and training**

  * ISO/IEC 27002:2022 – **6.3 Information security awareness, education and training**
  * NIST SP 800-53 – **AT-2 (Awareness Training)**

* **Secure configuration management**

  * ISO/IEC 27002:2022 – **8.9 Configuration management**
  * NIST SP 800-53 – **CM-2 (Baseline Configuration)**

---

### Conclusion

Mapping the proposed mitigations to **ISO/IEC 27002** and **NIST SP 800-53** demonstrates that the identified risks can be addressed using **standardized, auditable controls.**
