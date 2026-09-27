# Transformaciones y errores detectados

## Tabla de transformaciones

| Columna original | Qué le hice | Técnica | Por qué |
|---|---|---|---|
| `id` | Conservar | Conservación | Permite identificar cada registro sin usar el nombre. |
| `nombre` | Sustituir por `id_persona` | Seudonimización | Evita mostrar directamente el nombre de la persona. |
| `correo` | Eliminar | Eliminación | Es un identificador directo y no es necesario para analizar los accesos. |
| `telefono` | Eliminar | Eliminación | Es un identificador directo y no es necesario para el análisis. |
| `fecha_acceso` | Convertir en `semana` | Generalización | Se conserva información temporal sin mostrar la fecha exacta. |
| `hora_entrada` | Convertir en `franja` | Generalización | Se conserva el momento aproximado sin mostrar la hora exacta. |
| `area` | Conservar | Conservación | Es útil para analizar dónde ocurren los accesos. |
| `empresa` | Convertir en `tipo_empresa` | Generalización | Se conserva el tipo de empresa sin mostrar el nombre específico. |
| `motivo` | Conservar | Conservación | Es útil para analizar el motivo de los accesos. |
| `Motivo normalizado` | Eliminar | Eliminación | Era una columna auxiliar de limpieza. |
| `correo_valido` | Eliminar | Eliminación | Era una columna auxiliar de validación. |
| `telefono_valido` | Eliminar | Eliminación | Era una columna auxiliar de validación. |
| `fecha_valida` | Eliminar | Eliminación | Era una columna auxiliar de validación. |
| `hora_laboral` | Eliminar | Eliminación | Era una columna auxiliar de validación. |
| `telefono_normalizado` | Eliminar | Eliminación | Era una columna auxiliar utilizada durante la limpieza. |
| `id_persona` | Crear códigos como `P001`, `P002`, etc. | Seudonimización | Permite distinguir a las personas sin mostrar sus nombres. |

## Errores detectados

| id | campo | problema | acción |
|---|---|---|---|
| 3 | teléfono | Teléfono vacío | Se dejó en blanco |
| 4 | correo | Falta el dominio del correo | Se dejó en blanco |
| 6 | fecha | Mes inválido (13) | Se dejó en blanco |
| 15 | teléfono | Teléfono vacío | Se dejó en blanco |
| 19 | teléfono | Tiene menos de 10 dígitos | Se dejó en blanco |
| 21 | correo | Falta el dominio del correo | Se dejó en blanco |
