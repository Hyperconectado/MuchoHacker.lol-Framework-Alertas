<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Framework de Clasificación de Alertas Digitales | MuchoHacker.lol</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #2c3e50;
            --secondary-color: #3498db;
            --high-risk: #e74c3c;
            --medium-risk: #f39c12;
            --low-risk: #27ae60;
            --light-bg: #f8f9fa;
            --border-color: #dee2e6;
            --text-color: #333;
            --text-light: #6c757d;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: var(--text-color);
            background-color: var(--light-bg);
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        header {
            background-color: var(--primary-color);
            color: white;
            padding: 2rem;
            border-radius: 10px;
            margin-bottom: 2rem;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }
        
        .logo-header {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 1rem;
        }
        
        .logo-header i {
            font-size: 2.5rem;
            color: var(--secondary-color);
        }
        
        h1 {
            font-size: 2.2rem;
            margin-bottom: 0.5rem;
        }
        
        .subtitle {
            font-size: 1.1rem;
            color: #ecf0f1;
            margin-bottom: 1.5rem;
            font-weight: 300;
        }
        
        .metadata {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            font-size: 0.9rem;
            color: #bdc3c7;
        }
        
        .metadata span {
            background-color: rgba(255, 255, 255, 0.1);
            padding: 5px 10px;
            border-radius: 20px;
        }
        
        .badge {
            display: inline-block;
            padding: 3px 10px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: bold;
            margin-right: 5px;
        }
        
        .badge-high {
            background-color: var(--high-risk);
            color: white;
        }
        
        .badge-medium {
            background-color: var(--medium-risk);
            color: white;
        }
        
        .badge-low {
            background-color: var(--low-risk);
            color: white;
        }
        
        section {
            background-color: white;
            padding: 1.5rem 2rem;
            margin-bottom: 2rem;
            border-radius: 10px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
            border-left: 5px solid var(--secondary-color);
        }
        
        h2 {
            color: var(--primary-color);
            margin-bottom: 1rem;
            padding-bottom: 0.5rem;
            border-bottom: 2px solid var(--border-color);
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        h2 i {
            color: var(--secondary-color);
        }
        
        h3 {
            color: var(--primary-color);
            margin: 1.5rem 0 0.8rem;
        }
        
        p {
            margin-bottom: 1rem;
        }
        
        ul, ol {
            margin-left: 1.5rem;
            margin-bottom: 1rem;
        }
        
        li {
            margin-bottom: 0.5rem;
        }
        
        .classification-levels {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
            margin-top: 1.5rem;
        }
        
        .level-card {
            border-radius: 10px;
            padding: 1.5rem;
            color: white;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        
        .level-high {
            background-color: var(--high-risk);
        }
        
        .level-medium {
            background-color: var(--medium-risk);
        }
        
        .level-low {
            background-color: var(--low-risk);
        }
        
        .level-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1rem;
        }
        
        .level-title {
            font-size: 1.5rem;
            font-weight: bold;
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 1.5rem 0;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.05);
        }
        
        th {
            background-color: var(--primary-color);
            color: white;
            text-align: left;
            padding: 1rem;
        }
        
        td {
            padding: 1rem;
            border-bottom: 1px solid var(--border-color);
        }
        
        tr:nth-child(even) {
            background-color: #f8f9fa;
        }
        
        .examples {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
            margin-top: 1.5rem;
        }
        
        .example-card {
            border-radius: 8px;
            padding: 1.5rem;
            border: 1px solid var(--border-color);
            background-color: white;
        }
        
        .example-header {
            display: flex;
            justify-content: space-between;
            margin-bottom: 1rem;
        }
        
        .example-alert {
            background-color: #f8f9fa;
            padding: 1rem;
            border-radius: 5px;
            font-style: italic;
            margin-bottom: 1rem;
            border-left: 3px solid var(--secondary-color);
        }
        
        footer {
            text-align: center;
            padding: 2rem;
            color: var(--text-light);
            border-top: 1px solid var(--border-color);
            margin-top: 2rem;
            font-size: 0.9rem;
        }
        
        .license {
            background-color: #f8f9fa;
            padding: 1rem;
            border-radius: 5px;
            margin-top: 1rem;
            font-family: monospace;
        }
        
        .contributions {
            background-color: #e8f4fc;
            padding: 1.5rem;
            border-radius: 8px;
            margin-top: 1rem;
            border-left: 5px solid var(--secondary-color);
        }
        
        @media (max-width: 768px) {
            body {
                padding: 10px;
            }
            
            section {
                padding: 1rem;
            }
            
            .classification-levels, .examples {
                grid-template-columns: 1fr;
            }
            
            h1 {
                font-size: 1.8rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="logo-header">
            <i class="fas fa-shield-alt"></i>
            <div>
                <h1>Framework de Clasificación de Alertas Digitales</h1>
                <div class="subtitle">Un sistema simple y estandarizado para evaluar alertas digitales dirigidas al público general</div>
            </div>
        </div>
        
        <div class="metadata">
            <span><i class="fas fa-code-branch"></i> Versión 1.0</span>
            <span><i class="fas fa-file-alt"></i> Documento público</span>
            <span><i class="fas fa-balance-scale"></i> Uso libre bajo licencia MIT</span>
            <span><i class="fas fa-globe-americas"></i> MuchoHacker.lol</span>
        </div>
    </header>
    
    <section>
        <h2><i class="fas fa-info-circle"></i> Introducción</h2>
        <p>Este documento define un marco de clasificación simple y estandarizado para evaluar alertas digitales dirigidas al público general. El propósito es facilitar la identificación del nivel de riesgo que representa una alerta digital, especialmente para personas sin conocimientos técnicos, y apoyar a medios de comunicación en la evaluación responsable de incidentes digitales.</p>
        
        <p>El framework clasifica cada alerta en uno de tres niveles:</p>
        
        <div style="display: flex; gap: 1rem; margin-top: 1.5rem;">
            <div><span class="badge badge-high">ALTO</span> Riesgo económico o de seguridad inmediato</div>
            <div><span class="badge badge-medium">MEDIO</span> Posibilidad de engaño que podría escalar</div>
            <div><span class="badge badge-low">BAJO</span> Riesgo mínimo sin elementos fraudulentos activos</div>
        </div>
        
        <p style="margin-top: 1.5rem;">La evaluación puede ser realizada manualmente y asistida por herramientas de inteligencia artificial.</p>
    </section>
    
    <section>
        <h2><i class="fas fa-bullseye"></i> Alcance</h2>
        <p>El framework aplica a:</p>
        <ul>
            <li>Intentos de fraude digital (phishing, smishing, vishing).</li>
            <li>Filtraciones de datos.</li>
            <li>Mensajes engañosos o suplantación de identidad.</li>
            <li>Intentos de robo de cuentas (WhatsApp, correo, redes sociales).</li>
            <li>Enlaces sospechosos enviados por terceros.</li>
            <li>Comunicaciones que generen duda o confusión sobre su autenticidad.</li>
        </ul>
        
        <div style="background-color: #f8f9fa; padding: 1rem; border-radius: 5px; margin-top: 1rem;">
            <p><strong>Nota:</strong> Este no es un framework técnico para análisis forense, sino un instrumento de evaluación ciudadana con fundamento en buenas prácticas internacionales.</p>
        </div>
    </section>
    
    <section>
        <h2><i class="fas fa-bullseye"></i> Objetivo General</h2>
        <p>Establecer un sistema coherente, verificable y sencillo para determinar la gravedad de alertas digitales que pueden afectar a usuarios finales.</p>
    </section>
    
    <section>
        <h2><i class="fas fa-layer-group"></i> Niveles de Clasificación</h2>
        
        <div class="classification-levels">
            <div class="level-card level-high">
                <div class="level-header">
                    <div class="level-title">Nivel Alto</div>
                    <div><i class="fas fa-exclamation-triangle fa-2x"></i></div>
                </div>
                <p><strong>Definición:</strong> Existe riesgo económico o riesgo inmediato de pérdida de control sobre cuentas, identidad o datos sensibles.</p>
                
                <h3>Indicadores típicos:</h3>
                <ul>
                    <li>Solicitud de dinero, transferencias o códigos de verificación.</li>
                    <li>Enlaces que simulan bancos, entidades del Estado o servicios de pago.</li>
                    <li>Amenazas de bloqueo de cuentas.</li>
                    <li>Filtración confirmada de información personal crítica.</li>
                    <li>Acciones que podrían resultar en pérdida financiera inmediata.</li>
                </ul>
                
                <h3>Acción recomendada:</h3>
                <p><strong>Interrumpir la interacción y reportar la alerta.</strong></p>
            </div>
            
            <div class="level-card level-medium">
                <div class="level-header">
                    <div class="level-title">Nivel Medio</div>
                    <div><i class="fas fa-exclamation-circle fa-2x"></i></div>
                </div>
                <p><strong>Definición:</strong> No hay riesgo económico inmediato, pero sí posibilidad de engaño que podría escalar a un incidente mayor.</p>
                
                <h3>Indicadores típicos:</h3>
                <ul>
                    <li>Solicitudes poco claras de información.</li>
                    <li>Enlaces desconocidos sin elementos explícitamente fraudulentos.</li>
                    <li>Suplantación probable, pero sin presión o urgencia significativa.</li>
                    <li>Actividad inusual que requiere verificación.</li>
                </ul>
                
                <h3>Acción recomendada:</h3>
                <p><strong>Verificar la información antes de responder o hacer clic.</strong></p>
            </div>
            
            <div class="level-card level-low">
                <div class="level-header">
                    <div class="level-title">Nivel Bajo</div>
                    <div><i class="fas fa-info-circle fa-2x"></i></div>
                </div>
                <p><strong>Definición:</strong> El riesgo es mínimo. La alerta no presenta elementos suficientes para considerarse un intento de fraude activo.</p>
                
                <h3>Indicadores típicos:</h3>
                <ul>
                    <li>Mensajes dudosos pero sin solicitud de acción.</li>
                    <li>Comunicaciones publicitarias o no deseadas sin contenido engañoso.</li>
                    <li>Señales débiles sin impacto potencial inmediato.</li>
                </ul>
                
                <h3>Acción recomendada:</h3>
                <p><strong>Monitorear o ignorar.</strong></p>
            </div>
        </div>
    </section>
    
    <section>
        <h2><i class="fas fa-clipboard-list"></i> Criterios del Framework</h2>
        <p>Cada alerta se evalúa en función de seis criterios:</p>
        
        <table>
            <thead>
                <tr>
                    <th>Criterio</th>
                    <th>Descripción</th>
                    <th>Nivel asociado</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td><strong>Riesgo económico</strong></td>
                    <td>¿Existe posibilidad real de perder dinero?</td>
                    <td><span class="badge badge-high">Alto</span></td>
                </tr>
                <tr>
                    <td><strong>Robo de cuentas / identidad</strong></td>
                    <td>¿Existe riesgo de perder acceso a una cuenta?</td>
                    <td><span class="badge badge-high">Alto</span></td>
                </tr>
                <tr>
                    <td><strong>Plausibilidad técnica</strong></td>
                    <td>¿Emplea técnicas conocidas de fraude digital?</td>
                    <td><span class="badge badge-medium">Medio</span></td>
                </tr>
                <tr>
                    <td><strong>Urgencia / presión</strong></td>
                    <td>¿Exige una acción rápida o genera miedo?</td>
                    <td><span class="badge badge-medium">Medio</span></td>
                </tr>
                <tr>
                    <td><strong>Solicitud de datos</strong></td>
                    <td>¿Pide información o interacción?</td>
                    <td><span class="badge badge-low">Bajo</span></td>
                </tr>
                <tr>
                    <td><strong>Impacto colectivo</strong></td>
                    <td>¿Puede afectar a varias personas o grupos?</td>
                    <td><span class="badge badge-low">Bajo</span></td>
                </tr>
            </tbody>
        </table>
    </section>
    
    <section>
        <h2><i class="fas fa-gavel"></i> Regla de Decisión</h2>
        
        <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 1.5rem; margin-top: 1.5rem;">
            <div style="background-color: #fff5f5; padding: 1.5rem; border-radius: 8px; border-left: 5px solid var(--high-risk);">
                <h3><span class="badge badge-high">Nivel Alto</span></h3>
                <p>Si la alerta cumple <strong>al menos un criterio</strong> de nivel alto.</p>
                <div style="text-align: center; font-size: 2rem; margin: 1rem 0;">→</div>
                <p>Clasificación: <strong>Nivel Alto</strong></p>
            </div>
            
            <div style="background-color: #fff9e6; padding: 1.5rem; border-radius: 8px; border-left: 5px solid var(--medium-risk);">
                <h3><span class="badge badge-medium">Nivel Medio</span></h3>
                <p>Si no cumple criterios altos, pero cumple <strong>dos o más criterios</strong> de nivel medio.</p>
                <div style="text-align: center; font-size: 2rem; margin: 1rem 0;">→</div>
                <p>Clasificación: <strong>Nivel Medio</strong></p>
            </div>
            
            <div style="background-color: #f0fff4; padding: 1.5rem; border-radius: 8px; border-left: 5px solid var(--low-risk);">
                <h3><span class="badge badge-low">Nivel Bajo</span></h3>
                <p>Si solo cumple criterios de nivel bajo.</p>
                <div style="text-align: center; font-size: 2rem; margin: 1rem 0;">→</div>
                <p>Clasificación: <strong>Nivel Bajo</strong></p>
            </div>
        </div>
    </section>
    
    <section>
        <h2><i class="fas fa-vial"></i> Ejemplos de Aplicación</h2>
        
        <div class="examples">
            <div class="example-card">
                <div class="example-header">
                    <h3>Ejemplo A</h3>
                    <span class="badge badge-high">Nivel Alto</span>
                </div>
                
                <div class="example-alert">
                    "Hemos bloqueado temporalmente su cuenta bancaria. Valide su identidad aquí."
                </div>
                
                <p><strong>Criterios activados:</strong></p>
                <ul>
                    <li>Riesgo económico <span class="badge badge-high">Alto</span></li>
                    <li>Urgencia <span class="badge badge-medium">Medio</span></li>
                    <li>Suplantación <span class="badge badge-high">Alto</span></li>
                </ul>
                
                <p><strong>Clasificación:</strong> <span class="badge badge-high">Nivel Alto</span></p>
            </div>
            
            <div class="example-card">
                <div class="example-header">
                    <h3>Ejemplo B</h3>
                    <span class="badge badge-medium">Nivel Medio</span>
                </div>
                
                <div class="example-alert">
                    "Detectamos actividad inusual en su correo. ¿Fue usted?"
                </div>
                
                <p><strong>Criterios activados:</strong></p>
                <ul>
                    <li>Plausibilidad técnica <span class="badge badge-medium">Medio</span></li>
                    <li>Solicitud de verificación leve <span class="badge badge-low">Bajo</span></li>
                </ul>
                
                <p><strong>Clasificación:</strong> <span class="badge badge-medium">Nivel Medio</span></p>
            </div>
            
            <div class="example-card">
                <div class="example-header">
                    <h3>Ejemplo C</h3>
                    <span class="badge badge-low">Nivel Bajo</span>
                </div>
                
                <div class="example-alert">
                    Correo dudoso sin enlaces y sin solicitud de datos.
                </div>
                
                <p><strong>Criterios activados:</strong></p>
                <ul>
                    <li>Solicitud de datos <span class="badge badge-low">Bajo</span></li>
                </ul>
                
                <p><strong>Clasificación:</strong> <span class="badge badge-low">Nivel Bajo</span></p>
            </div>
        </div>
    </section>
    
    <section>
        <h2><i class="fas fa-book"></i> Referencias Metodológicas</h2>
        <p>El framework se inspira en lineamientos de organizaciones especializadas, incluyendo:</p>
        
        <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 1rem; margin-top: 1.5rem;">
            <div style="padding: 1rem; background-color: #f8f9fa; border-radius: 5px;">
                <i class="fas fa-shield-alt" style="color: var(--secondary-color); margin-right: 10px;"></i> NIST Cybersecurity Framework
            </div>
            <div style="padding: 1rem; background-color: #f8f9fa; border-radius: 5px;">
                <i class="fas fa-shield-alt" style="color: var(--secondary-color); margin-right: 10px;"></i> ENISA Threat Landscape
            </div>
            <div style="padding: 1rem; background-color: #f8f9fa; border-radius: 5px;">
                <i class="fas fa-shield-alt" style="color: var(--secondary-color); margin-right: 10px;"></i> CISA Phishing Guidance
            </div>
            <div style="padding: 1rem; background-color: #f8f9fa; border-radius: 5px;">
                <i class="fas fa-shield-alt" style="color: var(--secondary-color); margin-right: 10px;"></i> OWASP Phishing Initiative
            </div>
            <div style="padding: 1rem; background-color: #f8f9fa; border-radius: 5px;">
                <i class="fas fa-shield-alt" style="color: var(--secondary-color); margin-right: 10px;"></i> CERT/CSIRT de referencia internacional
            </div>
            <div style="padding: 1rem; background-color: #f8f9fa; border-radius: 5px;">
                <i class="fas fa-shield-alt" style="color: var(--secondary-color); margin-right: 10px;"></i> Investigaciones sobre fraude digital en Latinoamérica
            </div>
        </div>
    </section>
    
    <section>
        <h2><i class="fas fa-handshake"></i> Contribuciones</h2>
        <div class="contributions">
            <p>Las sugerencias y mejoras son bienvenidas. Este es un proyecto abierto mantenido por <strong>MuchoHacker.lol</strong> para fortalecer la alfabetización digital en la región.</p>
            <p style="margin-top: 1rem;"><i class="fas fa-external-link-alt"></i> <strong>Colabora:</strong> Puedes contribuir mediante issues, pull requests o discusiones en el repositorio oficial del proyecto.</p>
        </div>
    </section>
    
    <section>
        <h2><i class="fas fa-file-contract"></i> Licencia</h2>
        <p>Este marco se publica bajo la Licencia MIT.</p>
        
        <div class="license">
            <p>Copyright © 2023 MuchoHacker.lol</p>
            <p>Se concede permiso, de forma gratuita, a cualquier persona que obtenga una copia de este software y de los archivos de documentación asociados (el "Software"), para utilizar el Software sin restricción, incluyendo sin limitación los derechos a usar, copiar, modificar, fusionar, publicar, distribuir, sublicenciar y/o vender copias del Software, y a permitir a las personas a las que se les proporcione el Software a hacer lo mismo, sujeto a las siguientes condiciones:</p>
            <p>El aviso de copyright anterior y este aviso de permiso se incluirán en todas las copias o partes sustanciales del Software.</p>
        </div>
    </section>
    
    <footer>
        <p><strong>Framework de Clasificación de Alertas Digitales</strong> · Versión 1.0</p>
        <p>Desarrollado por <strong>MuchoHacker.lol</strong> · Documento público · Uso libre bajo licencia MIT</p>
        <p style="margin-top: 1rem; color: var(--text-light); font-size: 0.8rem;">
            <i class="fas fa-globe-americas"></i> Diseñado para fortalecer la seguridad digital en Latinoamérica
        </p>
    </footer>
</body>
</html>
