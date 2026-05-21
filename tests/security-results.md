# Resultados de herramientas automáticas de seguridad

## 1. npm audit
Comando ejecutado:

```bash
npm audit
```
Resultado observado:
- Se detectaron 15 vulnerabilidades en dependencias Node.js.
- 3 vulnerabilidades bajas.
- 3 vulnerabilidades moderadas.
- 9 vulnerabilidades altas.
- npm audit generó recomendaciones automáticas de mitigación 
mediante `npm audit fix`.

## 2. GitHub Actions
Herramienta utilizada:
- GitHub Actions
- Workflow: `security.yml`

Resultado observado:
- El workflow `security.yml` se ejecutó automáticamente tras realizar `git push`.
- GitHub Actions realizó comprobaciones automáticas del pipeline DevSecOps.
- Durante las pruebas se detectaron errores relacionados con la configuración 
automática del workflow.
- GitHub Actions permitió comprobar el funcionamiento real de la automatización 
CI/CD y DevSecOps.

## 3. Docker Compose
Comando ejecutado:
```bash
docker compose up --build
```
Resultado observado:
- Construcción correcta del contenedor Docker.
- Inicio correcto de la aplicación Node.js.
- Inicialización correcta de SQLite.
- Acceso funcional desde `http://localhost:3001`.
- Funcionamiento correcto de la To-Do App desde navegador.

## 4. .gitignore

Configuración aplicada:

```text
node_modules/
.idea/
.DS_Store
.env
```
Resultado observado:
- Prevención de subida de archivos locales del entorno PyCharm.
- Eliminación de archivos innecesarios del repositorio GitHub.
- Mejora de organización y limpieza del proyecto.
- Protección frente a exposición accidental de información local.

## 5. GitHub Security y Dependabot
Resultado observado:
- GitHub monitorizó automáticamente el repositorio y los workflows.
- Se integraron comprobaciones automáticas relacionadas con seguridad y DevSecOps.
- GitHub permitió supervisar automáticamente dependencias y automatizaciones del proyecto.
