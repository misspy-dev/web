# `misspy.Bot.notas`
## notas
Obtenga una lista de notas.

Nombre | Tipo | Predeterminado | Descripción |
| - | - | - | - |
| local | bool | False | Solo recupera notas creadas localmente.<br> |
| respuesta | bool | | Establezca en `True` para obtener solo respuestas, `False` para obtener no respuestas.Si no establece el valor, recibirá la nota independientemente de si es una respuesta o no.<br> |
| renote | bool | | Establezca en `True` para obtener solo renotes, `False` para obtener no renotes.Si no establece un valor, obtendrá la nota independientemente de si es una renota o no.|
| withFiles | bool | | Establezca en `True` para obtener solo notas con archivos adjuntos, `False` para obtener solo notas sin archivos adjuntos.Si no establece un valor, recibirá notas con o sin archivos adjuntos.|
| encuesta | bool | | Establezca en `True` para obtener solo notas con encuestas, `False` para obtener solo notas sin encuestas.Si no establece un valor, obtendrá notas con o sin votos.|
| límite | int | 10 | Especifica el número máximo de notas a recuperar.|
|sinceId | str | | Si se especifica, devuelve notas cuya identificación es mayor que ese valor.<br> |
| UntilId | str | | Si se especifica, devuelve notas cuya identificación es menor que ese valor.<br> |

## notas_create
Crea notas.Responder y Renotar también se realizan con esta función.

Nombre | Tipo | Predeterminado | Descripción |
| - | - | - | - |
| visibilidad | str<br>(`public` `home` `followers` `especificado`) | public | Rango de visibilidad de la nota.|
| visibleUserIds | list<br>(str) | | Lista de ID de usuarios que pueden ver la nota.Se aplica solo cuando se especifica visibilidad.<br> |
text | str &#124; Ninguno | | El cuerpo de la nota.<br> |
| cw | str &#124; Ninguno | | CW de la nota.|
| localOnly | bool | False | True para publicar solo localmente.|
| noExtractMentions | bool | False | Si es verdadero, no extraiga menciones del cuerpo.|
| noExtractHashtags | bool | False | True no extrae hashtags del cuerpo.|
| noExtractEmojis | bool | False | Si es verdadero, no extraiga emojis del cuerpo.<br> |
| fileIds | list<br>(str) | | Los identificadores de los archivos a adjuntar.<br> |
| respuestaId | str &#124; Ninguno | | La identificación de la nota a responder.|
| renoteId | str &#124; Ninguno | | La identificación de la nota a renotar.|
| channelId | str &#124; Ninguno | | La identificación del canal en el que publicar.<br> |
| encuesta | objeto &#124; Ninguno | | Parámetros para la votación.|

### tipos

Nombre | Tipo | Predeterminado | Descripción |
| - | - | - | - |
| opciones | lista | ||
| multiple | bool | Falso | Verdadero para permitir selecciones múltiples.<br> |
| expiresAt | int &#124; Ninguno | | Fecha límite para la votación.Especificado en segundos de época.<br> |
| expiredAfter | int &#124;Si se especifica con expiresAt, expiresAt tiene prioridad.<br> |

<!--
Nombre | Tipo | Predeterminado | Descripción |
| - | - | - | - |
| | | | |
| | | | |
| | | | |
-->
## notas_delete
Eliminar notas.

Nombre | Tipo | Predeterminado | Descripción |
| - | - | - | - |
| noteId | str | | La identificación de la nota.|