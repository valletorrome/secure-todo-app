# Resultados de herramientas automáticas de seguridad

## 1. npm audit
Comando ejecutado:

```bash
npm audit
```
Resultado observado:
- La herramienta analizó automáticamente las dependencias instaladas.
- Se detectaron recomendaciones relacionadas con vulnerabilidades conocidas.
- npm audit mostró advertencias de seguridad sobre paquetes de Node.js.

Conclusión:
La herramienta permite identificar rápidamente dependencias inseguras y facilita su actualización.

## 2. GitHub Actions
Herramienta utilizada:
- GitHub Actions
- Workflow: `security.yml`

Resultado observado:
- El pipeline DevSecOps se ejecutó automáticamente al subir cambios al repositorio.
- GitHub Actions realizó comprobaciones automáticas del proyecto.

Conclusión:
GitHub Actions permite automatizar tareas de seguridad y validación dentro del flujo de desarrollo.

## 3. Docker Compose
Comando ejecutado:
```bash
docker compose up --build
```
Resultado observado:
- Construcción correcta del contenedor.
- Ejecución funcional de la aplicación web.
- Acceso correcto desde localhost.

Conclusión:
Docker facilita la ejecución segura y reproducible del entorno.

## 4. .gitignore

Configuración aplicada:

```text
node_modules/
.idea/
.DS_Store
.env
```
Resultado observado:
- Reducción de archivos innecesarios en el repositorio.
- Prevención de subida accidental de archivos locales.

Conclusión:
El uso de `.gitignore` mejora la organización y seguridad del proyecto.

## 5. GitHub Security y Dependabot
Resultado observado:
- GitHub monitoriza automáticamente dependencias y workflows.
- Se habilitó integración básica de seguridad dentro del repositorio.

Conclusión:
Las herramientas automáticas de GitHub ayudan a mejorar el mantenimiento 
seguro del proyecto.

# Conclusión general
Las herramientas utilizadas permitieron automatizar parte del análisis de 
seguridad de la aplicación y facilitar la integración de prácticas DevSecOps 
dentro del proyecto.

El uso combinado de Docker, GitHub Actions, npm audit y GitHub Security permitió 
detectar riesgos potenciales y mejorar la seguridad del entorno de desarrollo.