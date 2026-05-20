# Secure To-Do App

## 1. Descripción de la aplicación
Este proyecto reutiliza una aplicación web tipo To-Do List
como base para documentar la ejecución de un ciclo de vida
de desarrollo seguro, conocido como S-SDLC.

La aplicación permite añadir tareas pendientes desde una in-
terfaz web sencilla. Se ejecuta mediante Docker y Docker 
Compose, lo que facilita su despliegue, reproducción y pruebas.

## 2. Objetivo de la actividad
El objetivo es seleccionar una aplicación funcional, crear una
estructura de proyecto adecuada y añadir documentación relacio-
nada con la seguridad durante las diferentes fases del SDLC.

## 3. Tecnologías utilizadas

- Docker
- Docker Compose
- Node.js
- Express
- SQLite
- Git y GitHub

## 4. Estructura del proyecto

```text
    secure-todo-app/
    ├── app/
    ├── docs/
    ├── tests/
    ├── docker-compose.yml
    ├── .gitignore
    └── README.md
```

## 5. Cómo ejecutar la aplicación

- Requisitos: 
  - Docker Desktop instalado
  - Docker Compose disponible
- Ejecución: docker compose up --build
  - la aplicación queda disponible en: http://localhost:3001
  - para detenerla: CTRL + C docker compose down
  
## 6. Consideraciones de seguridad
Durante el diseño del proyecto se han considerado las siguientes 
medidas:
    - Validación de entradas introducidas por el usuario
    - Prevención de XSS
    - Revisión de dependencias vulnerables
    - Uso de contenedores Docker para aislar el entorno
    - No inclusión de secretos dentro del repositorio
    - Uso de .gitignore para evitar subir archivos innecesarios
    - Documentación del proceso de desarollo seguro

## 7. Ejecución del S-SDLC

1. Planificación
Se selecciona una aplicación To-Do funcional y ejecutable mediante Docker
2. Requisitos de seguridad
Se identifican requisitos como validación de entradas, protección frente a 
XSS, revisión de dependencias y gestión segura del entorno.
3. Diseño seguro
Se crea una estructura separada para aplicación, documentación y pruebas
4. Implementación
Se configura la aplicación en Docker y se documentan las medidas de seguridad
necesarias
5. Pruebas
Se comprueba que la aplicación se ejecuta correctamente y que puede usarse desde
el navegador
6. Despliegue
El despliegue se realiza localmente mediante Docker Compose
7. Mantenimiento
Se recomienda revisar dependencias, actualizar imágenes Docker y repetir pruebas
de seguridad periódicamente

## 8. Evidencias
Se han obtenido evidencias de:
- Aplicación ejecutándose en Docker
- Aplicación accesible desde navegador
- Estructura del proyecto en PyCharm
- Configuración mediante Docker Compose

