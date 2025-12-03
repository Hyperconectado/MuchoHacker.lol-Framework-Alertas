MuchoHacker.lol – Framework de Clasificación de Alertas Digitales (Alto, Medio, Bajo)

Framework público desarrollado por MuchoHacker.lol para clasificar alertas digitales y amenazas cibernéticas en tres niveles simples: Alto, Medio y Bajo.

Está diseñado para personas sin conocimientos técnicos, para evaluación manual, y apoyado opcionalmente con herramientas de IA. Se inspira en estándares como NIST, ENISA, MITRE ATT&CK, CVSS y buenas prácticas de la industria.

1. Objetivo

Proveer una herramienta clara y accesible para evaluar riesgos asociados a:

Phishing

Smishing

Estafas digitales

Malware

Fugas de datos

Suplantación

Incidentes de seguridad en general

La filosofía del marco:
👉 Una amenaza es ALTA si existe riesgo real de pérdida económica o daño grave.

2. Criterios de evaluación

La severidad de una alerta se clasifica considerando cinco factores:

2.1. Impacto económico (criterio principal)

¿Existe posibilidad real de perder dinero?

¿Puede generar fraude, pagos no autorizados, extorsión o robo?

Si la respuesta es SÍ → Riesgo ALTO.

2.2. Impacto operativo

Mide si afecta sistemas, servicios o procesos críticos.

Paralización o daño grave → ALTO

Interrupciones moderadas → MEDIO

Sin impacto visible → BAJO

2.3. Sensibilidad de los datos involucrados

Datos financieros, contraseñas, datos personales sensibles → ALTO

Información interna no sensible → MEDIO

Información pública → BAJO

2.4. Alcance (cuántos están afectados)

Muchas personas o sistemas críticos → ALTO

Grupos pequeños → MEDIO

Un único usuario → BAJO

2.5. Evidencia del ataque

Ataque confirmado o artefacto malicioso detectado → ALTO

Señal sospechosa creíble → MEDIO

Evento probablemente benigno → BAJO

3. Definiciones de los niveles
✔️ ALTO

Involucra pérdida económica, daño operativo severo o fuga de datos sensibles.
Requiere acción inmediata.

✔️ MEDIO

Riesgo moderado, creíble pero sin impacto grave inmediato.
Requiere revisión y seguimiento.

✔️ BAJO

Impacto mínimo o incierto.
Requiere monitoreo básico.

4. Ejemplos prácticos
Escenario	Clasificación	Motivo
SMS que dice “su cuenta será bloqueada, ingrese aquí”	ALTO	Riesgo de fraude directo
Email genérico de premio falso	MEDIO	Menor probabilidad de pérdida real
Spam masivo	BAJO	Sin impacto económico
Ransomware en equipo corporativo	ALTO	Paraliza operaciones
Fuga de datos internos no sensibles	MEDIO	Impacto limitado
Intentos de login desde país desconocido	MEDIO	Sospecha moderada
5. Pasos para aplicar el framework

Identificar el incidente.

Evaluar el impacto económico (criterio clave).

Revisar los demás factores:

Datos

Alcance

Operación

Evidencia

Asignar Alto / Medio / Bajo.

Registrar la razón en una frase.

6. Fuentes oficiales (públicas y verificables)
NIST

Guía de manejo de incidentes (SP 800-61 Rev.2):
https://csrc.nist.gov/publications/detail/sp/800-61/rev-2/final

Framework de ciberseguridad:
https://www.nist.gov/cyberframework

ENISA

https://www.enisa.europa.eu

MITRE ATT&CK

https://attack.mitre.org/

CVSS – FIRST

https://www.first.org/cvss/

Microsoft Defender – Severidad de alertas

https://learn.microsoft.com/en-us/defender/

INCIBE – guías para usuarios

https://www.incibe.es/

7. Licencia

Este framework se distribuye bajo la MIT License.

8. Autor

MuchoHacker.lol
Marco abierto para fortalecer la educación digital en usuarios no técnicos.

✨ Gracias por usar y mejorar este framework

Pull requests y mejoras son bienvenidas.
