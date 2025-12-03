🕵️‍♂️ MuchoHacker.lol — Framework de Clasificación de Alertas Digitales
Versión 1.0 — Evaluación simple y clara para personas sin conocimiento técnico

🧭 ¿Qué es este Framework?

El Framework de Clasificación de Alertas Digitales de MuchoHacker.lol es una herramienta pública diseñada para ayudar a personas sin conocimientos técnicos a entender rápidamente el nivel de riesgo de alertas digitales, estafas, filtraciones o intentos de engaño.

Está inspirado en buenas prácticas internacionales (NIST, ENISA, CISA) pero traducido a un lenguaje simple, directo y útil para cualquier ciudadano.

📚 Tabla de Contenidos

Objetivo

Cómo se usa

Niveles de alerta

Criterios de evaluación

Flujo de decisión

Ejemplos prácticos

Referencias

Contribuciones

Licencia

🎯 Objetivo

Crear un sistema simple y estandarizado para clasificar alertas digitales en:

🔴 Alto

🟡 Medio

🟢 Bajo

Este framework permite una evaluación manual, apoyada por IA, en medios de comunicación, periodistas, equipos de atención ciudadana o cualquier persona que quiera entender riesgos en Internet.

🧩 Cómo se usa

Evalúa la alerta (mensaje, correo, enlace, publicación, filtración).

Revisa los criterios del framework.

Marca cada criterio como Sí o No.

Suma el nivel final siguiendo la tabla de decisión.

La IA puede ayudarte a:

Identificar señales sospechosas.

Resumir información.

Detectar patrones de phising, smishing o fraude.

Pero la decisión final siempre es humana.

🚦 Niveles de Alerta
🔴 Alerta ALTA (Riesgo Inmediato)

Color: Rojo
Significa: La persona puede perder dinero, datos críticos o acceso a cuentas.
Reacción recomendada: No interactuar, bloquear, denunciar.

Criterios típicos

Riesgo económico real.

Robo de cuentas bancarias o WhatsApp.

Solicitud urgente de dinero.

Filtración de datos personales sensibles.

Enlaces que simulan bancos o entidades oficiales.

Mensajes con urgencia o amenazas.

🟡 Alerta MEDIA (Precaución)

Color: Amarillo
Significa: Podría convertirse en una estafa o engaño si la persona no tiene cuidado.
Reacción recomendada: Verificar, preguntar, confirmar antes de actuar.

Criterios típicos

Solicitudes sospechosas sin urgencia extrema.

Enlaces desconocidos pero no bancarios.

Mensajes que piden datos “no críticos”.

Contactos no verificados que solicitan información.

Patrones incompletos de fraude.

🟢 Alerta BAJA (Monitoreo / Riesgo Mínimo)

Color: Verde
Significa: El impacto es bajo o nulo. No hay señales fuertes de estafa.
Reacción recomendada: Observar, borrar o ignorar.

Criterios típicos

Mensajes sin solicitud de acción.

Actividad sospechosa pero sin impacto directo.

Errores sin consecuencias (e.g., correo publicitario dudoso).

Informaciones no verificadas que no incluyen enlaces maliciosos.

🛠️ Criterios de Evaluación (Framework)

El evaluador debe revisar estos 6 criterios. Cada uno suma peso para el nivel final.

Criterio	Peso	Pregunta
1. Riesgo Económico	Alto	¿La persona puede perder dinero directamente?
2. Robo de Identidad / Cuentas	Alto	¿Pueden robar una cuenta (WhatsApp, correo, redes)?
3. Verosimilitud Técnica	Medio	¿El mensaje replica técnicas comunes de phising/smishing?
4. Urgencia / Presión Psicológica	Medio	¿Exige actuar rápido o crea miedo?
5. Solicitud de Datos / Acciones	Bajo	¿Solicita información o un clic?
6. Impacto Colectivo	Bajo	¿Puede afectar a múltiples personas (fraudes masivos)?
🧮 Flujo de Decisión

Si 1 o más criterios de ALTO están presentes → 🔴 ALTA

Si NO hay criterios ALTO, pero 2 criterios MEDIOS → 🟡 MEDIA

Si solo hay criterios BAJOS → 🟢 BAJA

Si no aplica ninguno → No es una alerta

🧰 Ejemplos Prácticos
📌 Caso 1: “Tu banco bloqueó tu cuenta. Valida aquí.”

→ Enlace sospechoso + urgencia + riesgo económico
Resultado: 🔴 ALTA

📌 Caso 2: “Hemos visto un intento de acceso. ¿Fuiste tú?”

→ Sospechoso, pero sin solicitud de dinero
Resultado: 🟡 MEDIA

📌 Caso 3: “Promoción sospechosa pero sin pedir datos.”

→ Riesgo bajo, no solicita acciones críticas
Resultado: 🟢 BAJA

📚 Referencias

NIST Cybersecurity Framework

ENISA Threat Landscape

CISA Phishing Guidance

OWASP Phishing Initiative

Centros de Respuesta a Incidentes (CERT/CSIRT) internacionales

Investigaciones de fraude digital en Latinoamérica

🤝 Contribuciones

Pull Requests, issues y mejoras son bienvenidas.
MuchoHacker.lol es una comunidad orientada a ayudar a personas sin conocimiento técnico a moverse seguras en Internet.
