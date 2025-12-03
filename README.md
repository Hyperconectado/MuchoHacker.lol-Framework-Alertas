MuchoHacker.lol — Framework de Clasificación de Alertas Digitales
Versión 1.0 · Documento público · Uso libre bajo licencia MIT
1. Introducción

Este documento define un marco de clasificación simple y estandarizado para evaluar alertas digitales dirigidas al público general. El propósito es facilitar la identificación del nivel de riesgo que representa una alerta digital, especialmente para personas sin conocimientos técnicos, y apoyar a medios de comunicación en la evaluación responsable de incidentes digitales.

El framework clasifica cada alerta en uno de tres niveles:

Alto

Medio

Bajo

La evaluación puede ser realizada manualmente y asistida por herramientas de inteligencia artificial.

2. Alcance

El framework aplica a:

Intentos de fraude digital (phishing, smishing, vishing).

Filtraciones de datos.

Mensajes engañosos o suplantación de identidad.

Intentos de robo de cuentas (WhatsApp, correo, redes sociales).

Enlaces sospechosos enviados por terceros.

Comunicaciones que generen duda o confusión sobre su autenticidad.

No es un framework técnico para análisis forense, sino un instrumento de evaluación ciudadana con fundamento en buenas prácticas internacionales.

3. Objetivo General

Establecer un sistema coherente, verificable y sencillo para determinar la gravedad de alertas digitales que pueden afectar a usuarios finales.

4. Niveles de Clasificación
4.1. Nivel Alto

Definición:
Existe riesgo económico o riesgo inmediato de pérdida de control sobre cuentas, identidad o datos sensibles.

Indicadores típicos:

Solicitud de dinero, transferencias o códigos de verificación.

Enlaces que simulan bancos, entidades del Estado o servicios de pago.

Amenazas de bloqueo de cuentas.

Filtración confirmada de información personal crítica.

Acciones que podrían resultar en pérdida financiera inmediata.

Acción recomendada:
Interrumpir la interacción y reportar la alerta.

4.2. Nivel Medio

Definición:
No hay riesgo económico inmediato, pero sí posibilidad de engaño que podría escalar a un incidente mayor.

Indicadores típicos:

Solicitudes poco claras de información.

Enlaces desconocidos sin elementos explícitamente fraudulentos.

Suplantación probable, pero sin presión o urgencia significativa.

Actividad inusual que requiere verificación.

Acción recomendada:
Verificar la información antes de responder o hacer clic.

4.3. Nivel Bajo

Definición:
El riesgo es mínimo. La alerta no presenta elementos suficientes para considerarse un intento de fraude activo.

Indicadores típicos:

Mensajes dudosos pero sin solicitud de acción.

Comunicaciones publicitarias o no deseadas sin contenido engañoso.

Señales débiles sin impacto potencial inmediato.

Acción recomendada:
Monitorear o ignorar.

5. Criterios del Framework

Cada alerta se evalúa en función de seis criterios:

Criterio	Descripción	Nivel asociado
Riesgo económico	¿Existe posibilidad real de perder dinero?	Alto
Robo de cuentas / identidad	¿Existe riesgo de perder acceso a una cuenta?	Alto
Plausibilidad técnica	¿Emplea técnicas conocidas de fraude digital?	Medio
Urgencia / presión	¿Exige una acción rápida o genera miedo?	Medio
Solicitud de datos	¿Pide información o interacción?	Bajo
Impacto colectivo	¿Puede afectar a varias personas o grupos?	Bajo
6. Regla de Decisión

Si la alerta cumple al menos un criterio de nivel alto, se clasifica como:
→ Nivel Alto

Si no cumple criterios altos, pero cumple dos o más criterios de nivel medio, se clasifica como:
→ Nivel Medio

Si solo cumple criterios de nivel bajo, se clasifica como:
→ Nivel Bajo

7. Ejemplos de Aplicación
Ejemplo A

"Hemos bloqueado temporalmente su cuenta bancaria. Valide su identidad aquí."
Criterios activados: riesgo económico, urgencia, suplantación.
Clasificación: Nivel Alto.

Ejemplo B

"Detectamos actividad inusual en su correo. ¿Fue usted?"
Criterios activados: plausibilidad técnica, solicitud de verificación leve.
Clasificación: Nivel Medio.

Ejemplo C

Correo dudoso sin enlaces y sin solicitud de datos.
Clasificación: Nivel Bajo.

8. Referencias Metodológicas

El framework se inspira en lineamientos de organizaciones especializadas, incluyendo:

NIST Cybersecurity Framework

ENISA Threat Landscape

CISA Phishing Guidance

OWASP Phishing Initiative

CERT/CSIRT de referencia internacional

Investigaciones documentadas sobre fraude digital en Latinoamérica

9. Contribuciones

Las sugerencias y mejoras son bienvenidas.
Este es un proyecto abierto mantenido por MuchoHacker.lol para fortalecer la alfabetización digital en la región.

10. Licencia

Este marco se publica bajo la Licencia MIT.
