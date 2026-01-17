# Conclusiones y Lecciones Aprendidas

---

## Conclusiones y lecciones aprendidas

### Conclusiones generales

Este proyecto demostró que **ataques basados en dispositivos HID** pueden generar **impactos significativos en la postura de seguridad** de un sistema, incluso **sin explotar vulnerabilidades de software**. La evaluación confirma que factores como el **acceso físico**, la **confianza implícita del sistema operativo** y las **configuraciones por defecto** representan riesgos reales y frecuentemente subestimados.

A partir de los resultados obtenidos, se evidencia que un atacante con acceso físico limitado y recursos mínimos puede:

* Interactuar con el sistema bajo el contexto de un usuario legítimo.
* Deshabilitar controles de seguridad críticos.
* Acceder a información sensible almacenada localmente.
* Exfiltrar datos sin generar alertas inmediatas.

Estos hallazgos refuerzan la necesidad de abordar la ciberseguridad desde una perspectiva **integral**, donde la seguridad lógica, física y organizativa estén estrechamente alineadas.

---

### Lecciones aprendidas

#### 1. La seguridad física es parte fundamental de la ciberseguridad

El acceso físico al equipo fue el habilitador principal de todos los vectores analizados. Este proyecto evidencia que **la falta de controles físicos adecuados puede anular controles lógicos avanzados**, reafirmando la importancia de integrar la seguridad física dentro del modelo de gestión de riesgos.

#### 2. La confianza implícita en dispositivos HID amplía la superficie de ataque

Los sistemas operativos modernos priorizan la usabilidad, lo que deriva en una **confianza automática en dispositivos HID**. Esta característica, aunque funcional, puede ser explotada si no se complementa con políticas de control de dispositivos y monitoreo.

#### 3. Las configuraciones por defecto representan un riesgo operativo

Las configuraciones estándar facilitan la administración inicial de los sistemas, pero también crean **condiciones predecibles** que pueden ser aprovechadas. El proyecto demuestra la necesidad de adoptar enfoques de **hardening temprano**.

#### 4. La velocidad de ejecución incrementa el impacto del ataque

Los tiempos reducidos de ejecución observados en los vectores evaluados disminuyen significativamente las oportunidades de detección y respuesta, incrementando el riesgo operativo y la probabilidad de éxito del ataque.

#### 5. La concienciación del usuario es un control crítico

Incluso con controles técnicos implementados, el **factor humano** sigue siendo determinante. La confianza del usuario en dispositivos externos y la falta de concienciación pueden facilitar escenarios de compromiso.

---

## Conclusions and lessons learned

### General conclusions

This project demonstrated that **HID-based attacks** can produce **significant security impacts** even **without exploiting software vulnerabilities**. The assessment confirms that **physical access**, **implicit operating system trust**, and **default configurations** represent real and often underestimated risks.

The results show that an attacker with limited physical access and minimal resources can:

* Interact with the system under a legitimate user context.
* Disable critical security controls.
* Access sensitive locally stored information.
* Exfiltrate data without immediate detection.

These findings highlight the need for a **holistic security approach**, where logical, physical, and organizational controls are closely aligned.

---

### Lessons learned

#### 1. Physical security is a fundamental component of cybersecurity

Physical access was the primary enabler for all analyzed vectors. This project demonstrates that **weak physical controls can neutralize advanced logical defenses**, reinforcing the importance of integrating physical security into risk management models.

#### 2. Implicit trust in HID devices expands the attack surface

Modern operating systems prioritize usability, resulting in **automatic trust of HID devices**. While functional, this behavior can be abused if not complemented by device control policies and monitoring.

#### 3. Default configurations introduce operational risk

Default settings simplify system deployment but also create **predictable conditions** that attackers can leverage. The project underscores the importance of **early system hardening**.

#### 4. Execution speed amplifies attack impact

The short execution times observed significantly reduce detection and response windows, increasing both operational risk and attack success probability.

#### 5. User awareness remains a critical control

Even with technical safeguards in place, the **human factor** remains decisive. User trust in external devices and lack of awareness can facilitate compromise scenarios.
