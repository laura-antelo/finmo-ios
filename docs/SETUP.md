# Project Setup

Guía de configuración inicial para nuevos proyectos Swift/iOS creados desde `github-repository-template`.

## 1. Crear el repositorio

1. Abrir `github-repository-template`.
2. Seleccionar **Use this template → Create a new repository**.
3. Elegir nombre, descripción y visibilidad.
4. Clonar el repositorio.
5. Crear o incorporar el proyecto Xcode.

Comprobar que los archivos `.xcodeproj` o `.xcworkspace` necesarios están versionados.

## 2. Configurar GitFlow

Crear la rama `develop` a partir de `main`.

Mantener:

- `main`: código estable.
- `develop`: integración de cambios.
- `feature/*`, `fix/*`, `docs/*`, `refactor/*`, `chore/*`: ramas temporales.

Consultar [CONTRIBUTING.md](../CONTRIBUTING.md) para las convenciones completas.

## 3. Configurar GitHub Actions

Acceder a:

**Settings → Secrets and variables → Actions → Variables**

Crear las variables:

| Variable | Valor |
|---|---|
| `IOS_PROJECT` | Ruta relativa del archivo `.xcodeproj` |
| `IOS_WORKSPACE` | Ruta relativa del `.xcworkspace`, si corresponde |
| `IOS_SCHEME` | Scheme compartido de Xcode |
| `IOS_DESTINATION` | Destino de simulador para ejecutar tests |

Configurar `IOS_PROJECT` o `IOS_WORKSPACE`, según la estructura de la aplicación.

Ejemplo:

```text
IOS_PROJECT = FinanceApp.xcodeproj
IOS_SCHEME = FinanceApp
IOS_DESTINATION = platform=iOS Simulator,name=iPhone 16,OS=latest
```

Los valores deben adaptarse al proyecto y a los simuladores disponibles en el runner.

### Validación

Desde **Actions → iOS CI**, ejecutar manualmente el workflow.

Comprobar que:

- SwiftLint analiza el código.
- Build compila correctamente.
- Tests ejecuta las pruebas existentes.

**Importante:** un job omitido (`Skipped`) no significa que se haya ejecutado correctamente. Si Build o Tests aparecen omitidos, revisar las variables y la configuración del proyecto.

El workflow puede requerir ajustes para dependencias, versión de Xcode, firma o simuladores específicos.

## 4. Configurar Rulesets

Los Rulesets del repositorio plantilla no se transfieren automáticamente.

Acceder a:

**Settings → Rules → Rulesets**

Crear:

### Protect main

- Target: `main`.
- Enforcement: `Active`.
- Restrict deletions.
- Block force pushes.
- Require a pull request before merging.
- Required approvals: `0`.
- Require conversation resolution before merging.
- Merge methods permitidos: Merge y Squash.

### Protect develop

Aplicar las mismas protecciones a `develop`.

Una vez que la CI esté correctamente configurada y validada, establecer los status checks obligatorios.

Verificar que las reglas se aplican efectivamente según la visibilidad del repositorio y el plan de GitHub.

## 5. Configurar Labels

Las etiquetas personalizadas del repositorio plantilla no se copian automáticamente.

Mantener las etiquetas predeterminadas de GitHub y añadir cuando corresponda:

| Label | Descripción |
|---|---|
| `refactor` | Mejoras internas del código |
| `chore` | Mantenimiento y configuración |

Añadir etiquetas específicas de áreas o prioridades únicamente cuando sean necesarias.

## 6. Configurar GitHub Projects

Crear una copia del Project maestro y vincularla al repositorio.

Campos recomendados:

| Campo | Valores o tipo |
|---|---|
| Status | Todo, In Progress, In Review, Blocked, Done |
| Priority | Urgent, High, Medium, Low |
| Story Points | Number |
| Start Date | Date |
| End Date | Date |

Las fechas de inicio y finalización representan **fechas reales**, no fechas previstas.

Revisar las automatizaciones y las vinculaciones del Project después de copiarlo.

## 7. Personalizar el README

Sustituir el README de la plantilla por uno específico de la aplicación.

Incluir cuando corresponda:

- Descripción del proyecto.
- Funcionalidades principales.
- Tecnologías utilizadas.
- Requisitos e instalación.
- Capturas de pantalla.
- Enlace al diseño de Figma.
- Arquitectura y estructura del proyecto.
- Licencia.

## 8. Checklist final

- [ ] Proyecto Xcode incorporado.
- [ ] Rama `develop` creada.
- [ ] Variables de Actions configuradas.
- [ ] SwiftLint validado.
- [ ] Build ejecutada correctamente.
- [ ] Tests ejecutados o ausencia de tests documentada.
- [ ] Rulesets creados y verificados.
- [ ] Etiquetas personalizadas revisadas.
- [ ] GitHub Project vinculado, si corresponde.
- [ ] README personalizado.
- [ ] Archivos temporales y credenciales excluidos.
