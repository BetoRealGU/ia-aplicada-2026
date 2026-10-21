# Iteración 0 — Prompt mínimo

**Materia:** Inteligencia Artificial Aplicada  
**Área:** Ciberseguridad  
**Modelo utilizado:** ChatGPT  
**Objetivo:** Evaluar las respuestas iniciales del modelo antes de aplicar técnicas de mejora de prompts.

## Prompt utilizado

```text
Clasifica este reporte de incidente:

[pega aquí la entrada]
```

---

## Entrada 1 — Reporte claro y completo

### Texto de entrada

El lunes a las 10:30 a. m., un empleado recibió un correo de phishing en su computadora de trabajo. El mensaje solicitaba verificar su contraseña mediante un enlace sospechoso. El empleado hizo clic, pero no ingresó sus credenciales. El equipo afectado es una laptop corporativa con acceso al correo empresarial. El incidente fue reportado al área de TI y el dispositivo continúa conectado a la red.

### Respuesta original de ChatGPT

Con la información proporcionada, podemos documentar el incidente como un caso de phishing en un entorno corporativo y establecer las acciones de respuesta correspondientes.

## 1. Registro del incidente de ciberseguridad

| Campo | Información |
|---|---|
| Tipo de incidente | Phishing |
| Fecha y hora | Lunes, 10:30 a. m. (fecha exacta por confirmar) |
| Activo afectado | Laptop corporativa |
| Recurso relacionado | Correo empresarial |
| Vector de ataque | Correo electrónico con enlace sospechoso |
| Acción del empleado | Hizo clic en el enlace |
| Credenciales ingresadas | No |
| Reporte | Notificado al área de TI |
| Estado del dispositivo | Continúa conectado a la red |
| Nivel de riesgo inicial | Moderado, pendiente de investigación |

## 2. Análisis del incidente

El incidente comenzó cuando un empleado recibió un correo electrónico que solicitaba verificar su contraseña mediante un enlace sospechoso. Aunque hizo clic, no ingresó sus credenciales, lo que reduce el riesgo de robo de contraseñas mediante ese formulario. Sin embargo, esto no descarta otros riesgos, como la descarga automática de archivos, la explotación de vulnerabilidades del navegador o la ejecución de contenido malicioso.

El principal punto de atención es que la laptop continúa conectada a la red corporativa. El área de TI debe determinar si el enlace provocó alguna actividad maliciosa y si existe riesgo para otros equipos o para el correo empresarial.

## 3. Acciones de respuesta recomendadas

1. **Contener el posible incidente.** Solicitar al área de TI que aísle temporalmente la laptop de la red corporativa, siguiendo el procedimiento de respuesta de la organización. No apagarla ni borrar archivos antes de recibir instrucciones, para preservar posibles evidencias.

2. **Investigar el enlace.** Revisar el correo original, el remitente, la dirección del enlace, los registros del navegador y las alertas del antivirus o EDR para identificar descargas, redirecciones o procesos sospechosos.

3. **Proteger el correo empresarial.** Buscar mensajes similares en la organización y bloquear el remitente o dominio malicioso cuando la investigación lo confirme. Revisar los registros de acceso para detectar actividad inusual.

4. **Documentar y recuperar.** Registrar la cronología, las evidencias, las medidas aplicadas y los resultados. Restablecer la conexión del equipo solo después de que TI determine que es seguro.

## 4. Clasificación inicial del riesgo

- **Confidencialidad:** existe un riesgo potencial, pero no hay evidencia proporcionada de robo de credenciales.
- **Integridad:** debe comprobarse si se descargaron archivos o se ejecutó código.
- **Disponibilidad:** no se reporta interrupción del servicio.
- **Prioridad:** atender el incidente de inmediato, especialmente porque el dispositivo permanece conectado a la red.

Importante: el nivel de riesgo es provisional. Hacer clic en un enlace no demuestra por sí solo que el equipo esté comprometido.

## 5. Referencias para el procedimiento

- NIST: consultar la publicación SP 800-61 Rev. 3, sobre preparación, detección, respuesta y recuperación ante incidentes de ciberseguridad.
- CISA: consultar sus recomendaciones para reconocer, reportar y responder al phishing.

Para orientar el siguiente paso, ¿este caso forma parte de tu laboratorio de ciberseguridad y necesitas elaborar un informe formal del incidente, una matriz de riesgos o un procedimiento de respuesta paso a paso?

*Nota: la respuesta original también incluía un mensaje sobre el plan gratuito de ChatGPT. Se omite aquí porque no forma parte del análisis del incidente.*

---

## Entrada 2 — Reporte con información faltante

### Texto de entrada

Hola, creo que alguien entró a mi correo porque me llegó un aviso extraño de inicio de sesión. No sé exactamente cuándo ocurrió ni desde qué dispositivo. Ya cambié mi contraseña, pero sigo preocupado porque utilizo esa cuenta para asuntos del trabajo. No sé si alguien descargó información o si otras cuentas están afectadas.

### Respuesta original de ChatGPT

Lo primero: hiciste bien en cambiar tu contraseña, pero como utilizas ese correo para asuntos del trabajo, conviene tratarlo como un posible incidente de ciberseguridad hasta comprobar qué ocurrió.

No significa necesariamente que alguien haya conseguido entrar. El aviso podría corresponder a un intento de acceso bloqueado, pero también podría indicar que alguien inició sesión correctamente. Por ahora, tampoco sabemos si se descargó información o si otras cuentas están comprometidas.

## Paso 1. Protege tu cuenta y el acceso al trabajo

Te recomiendo seguir este orden:

1. **Cierra las sesiones desconocidas.** Entra directamente en la página o aplicación oficial de tu proveedor de correo. Revisa la actividad reciente y cierra las sesiones o dispositivos que no reconozcas. Si existe la opción de cerrar todas las sesiones, considera utilizarla.

2. **Verifica los métodos de recuperación.** Comprueba que el teléfono, el correo de recuperación y los métodos de autenticación de dos factores sean tuyos. Activa la autenticación multifactor si todavía no la tienes.

3. **Revisa las reglas y los permisos del correo.** Busca reglas de reenvío, filtros, respuestas automáticas, aplicaciones conectadas y permisos que no hayas configurado. Alguien podría mantener acceso a los mensajes incluso después de cambiar la contraseña.

4. **Informa al área de TI de tu trabajo.** Comunica el aviso sospechoso y el cambio de contraseña. Pide que revisen los registros de inicio de sesión, las sesiones activas y el acceso a archivos o mensajes. Si la cuenta es corporativa, sigue sus instrucciones antes de realizar cambios adicionales en el dispositivo de trabajo.

## Paso 2. Comprueba si hubo un acceso real

Puedes consultar estas guías oficiales según el tipo de cuenta:

- Outlook o Microsoft 365: [Revisar la actividad reciente](https://support.microsoft.com/es-es/account-billing/security/what-is-the-recent-activity-page). Si es una cuenta laboral, revisa también [la actividad de inicio de sesión de trabajo o escuela](https://support.microsoft.com/es-es/account-billing/work-school/view-your-work-or-school-account-sign-in-activity-from-my-sign-ins).
- Gmail o Google Workspace: [Proteger una cuenta de Google comprometida](https://support.google.com/accounts/answer/6294825?hl=es).

Busca inicios de sesión exitosos que no reconozcas, cambios de seguridad, dispositivos desconocidos y accesos a aplicaciones. Guarda capturas de los avisos y las horas, si están disponibles, para que TI pueda investigarlos. Ten en cuenta que la ubicación puede ser aproximada y que el historial no siempre muestra toda la actividad.

## Paso 3. Comprueba si otras cuentas están en riesgo

- Si reutilizabas la misma contraseña en otros servicios, cámbiala también en esos servicios.
- Revisa las cuentas que utilizan ese correo para recuperar contraseñas.
- Si observas correos enviados que no reconoces, reglas extrañas o acceso inesperado a archivos compartidos, comunícalo inmediatamente a TI.
- No borres mensajes de alerta ni restablezcas el equipo antes de que TI te indique cómo preservar la información necesaria para la investigación.

Importante: cambiar la contraseña es una buena medida, pero no demuestra por sí solo que se haya eliminado todo acceso no autorizado.

## Vamos paso a paso

Para darte instrucciones concretas para tu cuenta, necesito saber una cosa:

1. ¿Qué tipo de correo utilizas?
   - Outlook / Microsoft 365 del trabajo.
   - Gmail / Google Workspace del trabajo.
   - Correo personal (Outlook, Gmail u otro).
   - Otro proveedor o no estoy seguro.

2. ¿Qué decía el aviso de inicio de sesión?
   - Intento bloqueado o acceso denegado.
   - Inicio de sesión exitoso.
   - No lo recuerdo o no estoy seguro.

No compartas tu contraseña, códigos de verificación ni enlaces privados de acceso. Con esos dos datos podremos continuar con una revisión más específica.

*Nota: la respuesta original también incluía elementos visuales, enlaces con parámetros de seguimiento y un mensaje sobre el plan gratuito de ChatGPT. Los elementos visuales y el mensaje promocional se omitieron para facilitar su lectura en Markdown.*

---

## Entrada 3 — Reporte contradictorio o ambiguo

### Texto de entrada

Un empleado reportó que su computadora fue infectada por un archivo sospechoso descargado de un correo. Afirma que nunca abrió el archivo, pero también comenta que lo ejecutó para comprobar qué contenía. El antivirus indica que no encontró amenazas, aunque el usuario menciona que aparecieron ventanas extrañas. No se sabe si el equipo se conectó a otros sistemas ni si hubo pérdida de información.

### Respuesta original de ChatGPT

Este caso puede documentarse como un incidente de ciberseguridad por posible ejecución de malware mediante un archivo recibido por correo electrónico. Aunque el antivirus no detectó amenazas, las ventanas extrañas y las contradicciones en el relato del empleado justifican investigar el equipo antes de descartar una infección.

## Reporte del incidente de ciberseguridad

### Incidente: posible infección por malware

**Estado:** En investigación.

### 1. Descripción del incidente

Un empleado reportó la descarga de un archivo sospechoso proveniente de un correo electrónico. Inicialmente afirmó que nunca lo abrió, pero posteriormente indicó que lo ejecutó para comprobar su contenido. Después de este hecho, observó ventanas extrañas en su computadora.

### 2. Activo afectado

Computadora del empleado. Se desconoce si otros dispositivos o sistemas fueron afectados.

### 3. Indicadores observados

- Archivo sospechoso descargado desde un correo electrónico.
- Posible ejecución del archivo.
- Aparición de ventanas inusuales.
- Antivirus sin detecciones reportadas.

### 4. Información desconocida

- Tipo de malware, si existe.
- Conexiones con otros equipos o servidores.
- Posible robo, modificación o pérdida de información.
- Persistencia del archivo o de procesos maliciosos.

### 5. Nivel de riesgo preliminar

**Alto, sujeto a evaluación técnica.** La posible ejecución del archivo y los comportamientos anormales justifican medidas preventivas inmediatas. Esto no confirma que exista malware.

## Acciones de respuesta recomendadas

1. **Contener:** desconectar temporalmente el equipo de la red corporativa y del Wi-Fi, siguiendo el procedimiento de respuesta de la organización. No apagarlo automáticamente si el equipo de seguridad necesita preservar evidencias volátiles.

2. **Preservar evidencias:** guardar el correo original, el archivo sospechoso, la hora aproximada de descarga y ejecución, capturas de las ventanas y registros de seguridad. No volver a ejecutar el archivo.

3. **Investigar:** solicitar al área de TI que examine procesos, conexiones de red, registros del sistema y alertas del antivirus o EDR. La ausencia de detecciones no descarta una infección.

4. **Evaluar el alcance:** revisar posibles conexiones a servidores, carpetas compartidas y otros equipos, así como indicios de extracción o modificación de datos.

5. **Remediar y recuperar:** eliminar la amenaza si se confirma, restablecer credenciales desde un dispositivo confiable cuando corresponda y restaurar el equipo siguiendo el procedimiento autorizado.

## Relación con el laboratorio de ciberseguridad

Este escenario permite evaluar si un modelo de IA identifica correctamente las contradicciones, evita afirmar que la infección está confirmada y recomienda medidas de contención y análisis sin inventar datos.

Importante: los datos anteriores corresponden únicamente al escenario proporcionado. No se ha realizado un análisis técnico real del equipo.

Si estás trabajando en tu laboratorio de Mejora iterativa de prompts con métricas, puedes utilizar este caso como una entrada de prueba para evaluar la precisión, la detección de incertidumbre y la calidad de las recomendaciones de respuesta a incidentes.

---

## Observaciones iniciales de la iteración

Las tres respuestas muestran que el modelo puede generar análisis extensos y recomendaciones prácticas. Sin embargo, también incluyen información adicional y formatos diferentes, lo que dificulta comparar las clasificaciones de manera uniforme.

Las respuestas se evaluarán con los siguientes criterios:

| Criterio | Descripción | Escala |
|---|---|---|
| C1 — Completitud | Identifica el tipo de incidente, la severidad, el activo afectado y la primera acción recomendada. | 0–2 |
| C2 — Formato | Presenta los campos de forma clara y organizada. | 0–2 |
| C3 — Manejo de incertidumbre | Reconoce los datos faltantes y las contradicciones sin inventar hechos. | 0–2 |

Las puntuaciones se registrarán en la hoja de cálculo durante el Paso 2.2. No se modificarán las respuestas originales para conservar la validez de la línea base.
