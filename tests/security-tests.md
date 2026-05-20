# Pruebas de seguridad realizadas

## 1. Validación de entradas
Objetivo:
Comprobar cómo responde la aplicación ante entradas no habituales o potencialmente maliciosas.

Pruebas realizadas:
- Introducción de texto normal.
- Introducción de caracteres especiales.
- Introducción de cadenas largas.
- Introducción de scripts simples.

Ejemplo utilizado:
```html
<script>alert('XSS')</script>
```
Resultado:
La aplicación mantuvo funcionamiento estable y no comprometió el entorno Docker.

## 2. Revisión de dependencias
Herramienta utilizada:
- npm audit

Comando ejecutado:
```bash
npm audit
```
Resultado:
- Análisis automático de dependencias.
- Detección de recomendaciones de seguridad.
- Revisión de paquetes vulnerables.

## 3. Ejecución del pipeline DevSecOps
Herramienta utilizada:
- GitHub Actions

Archivo:
```text
.github/workflows/security.yml
```
Resultado:
- Ejecución automática del workflow.
- Automatización básica de tareas de seguridad.
- Integración CI/CD dentro del proyecto.

## 4. Pruebas Docker
Comando ejecutado:
```bash
docker compose up --build
```
Resultado:
- Construcción correcta del contenedor.
- Ejecución estable de la aplicación.
- Acceso correcto mediante localhost.

## 5. Verificación de archivos sensibles
Herramienta utilizada:
- .gitignore

Archivos protegidos:
- node_modules/
- .idea/
- .DS_Store
- .env

Resultado:
- Prevención de subida de archivos innecesarios.
- Mejora de organización y seguridad del repositorio.

# Conclusión

Las pruebas realizadas permitieron comprobar el funcionamiento básico de diferentes 
herramientas automáticas de seguridad aplicadas sobre la aplicación web.

La combinación de Docker, GitHub Actions, npm audit y GitHub Security permitió automatizar 
parte del análisis de seguridad y reforzar el enfoque DevSecOps del proyecto.