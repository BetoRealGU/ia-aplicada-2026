# Iteración 2: Añadir contexto al prompt

## Objetivo

Mejorar la clasificación de reportes de incidentes de ciberseguridad mediante la incorporación de contexto sobre el origen de los reportes, las categorías de incidentes disponibles y los niveles de severidad permitidos.

## Prompt utilizado

Eres analista de seguridad de primer nivel en un centro de operaciones. Tu lector es un técnico que atenderá el incidente y necesita información precisa.

Contexto: este texto proviene de un formulario que llenan usuarios sin conocimientos técnicos. Los tipos de incidente posibles son: acceso no autorizado, phishing, malware, pérdida de dispositivo, otro. Las severidades posibles son: baja, media, alta.

Clasifica este reporte de incidente:

[pega aquí la entrada]

## Entrada 1: Reporte de phishing

### Respuesta obtenida

**Clasificación del incidente de seguridad**

| Campo | Clasificación |
|---|---|
| Tipo de incidente | Phishing |
| Severidad | Media |
| Fecha y hora | Lunes, 10:30 a. m. |
| Activo afectado | Laptop corporativa |
| Sistema o servicio involucrado | Correo empresarial |
| Descripción del incidente | El empleado recibió un correo fraudulento que solicitaba verificar su contraseña mediante un enlace sospechoso. Hizo clic en el enlace, pero no ingresó sus credenciales. |
| Impacto confirmado | No se reporta exposición de credenciales ni acceso no autorizado confirmado. |
| Estado del incidente | Reportado al área de TI; pendiente de investigación. |
| Riesgo principal | Posible descarga de malware o redirección a un sitio malicioso tras hacer clic en el enlace. |
| Acción recomendada | Revisar el historial del navegador, verificar posibles descargas, analizar la laptop y determinar si es necesario aislarla de la red. |

**Justificación de la severidad:** Se clasifica como media porque el usuario hizo clic en un enlace sospechoso desde un equipo corporativo conectado a la red, aunque no ingresó sus credenciales.

**Nota para el técnico:** La presencia de malware no está confirmada. Es necesario investigar el enlace y el equipo antes de determinar si hubo una infección o un compromiso de seguridad.

## Entrada 2: Posible acceso no autorizado

### Respuesta obtenida

**Clasificación del incidente de seguridad**

| Campo | Clasificación |
|---|---|
| Tipo de incidente | Acceso no autorizado (sospecha) |
| Severidad | Alta |
| Activo afectado | Cuenta de correo electrónico utilizada para asuntos laborales |
| Descripción | El usuario recibió una notificación inusual de inicio de sesión y sospecha que alguien accedió a su cuenta. Cambió su contraseña, pero desconoce si se descargó información o si otras cuentas resultaron afectadas. |
| Evidencia disponible | Notificación extraña de inicio de sesión y cambio de contraseña realizado por el usuario. |
| Información faltante | Fecha y hora del acceso, dispositivo y ubicación de origen, confirmación de si el inicio de sesión fue exitoso, posible exposición de información y afectación de otras cuentas. |
| Acciones recomendadas | Revisar los registros de inicio de sesión, cerrar sesiones activas, verificar los métodos de recuperación y la autenticación multifactor, y comprobar si existen accesos o actividades sospechosas. |
| Estado del incidente | Pendiente de investigación |

**Justificación de la clasificación:** Se clasifica como un posible caso de acceso no autorizado porque el usuario recibió una alerta de inicio de sesión que no reconoce. Se asigna severidad alta de manera preventiva debido al posible riesgo para una cuenta utilizada en el trabajo y a la incertidumbre sobre una posible exposición de información. La severidad debe confirmarse durante la investigación, ya que todavía no se ha comprobado que el acceso haya sido exitoso.

## Entrada 3: Archivo sospechoso y posible malware

### Respuesta obtenida

| Campo | Clasificación |
|---|---|
| Tipo de incidente | Malware |
| Severidad | Alta |
| Activo afectado | Computadora corporativa (no especificado si lo es) |
| Descripción | El usuario descargó y ejecutó un archivo sospechoso recibido por correo electrónico. Posteriormente, observó ventanas extrañas, aunque el antivirus no detectó amenazas. |
| Indicadores de riesgo | Ejecución de archivo sospechoso y comportamiento inusual del equipo. |
| Impacto confirmado | No determinado. No hay evidencia confirmada de pérdida de información ni de propagación a otros sistemas. |
| Justificación | La ejecución del archivo y las ventanas extrañas sugieren una posible infección por malware. La ausencia de alertas del antivirus no descarta una infección. |
| Acción recomendada | Desconectar temporalmente el equipo de la red, escalar el incidente al equipo de seguridad y realizar un análisis técnico del dispositivo. |

**Nota:** La severidad alta es provisional debido a la ejecución del archivo sospechoso y al comportamiento inusual del equipo. Debe confirmarse después de evaluar el impacto real y el alcance del incidente.

## Evaluación de resultados

| Entrada | C1: Completitud | C2: Formato | C3: Incertidumbre | Total |
|---|---:|---:|---:|---:|
| Entrada 1 | 2 | 2 | 2 | 6/6 |
| Entrada 2 | 2 | 2 | 1 | 5/6 |
| Entrada 3 | 2 | 2 | 1 | 5/6 |
| **Total** | **6/6** | **6/6** | **4/6** | **16/18** |

## Conclusión

La incorporación de contexto ayudó a delimitar las categorías de incidentes y los niveles de severidad disponibles. Las respuestas presentaron información organizada, identificaron los activos afectados y propusieron acciones de investigación. Sin embargo, todavía se observan oportunidades de mejora en el manejo de la incertidumbre, especialmente cuando se asigna una severidad alta sin evidencia suficiente o cuando el reporte original contiene contradicciones.
