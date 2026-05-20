# Secure To-Do App

## Repositorio GitHub
https://github.com/valletorrome/secure-todo-app/tree/main

## Miembros del grupo
Esta actividad se realiza de forma individual.

| Miembro | Repositorio actividad anterior |
|---|---|
| Valle Torromé | https://github.com/valletorrome/secure-todo-app/tree/main |

## 1. Descripción de la aplicación
Este proyecto reutiliza una aplicación web tipo To-Do List
como base para documentar la ejecución de un ciclo de vida
de desarrollo seguro, conocido como S-SDLC.

La aplicación permite añadir tareas pendientes desde una in-
terfaz web sencilla. Se ejecuta mediante Docker y Docker 
Compose, lo que facilita su despliegue, reproducción y pruebas.

## 2. Objetivo de la actividad 2
El objetivo de esta segunda actividad es continuar el proyecto
iniciado anteriormente e incorporar una visión DevSecOps al
desarrollo de la aplicación.

Para ello, se parte de la Web-App tipo To-Do List creada en la
actividad anterior, se revisan las medidas de seguridad aplica-
das durante el S-SDLC y se propone una integración de controles
de seguridad dentro del flujo de desarrollo mediante GitHub, Docker
y análisis de dependencias.

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

## 8. Aplicación de DevSecOps
DevSecOps consiste en integrar la seguridad dentro de todas las fases del desarrollo,
en lugar de tratarla como una revisión final.

En este proyecto, DevSecOps se aplica mediante la combinación de desarrollo seguro,
control de versiones, contenedores Docker y revisión de dependencias.

## Flujo DevSecOps

1. Planificación de requisitos funcionales y de seguridad
2. Diseño seguro de la estructura del proyecto
3. Implementación de la aplicación web
4. Subida del código a GitHub
5. Revisión de dependencias vulnerables mediante `npm audit`
6. Construcción del contenedor Docker
7. Pruebas de ejecución local
8. Mantenimiento y actualización del proyecto

### Pipeline DevSecOps propuesto

```text

Planificación
     ↓
Diseño seguro
     ↓
Desarrollo
     ↓
Repositorio GitHub
     ↓
Análisis de dependencias
     ↓
Construcción Docker
     ↓
Pruebas
     ↓
Despliegue local
     ↓
Mantenimiento
```
## 8. Herramientas DevSecOps utilizadas o propuestas

- GitHub para control de versiones
- Docker para crear un entorno reproducible
- Docker Compose para facilitar la ejecución
- .gitignore para evitar subir archivos innecesarios
- npm audit para revisar vulnerabilidades en dependencias
- Documentación de pruebas funcionales y de seguridad

## 9. Diagrama S-SDLC y DevSecOps

```text

┌────────────────────┐
│  Planificación     │
└─────────┬──────────┘
          ↓
┌────────────────────┐
│ Requisitos seguros │
└─────────┬──────────┘
          ↓
┌────────────────────┐
│  Diseño seguro     │
└─────────┬──────────┘
          ↓
┌────────────────────┐
│ Implementación     │
└─────────┬──────────┘
          ↓
┌────────────────────┐
│ Revisión seguridad │
└─────────┬──────────┘
          ↓
┌────────────────────┐
│ Construcción Docker│
└─────────┬──────────┘
          ↓
┌────────────────────┐
│ Pruebas            │
└─────────┬──────────┘
          ↓
┌────────────────────┐
│ Despliegue local   │
└─────────┬──────────┘
          ↓
┌────────────────────┐
│ Mantenimiento      │
└────────────────────┘
```

## 10. Evidencias
Se han obtenido evidencias de:
- Aplicación ejecutándose en Docker
- Aplicación accesible desde navegador
- Estructura del proyecto en PyCharm
- Configuración mediante Docker Compose
- Repositorio publicado en GitHub
- Documentación S-SDLC
- Propuesta de flujo DevSecOps
- Diagrama S-SDLC + DevSecOps
