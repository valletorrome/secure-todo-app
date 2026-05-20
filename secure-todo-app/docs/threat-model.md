# Modelo de amenazas

## Amenazas identificadas

| Amenaza | Riesgo | Mitigación |
|---|---|---|
| XSS | Alto | Validación y sanitización de entradas |
| Dependencias vulnerables | Medio | Uso de npm audit |
| Configuración insegura | Medio | Docker aislado |
| Exposición de secretos | Alto | Uso de variables de entorno |
| Acceso no autorizado | Bajo | Aplicación local y contenerizada |

## Riesgos principales

La principal amenaza detectada es la posibilidad de introducir código malicioso desde formularios web.

## Medidas aplicadas

- Uso de Docker.
- Validación básica de entradas.
- Organización segura del proyecto.
- Separación de documentación y código.