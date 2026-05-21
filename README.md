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

## 8.1. Herramientas automáticas de seguridad utilizadas
Para evaluar la seguridad de la aplicación se han utilizado diferentes herramientas
automáticas orientadas al análisis de vulnerabilidades, revisión de dependencias y 
comprobación de configuraciones inseguras.

Las herramientas seleccionadas han sido:

### 1. npm audit
Herramienta incluida en Node.js que permite analizar las dependencias del proyecto y
detectar vulnerabilidades conocidas.

Objetivo:
- Detectar librerías vulnerables
- Revisar dependencias inseguras
- Obtener alertas automáticas de seguridad

### 2. GitHub Actions
Se ha utilizado GitHub Actions para automatizar tareas relacionadas con seguridad y
DevSecOps mediante workflows.

Objetivo:
- Automatizar revisiones
- Ejecutar comprobaciones automáticamente
- Integrar seguridad dentro del ciclo DevSecOps

### 3. Docker
Docker permite ejecutar la aplicación dentro de un entorno aislado y reproducible.

Objetivo:
- Aislamiento de la aplicación
- Reproducción segura del entorno
- Evitar diferencias entre sistemas

### 4. .gitignore
El archivo `.gitignore` se utiliza para evitar la subida de archivos sensibles o
innecesarios al repositorio.

Objetivo:
- Evitar exposición de archivos internos
- Mejorar la seguridad del repositorio
- Prevenir subida accidental de configuraciones locales

### 5. GitHub Security / Dependabot
GitHub proporciona herramientas automáticas para monitorizar dependencias y detectar
posibles vulnerabilidades conocidas.

Objetivo:
- Detectar vulnerabilidades automáticamente
- Revisar librerías inseguras
- Mejorar mantenimiento del proyecto

## 8.2. Resultados de las pruebas de seguridad
A continuación se muestran los resultados obtenidos tras ejecutar las herramientas
automáticas seleccionadas sobre la aplicación.

### 1. Resultado de npm audit
Se ejecutó el siguiente comando
```bash
cd app
docker run --rm -v "$PWD":/app -w /app node:18 npm audit
```
Resultado obtenido:
- Se detectaron 15 vulnerabilidades en dependencias Node.js
- 3 vulnerabilidades bajas
- 3 moderadas
- 9 altas

npm audit permitió identificar paquetes vulnerables y proponer acciones automáticas de 
mitigación mediante `npm audit fix`.

### 2. Resultado de GitHub Actions
Se configuró un workflow automático mediante GitHub Actions utilizando el archivo:
```text
.github/workflows/security.yml
```
Comprobación realizada:
- Subida de cambios al repositorio GitHub
- Ejecución automática del pipeline DevSecOps

Resultado obtenido:
- Ejecución automática del pipeline DevSecOps
- Construcción automática del entorno Docker
- Ejecución de comprobaciones automáticas de seguridad 
- Detección automática de errores dentro del pipeline

Durante las pruebas, GitHub Actions generó alertas relacionadas con la ejecución del 
workflow y configuración del pipeline, demostrando el funcionamiento real de la 
automatización DevSecOps integrada en el proyecto.

GitHub Actions permitió automatizar tareas de validación y seguridad dentro del 
flujo de desarrollo.

### 3. Resultado del análisis de Docker
Comando ejecutado:
```bash
docker compose up --build
```
Resultado obtenido:
- Construcción correcta del contenedor Docker
- Inicio correcto de la aplicación Node.js
- Inicialización correcta de SQLite
- Aplicación accesible desde `http://localhost:3001`
- Funcionamiento correcto de la To-Do App desde navegador

Durante la prueba se comprobó que Docker y Docker Compose permiten 
desplegar la aplicación de forma reproducible y aislada.

### 4. Resultado de .gitignore
Se configuró un archivo `.gitignore` para evitar subir archivos innecesarios 
o sensibles al repositorio.
```text

node_modules/
.idea/
.DS_Store
.env
```

Resultado obtenido:
- Prevención de subida de archivos locales del entorno PyCharm
- Eliminación de archivos innecesarios del repositorio GitHub
- Mejora de organización y limpieza del proyecto
- Protección frente a exposición accidental de información local

La configuración del archivo `.gitignore` permitió controlar correctamente los 
archivos incluidos dentro del repositorio.

### 5. Resultado de GitHub Security / Dependabot
GitHub analizó automáticamente el repositorio y ejecutó comprobaciones relacionadas 
con dependencias y workflows.

Resultado obtenido:
- Monitorización automática del repositorio
- Revisión automática de dependencias
- Integración de seguridad dentro del flujo DevSecOps

Durante las pruebas, GitHub Actions detectó incidencias relacionadas con la configuración 
automática del workflow, demostrando el funcionamiento real de las comprobaciones automáticas 
dentro del entorno DevSecOps.

GitHub Security y Dependabot permitieron añadir supervisión continua sobre dependencias y 
automatizaciones del proyecto.

## 8.3 Alteraciones realizadas para provocar alertas de seguridad
Durante la actividad se realizaron pequeñas modificaciones y configuraciones sobre el 
proyecto con el objetivo de comprobar el funcionamiento de las herramientas automáticas 
seleccionadas.

### Alteraciones realizadas
1. Ejecución de `npm audit`
- Se analizaron dependencias potencialmente vulnerables.
- Objetivo: obtener alertas automáticas de seguridad.
2. Creación del workflow `security.yml`
- Se añadió un pipeline DevSecOps en GitHub Actions.
- Objetivo: automatizar revisiones de seguridad y construcción Docker.
3. Configuración de `.gitignore`
- Se añadieron exclusiones de archivos locales y sensibles.
- Objetivo: evitar exposición accidental de información.
4. Ejecución de Docker Compose
- Se verificó el despliegue automatizado del entorno.
- Objetivo: comprobar ejecución reproducible y controlada.
5. Revisión de dependencias Node.js
- Se revisaron librerías y paquetes instalados.
- Objetivo: detectar posibles vulnerabilidades conocidas.

## 8.4 Conclusiones de la evaluación automática
Las herramientas seleccionadas permitieron automatizar parte del análisis de 
seguridad de la aplicación y facilitar la integración de prácticas DevSecOps 
dentro del proyecto.

El uso combinado de Docker, GitHub Actions, npm audit y GitHub Security permitió 
detectar posibles riesgos, automatizar comprobaciones y mejorar la organización y 
mantenimiento del entorno de desarrollo seguro.

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
## 9. Herramientas DevSecOps utilizadas o propuestas

- GitHub para control de versiones
- Docker para crear un entorno reproducible
- Docker Compose para facilitar la ejecución
- .gitignore para evitar subir archivos innecesarios
- npm audit para revisar vulnerabilidades en dependencias
- Documentación de pruebas funcionales y de seguridad

## 10. Diagrama S-SDLC y DevSecOps

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

## 11. Evidencias
Se han obtenido evidencias de:
- Aplicación ejecutándose en Docker
- Aplicación accesible desde navegador
- Estructura del proyecto en PyCharm
- Configuración mediante Docker Compose
- Repositorio publicado en GitHub
- Documentación S-SDLC
- Propuesta de flujo DevSecOps
- Diagrama S-SDLC + DevSecOps
