# Análisis de Riesgos

### Activos afectados

* **Confidencialidad**: credenciales Wi‑Fi almacenadas, información de red.
* **Integridad**: configuración de seguridad (antivirus y firewall).
* **Disponibilidad**: degradación potencial por deshabilitación de controles.
* **Reputación y cumplimiento**: riesgo indirecto por fuga de información.

---

### Evaluación de riesgos por vector

#### Vector 1 – Reconocimiento automático de dispositivos HID

* **Impacto (CID)**: C: Medio | I: Bajo | D: Bajo
* **Probabilidad**: Alta (entornos con puertos USB habilitados y políticas por defecto).
* **Nivel de riesgo**: Medio
* **Justificación**: El reconocimiento automático habilita vectores posteriores sin alertas.
* **Controles recomendados**:

  * Políticas de control de dispositivos USB.
  * Whitelisting de HID.
  * Concientización sobre seguridad física.

---

#### Vector 2 – Inyección de pulsaciones y modificación de controles de seguridad

* **Impacto (CID)**: C: Medio | I: Alto | D: Medio
* **Probabilidad**: Media–Alta (sesión activa y políticas permisivas).
* **Nivel de riesgo**: Alto
* **Justificación**: La deshabilitación de antivirus y firewall reduce significativamente la postura de seguridad.
* **Controles recomendados**:

  * Restricción de cambios en controles de seguridad.
  * EDR con detección de comportamientos anómalos.
  * Bloqueo de entrada HID no autorizada.

---

#### Vector 3 – Acceso a información de conectividad almacenada

* **Impacto (CID)**: C: Alto | I: Bajo | D: Bajo
* **Probabilidad**: Media (existencia de perfiles Wi‑Fi almacenados).
* **Nivel de riesgo**: Alto
* **Justificación**: La exposición de credenciales permite movimientos laterales y accesos no autorizados.
* **Controles recomendados**:

  * Cifrado y protección de credenciales.
  * Minimización de información almacenada.
  * Monitoreo de acceso a perfiles de red.

---

#### Vector 4 – Exfiltración lógica de información

* **Impacto (CID)**: C: Alto | I: Bajo | D: Bajo
* **Probabilidad**: Media (conectividad disponible y sin controles de salida).
* **Nivel de riesgo**: Alto
* **Justificación**: La salida de información sin alertas incrementa el impacto del incidente.
* **Controles recomendados**:

  * Controles de egress (salida de datos) y DLP.
  * Monitoreo de tráfico saliente.
  * Alertas por uso anómalo de correo o servicios de red.

---

### Resumen del nivel de riesgo

| Vector                      | Probabilidad | Impacto | Riesgo |
| --------------------------- | ------------ | ------- | ------ |
| HID automático              | Alta         | Medio   | Medio  |
| Inyección de pulsaciones    | Media–Alta   | Alto    | Alto   |
| Acceso a credenciales       | Media        | Alto    | Alto   |
| Exfiltración de información | Media        | Alto    | Alto   |

---

### Conclusiones

El análisis evidencia que **vectores basados en HID** pueden generar **riesgos elevados** sin explotar fallos de software. La combinación de **acceso físico**, **configuraciones por defecto** y **confianza implícita del sistema** incrementa significativamente la superficie de ataque.

Este escenario refuerza la necesidad de controles preventivos y detectivos orientados a **seguridad física**, **gestión de dispositivos** y **concienciación del usuario**.

---

# Risk Analysis

### Affected assets

* **Confidentiality**: stored Wi‑Fi credentials and network information.
* **Integrity**: security configuration (antivirus and firewall).
* **Availability**: potential degradation due to disabled controls.
* **Reputation and compliance**: indirect risk from information leakage.

---

### Methodology

* Threat identification based on observed attack vectors.
* **CIA evaluation** (Confidentiality, Integrity, Availability).
* **Likelihood estimation** based on enabling conditions.
* **Qualitative risk rating** (Low / Medium / High).
* Definition of **preventive, detective, and corrective controls**.

---

### Risk assessment by vector

#### Vector 1 – Automatic HID device recognition

* **Impact (CIA)**: C: Medium | I: Low | A: Low
* **Likelihood**: High (USB ports enabled and default policies).
* **Risk level**: Medium
* **Rationale**: Automatic trust enables subsequent vectors without alerts.
* **Recommended controls**:

  * USB device control policies.
  * HID whitelisting.
  * Physical security awareness.

---

#### Vector 2 – Keystroke injection and security control modification

* **Impact (CIA)**: C: Medium | I: High | A: Medium
* **Likelihood**: Medium–High (active session and permissive policies).
* **Risk level**: High
* **Rationale**: Disabling antivirus and firewall significantly weakens the security posture.
* **Recommended controls**:

  * Restrict changes to security controls.
  * EDR with behavioral detection.
  * Blocking unauthorized HID input.

---

#### Vector 3 – Access to stored connectivity information

* **Impact (CIA)**: C: High | I: Low | A: Low
* **Likelihood**: Medium (presence of stored Wi‑Fi profiles).
* **Risk level**: High
* **Rationale**: Credential exposure enables lateral movement and unauthorized access.
* **Recommended controls**:

  * Credential protection and encryption.
  * Data minimization.
  * Monitoring access to network profiles.

---

#### Vector 4 – Logical information exfiltration

* **Impact (CIA)**: C: High | I: Low | A: Low
* **Likelihood**: Medium (network connectivity without egress controls).
* **Risk level**: High
* **Rationale**: Silent data exfiltration amplifies incident impact.
* **Recommended controls**:

  * Egress filtering and DLP.
  * Outbound traffic monitoring.
  * Alerts for anomalous email or network usage.

---

### Risk summary

| Vector                   | Likelihood  | Impact | Risk   |
| ------------------------ | ----------- | ------ | ------ |
| Automatic HID trust      | High        | Medium | Medium |
| Keystroke injection      | Medium–High | High   | High   |
| Credential access        | Medium      | High   | High   |
| Information exfiltration | Medium      | High   | High   |

---

### Conclusions

The analysis shows that **HID-based vectors** can introduce **high risk levels** without exploiting software vulnerabilities. The combination of **physical access**, **default configurations**, and **implicit system trust** significantly increases the attack surface.

This scenario highlights the importance of **physical security**, **device management**, and **user awareness** as key defensive controls.
