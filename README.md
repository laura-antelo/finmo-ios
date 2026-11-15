# Swift iOS Repository Template

Plantilla reutilizable para desarrollar aplicaciones **Swift/iOS** con GitHub, siguiendo convenciones de desarrollo, control de versiones e integración continua.

## Características

- **GitFlow:** organización del desarrollo mediante ramas `main`, `develop` y ramas temporales.
- **GitHub Issues:** plantillas para reportar bugs, solicitar funcionalidades y registrar tareas técnicas.
- **Pull Requests:** plantilla para documentar cambios, causas de errores y validaciones.
- **SwiftLint:** análisis estático con las reglas predeterminadas.
- **GitHub Actions:** CI preparada para SwiftLint, compilación y tests de Xcode.
- **Documentación:** convenciones y guía de configuración inicial.

## Uso

1. Seleccionar **Use this template → Create a new repository**.
2. Clonar el repositorio y añadir el proyecto Xcode.
3. Crear la rama `develop`.
4. Configurar las variables de GitHub Actions y los Rulesets.
5. Personalizar el README y comenzar el desarrollo.

Consulta [SETUP.md](docs/SETUP.md) para la configuración completa.

## Estructura

```text
.github/
├── ISSUE_TEMPLATE/
│   ├── bug_report.yml
│   ├── feature_request.yml
│   └── task.yml
├── workflows/
│   └── ios-ci.yml
└── pull_request_template.md

docs/
└── SETUP.md

.gitignore
.swiftlint.yml
CONTRIBUTING.md
README.md
```

## Convenciones

Las convenciones de ramas, commits, Issues y Pull Requests están documentadas en [CONTRIBUTING.md](CONTRIBUTING.md).

## Personalización

Esta plantilla proporciona la estructura inicial del repositorio. Cada aplicación deberá adaptar la configuración de Xcode, los workflows de CI y su documentación.

Las configuraciones de GitHub que no se copian automáticamente se detallan en [SETUP.md](docs/SETUP.md).
