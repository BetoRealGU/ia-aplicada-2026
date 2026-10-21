# Iteración 3: Añadir formato de salida

## Objetivo

Estandarizar las respuestas de clasificación de incidentes de ciberseguridad mediante una tabla con campos definidos e instrucciones explícitas para manejar información faltante.

## Prompt utilizado

Eres analista de seguridad de primer nivel en un centro de operaciones. Tu lector es un técnico que atenderá el incidente y necesita información precisa.

Contexto: este texto proviene de un formulario que llenan usuarios sin conocimientos técnicos. Los tipos de incidente posibles son: acceso no autorizado, phishing, malware, pérdida de dispositivo, otro. Las severidades posibles son: baja, media, alta.

Clasifica este reporte de incidente utilizando exactamente la siguiente tabla:

| Campo | Valor |
|---|---|
| Tipo de incidente | |
| Severidad | |
| Activo afectado | |
| Primera acción recomendada | |
| Información faltante | |

Instrucciones:
- Utiliza únicamente las categorías y severidades permitidas.
- Si un dato no puede determinarse a partir del reporte, escribe "NO ESPECIFICADO".
- En "Información faltante", indica qué datos se necesitan para confirmar la clasificación o atender el incidente.
- No inventes información ni presentes sospechas como hechos confirmados.
- La primera acción recomendada debe ser concreta y priorizar la seguridad.

Clasifica este reporte de incidente:

[pega aquí la entrada]

## Entrada 1: Reporte de phishing

### Respuesta obtenida

- **Tipo de incidente:** phishing
- **Severidad:** media
- **Activo afectado:** laptop corporativa con acceso al correo empresarial
- **Primera acción recomendada:** desconectar temporalmente la laptop de la red corporativa y solicitar al área de TI que inspeccione el enlace y el equipo.
- **Información faltante:** URL completa, dominio y remitente del correo, fecha exacta, resultados del análisis de seguridad y confirmación de posibles descargas, redireccionamientos o actividad inusual en la cuenta.

## Entrada 2: Posible acceso no autorizado

### Respuesta obtenida

- **Tipo de incidente:** acceso no autorizado
- **Severidad:** media
- **Activo afectado:** cuenta de correo electrónico utilizada para asuntos del trabajo
- **Primera acción recomendada:** verificar la actividad reciente de inicio de sesión, cerrar las sesiones activas desconocidas y activar la autenticación multifactor.
- **Información faltante:** fecha y hora del inicio de sesión sospechoso, dispositivo y ubicación de origen, detalles del aviso, evidencia de acceso o descarga de información, estado de las sesiones y posible afectación de otras cuentas.

## Entrada 3: Archivo sospechoso

### Respuesta obtenida

- **Tipo de incidente:** malware
- **Severidad:** media
- **Activo afectado:** computadora del empleado
- **Primera acción recomendada:** aislar la computadora de la red y notificar al equipo de seguridad para analizar el archivo y el sistema.
- **Información faltante:** nombre y ubicación del archivo, remitente y correo de origen, fecha y hora de ejecución, alertas y registros del antivirus, detalles de las ventanas extrañas, conexiones con otros sistemas y evidencia de posible pérdida o exposición de información.

## Evaluación de resultados

| Entrada | C1: Completitud | C2: Formato | C3: Incertidumbre | Total |
|---|---:|---:|---:|---:|
| Entrada 1 | 2 | 2 | 2 | 6/6 |
| Entrada 2 | 2 | 2 | 2 | 6/6 |
| Entrada 3 | 2 | 2 | 1 | 5/6 |
| **Total** | **6/6** | **6/6** | **5/6** | **17/18** |

## Conclusión

El formato de salida específico produjo respuestas más uniformes y facilitó la identificación del tipo de incidente, la severidad, el activo afectado, la primera acción recomendada y la información faltante. Sin embargo, todavía se puede mejorar la identificación explícita de contradicciones presentes en los reportes originales.
