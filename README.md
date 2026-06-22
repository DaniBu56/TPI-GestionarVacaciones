# TPI-GestionarVacaciones
#TPI OE Gestionar Vacaciones BOT

# Descripción
Este proyecto corresponde al Trabajo Práctico Integrador (TP2) de la materia **Organización Empresarial** de la UTN, para la carrera de Tecnicatura en Programación.  
El objetivo esidentificar un proceso administrativo crítico dentro de una organización, en mi caso elegí Gestión de vacaciones mediante un chatbot en Telegram, siguiendo el modelo BPMN 2.0.
Lenguaje utilizado: Python  
Plataforma escogida: Telegram Bot API  
Librerías:  
  - `python-telegram-bot` 
  - `pandas`  
_Estructura del repositorio_:
Nombre: TPI-GestionarVacaciones/
VacacionesTPI_Bot: estructura del bot
Dias_disponibles_trabajadores.csv: Base de datos simulada con nombre de los trabajadores de la nómina y días disponibles de vacaciones
Modelado de procesos con BPMN.png: Diagrama BPMN 2.0
requirements.txt: Librerías necesarias instaladas
README.md: Documentación del proyecto

Funcionalidad del bot: 
El bot utiliza el archivo `dias_disponibles_trabajadores.csv` como base de datos simulada. 
Cada vez que un usuario solicita vacaciones, el bot consulta este archivo con `pandas` y valida los días disponibles.
Ejemplo de estructura del CSV: 
trabajador,dias_disponibles
Alejandro,14
Ana,14
Andres,14
