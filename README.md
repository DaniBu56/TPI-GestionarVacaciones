# TPI-GestionarVacaciones
#TPI OE Gestionar Vacaciones BOT

# Descripción
Este proyecto corresponde al Trabajo Práctico Integrador (TP2) de la materia **Organización Empresarial** de la UTN, para la carrera de Tecnicatura en Programación.  
El objetivo esidentificar un proceso administrativo crítico dentro de una organización, en mi caso elegí Gestión de vacaciones mediante un chatbot en Telegram, siguiendo el modelo BPMN 2.0.
**Lenguaje utilizado**: Python  
**Plataforma escogida**: Telegram Bot API  
**Librerías**:  
  - `python-telegram-bot` 
  - `pandas`  
**Estructura del repositorio**:
Nombre: TPI-GestionarVacaciones/
VacacionesTPI_Bot: estructura del bot
Dias_disponibles_trabajadores.csv: Base de datos simulada con nombre de los trabajadores de la nómina y días disponibles de vacaciones
Modelado de procesos con BPMN.png: Diagrama BPMN 2.0
requirements.txt: Librerías necesarias instaladas
README.md: Documentación del proyecto

**Funcionalidad del bot**: 
El bot utiliza el archivo `dias_disponibles_trabajadores.csv` como base de datos simulada. 
Cada vez que un usuario solicita vacaciones, el bot consulta este archivo con `pandas` y valida los días disponibles. Este modelo refleja el flujo completo del proceso, incluyendo tanto el camino exitoso como los posibles rechazos por falta de saldo o imposibilidad de tomar esas fechas para la operación, garantizando coherencia entre el diseño del negocio y la futura implementación técnica.
El proceso modelado corresponde a la Solicitud de Vacaciones realizada por un trabajador a través de Telegram y procesado por el Telegram bot. El flujo inicia con la interacción del trabajador, quien ingresa su solicitud de días de vacaciones. El sistema consulta la base de datos y valida el saldo disponible. 
Si el saldo es insuficiente, se notifica el error al colaborador y la solicitud se rechaza, debiendo iniciar nuevamente el proceso. 
Si el saldo es suficiente, la solicitud se envía al Manager, quien revisa y decide su aprobación mediante botones. 
En caso de rechazo, se notifica al trabajador y el proceso finaliza. 
En caso de aprobación, la solicitud se remite a RRHH para la validación final. 
Finalmente, RRHH aprueba y registra la solicitud en el sistema de RRHH, concluyendo el proceso, o rechaza la solicitud.
Este diagrama refleja las decisiones críticas y los actores involucrados (Trabajador, Telegram bot, Manager y RRHH), siguiendo el estándar BPMN 2.0. 
Para poder realizar las validaciones en vivo, tuve que ajustar el bot para que consulte al usuario su nombre, que será validado por el bot con la lista de días de disponibilidad, y posteriormente el trabajador solicitará los días que precisa. 

**Ejemplo de estructura del CSV**: 
trabajador,dias_disponibles
Alejandro,14
Ana,14
Andres,14

**Para diccionario de datos, manual de usuario y pruebas, revisar el pdf compartido**

**Seguridad del GitHub**
Para la conexión entre Visual Studio Code / GitHub Desktop y el repositorio remoto se utilizó un **Personal Access Token (PAT)**.  
Todos los cambios se registraron mediante commits con descripción de los cambios y mensajes claros que documentan la evolución del proyecto.  
De esta manera, se cumple con las buenas prácticas de seguridad y versionado exigidas en la consigna.

