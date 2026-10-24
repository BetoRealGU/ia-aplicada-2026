# Iteración 5: Análisis previo y manejo de contradicciones

## Objetivo

Mejorar la capacidad del modelo para distinguir entre hechos explícitos, inferencias seguras e información desconocida o contradictoria antes de clasificar un incidente de ciberseguridad.

## Prompt utilizado

Eres analista de seguridad de primer nivel en un centro de operaciones. Tu lector es un técnico que atenderá el incidente y necesita información precisa.

Contexto: este texto proviene de un formulario que llenan usuarios sin conocimientos técnicos. Los tipos de incidente posibles son: acceso no autorizado, phishing, malware, pérdida de dispositivo, otro. Las severidades posibles son: baja, media, alta.

Antes de clasificar el reporte, incluye una sección titulada **Análisis** con exactamente tres viñetas:

- **Información explícita:** hechos que el usuario menciona directamente.
- **Inferencias seguras:** conclusiones razonables basadas en el reporte, sin presentarlas como hechos confirmados.
- **Información no determinada o contradictoria:** datos desconocidos, insuficientes o contradictorios. Si el reporte contiene afirmaciones incompatibles, señálalas expresamente.

Después del análisis, clasifica el reporte utilizando exactamente esta tabla:

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
- Si hay contradicciones, no elijas una versión como verdadera sin evidencia.
- La primera acción recomendada debe ser concreta y priorizar la seguridad.

## Entrada 1: Reporte de phishing

### Entrada utilizada

El lunes a las 10:30 a. m., un empleado recibió un correo de phishing en su computadora de trabajo. El mensaje solicitaba verificar su contraseña mediante un enlace sospechoso. El empleado hizo clic, pero no ingresó sus credenciales. El equipo afectado es una laptop corporativa con acceso al correo empresarial. El incidente fue reportado al área de TI y el dispositivo continúa conectado a la red.

### Respuesta obtenida

#### Análisis

- **Información explícita:** El lunes a las 10:30 a. m., un empleado recibió un correo de phishing en su laptop corporativa. El mensaje solicitaba verificar la contraseña mediante un enlace sospechoso. El empleado hizo clic, pero no ingresó sus credenciales. La laptop tiene acceso al correo empresarial, el incidente fue reportado a TI y el equipo continúa conectado a la red.
- **Inferencias seguras:** El incidente se clasifica como phishing porque el correo intentaba obtener información de autenticación mediante un enlace sospechoso. Aunque el empleado afirma no haber ingresado sus credenciales, es necesario verificar si el enlace provocó alguna descarga, redirección maliciosa o ejecución de contenido. Conviene aislar temporalmente el equipo de la red mientras se realiza una revisión inicial.
- **Información no determinada o contradictoria:** No se especifica la dirección del remitente, la URL del enlace ni si el antivirus detectó alguna amenaza. Tampoco se confirma si hubo descargas, ejecución de archivos o actividad sospechosa posterior al clic. No se identifican contradicciones explícitas en el reporte.

#### Clasificación del incidente

| Campo | Valor |
|---|---|
| Tipo de incidente | Phishing |
| Severidad | Media |
| Activo afectado | Laptop corporativa con acceso al correo empresarial |
| Primera acción recomendada | Desconectar temporalmente la laptop de la red corporativa y notificar al equipo de seguridad para analizar el enlace, revisar posibles descargas y verificar si hubo actividad maliciosa. |
| Información faltante | Dirección del remitente, URL completa del enlace, encabezados del correo, fecha y hora exactas con zona horaria, registros de navegación, alertas del antivirus o EDR, posibles descargas o ejecuciones, actividad posterior al clic y confirmación de que no hubo exposición de credenciales ni acceso no autorizado. |

## Entrada 2: Posible acceso no autorizado

### Entrada utilizada

Hola, creo que alguien entró a mi correo porque me llegó un aviso extraño de inicio de sesión. No sé exactamente cuándo ocurrió ni desde qué dispositivo. Ya cambié mi contraseña, pero sigo preocupado porque utilizo esa cuenta para asuntos del trabajo. No sé si alguien descargó información o si otras cuentas están afectadas.

### Respuesta obtenida

#### Análisis

- **Información explícita:** El usuario recibió un aviso extraño de inicio de sesión en su correo y sospecha que alguien pudo haber accedido a la cuenta. Desconoce cuándo ocurrió y desde qué dispositivo. Ya cambió su contraseña. Utiliza esa cuenta para asuntos laborales y desconoce si se descargó información o si otras cuentas están afectadas.
- **Inferencias seguras:** El aviso podría indicar un intento de acceso o un acceso no autorizado a la cuenta. El cambio de contraseña es una medida de protección ya realizada, pero no confirma que la cuenta esté completamente segura. Debido al uso laboral del correo, existe un posible riesgo para la información de trabajo.
- **Información no determinada o contradictoria:** No se ha confirmado que alguien haya accedido exitosamente a la cuenta. Se desconocen el origen del inicio de sesión, la fecha y hora, el dispositivo utilizado, la posible descarga de información y la afectación de otras cuentas. No se identifican afirmaciones contradictorias en el reporte.

#### Clasificación del incidente

| Campo | Valor |
|---|---|
| Tipo de incidente | Acceso no autorizado |
| Severidad | Media |
| Activo afectado | Cuenta de correo electrónico utilizada para asuntos laborales |
| Primera acción recomendada | Revisar los registros de inicio de sesión y cerrar todas las sesiones activas desconocidas; verificar los métodos de recuperación y habilitar la autenticación multifactor. |
| Información faltante | Fecha y hora del aviso, dirección IP y ubicación del inicio de sesión, dispositivo involucrado, resultado del intento de acceso, actividad reciente de la cuenta, existencia de descargas o accesos a información laboral y posible afectación de otras cuentas. |

## Entrada 3: Posible malware con información contradictoria

### Entrada utilizada

Un empleado reportó que su computadora fue infectada por un archivo sospechoso descargado de un correo. Afirma que nunca abrió el archivo, pero también comenta que lo ejecutó para comprobar qué contenía. El antivirus indica que no encontró amenazas, aunque el usuario menciona que aparecieron ventanas extrañas. No se sabe si el equipo se conectó a otros sistemas ni si hubo pérdida de información.

### Respuesta obtenida

#### Análisis

- **Información explícita:** El empleado reporta una posible infección de su computadora por un archivo sospechoso descargado de un correo. Afirma que nunca abrió el archivo, pero también declara que lo ejecutó para comprobar su contenido. El antivirus no encontró amenazas y el usuario observó ventanas extrañas. Se desconoce si hubo conexiones con otros sistemas o pérdida de información.
- **Inferencias seguras:** La ejecución del archivo y la aparición de ventanas extrañas justifican sospechar de una posible infección por malware, aunque no está confirmada. Es necesario aislar preventivamente el equipo para reducir el riesgo de propagación o de actividad maliciosa.
- **Información no determinada o contradictoria:** Existe una contradicción entre afirmar que nunca abrió el archivo y declarar que lo ejecutó. El resultado negativo del antivirus no descarta por completo una infección. Se desconoce el archivo involucrado, el origen exacto del correo, el alcance del incidente y si hubo afectación a otros sistemas o pérdida de información.

#### Clasificación del incidente de seguridad

| Campo | Valor |
|---|---|
| Tipo de incidente | Malware |
| Severidad | Media |
| Activo afectado | Computadora del empleado |
| Primera acción recomendada | Aislar preventivamente la computadora de la red, desconectando Wi-Fi y Ethernet sin apagarla, y notificar al equipo de seguridad para su análisis. |
| Información faltante | Nombre, extensión y origen del archivo; remitente y contenido del correo; fecha y hora de descarga y ejecución; detalles de las ventanas extrañas; registros y resultados completos del antivirus; conexiones con otros sistemas; y evidencia de posible pérdida o alteración de información. |

## Evaluación de resultados

Se utilizaron los tres criterios de evaluación definidos en `criterios.md`:

- **C1: Completitud.** Evalúa si se incluyen los campos requeridos.
- **C2: Formato.** Evalúa si la respuesta sigue la estructura solicitada.
- **C3: Manejo de incertidumbre.** Evalúa si el modelo reconoce datos faltantes y contradicciones sin inventar hechos.

Cada criterio tiene una puntuación máxima de 2 puntos por entrada.

| Entrada | C1: Completitud | C2: Formato | C3: Manejo de incertidumbre | Total |
|---|---:|---:|---:|---:|
| Entrada 1 | 2/2 | 2/2 | 2/2 | 6/6 |
| Entrada 2 | 2/2 | 2/2 | 2/2 | 6/6 |
| Entrada 3 | 2/2 | 2/2 | 2/2 | 6/6 |
| **Total** | **6/6** | **6/6** | **6/6** | **18/18** |

## Observaciones

La sección de análisis ayudó a separar los hechos mencionados por el usuario de las inferencias y de la información que todavía debe confirmarse. En la Entrada 3, el modelo identificó explícitamente la contradicción sobre si el archivo fue abierto o ejecutado y aclaró que un resultado negativo del antivirus no descarta por completo una infección.

Las respuestas mantuvieron los campos requeridos y propusieron acciones preventivas. Sin embargo, las severidades asignadas deben entenderse como evaluaciones iniciales basadas en la información disponible, no como una confirmación definitiva del impacto real de los incidentes.

## Conclusión

La iteración 5 obtuvo una puntuación de 18/18. En comparación con las iteraciones anteriores, el análisis previo fortaleció el manejo de la incertidumbre y permitió identificar explícitamente una contradicción importante. Esta mejora hace que el prompt sea más útil para una clasificación inicial de incidentes, aunque las conclusiones deben ser verificadas por el equipo de seguridad.
