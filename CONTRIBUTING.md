# Contributing Guidelines

Este documento define las convenciones de desarrollo de los proyectos creados a partir de esta plantilla.

## Branching Strategy

Utilizamos una adaptación de **GitFlow**.

| Rama | Propósito |
|---|---|
| `main` | Código estable |
| `develop` | Integración de cambios |
| `feature/*` | Nuevas funcionalidades |
| `fix/*` | Correcciones de errores |
| `refactor/*` | Refactorizaciones |
| `docs/*` | Documentación |
| `chore/*` | Mantenimiento y configuración |

Las ramas temporales se crean desde `develop` y se integran mediante Pull Requests.

Los cambios preparados para una versión estable se integran desde `develop` hacia `main`.

### Nomenclatura

Formato recomendado:

`<type>/<issue-number>-<description>`

Ejemplos:

```text
feature/12-add-expense
fix/24-login-error
refactor/31-network-layer
docs/update-readme
```

Se recomienda utilizar minúsculas, guiones y nombres descriptivos.

## Commit Convention

Seguimos la especificación **Conventional Commits**:

`<type>: <description>`

| Tipo | Uso |
|---|---|
| `feat` | Nueva funcionalidad |
| `fix` | Corrección de errores |
| `docs` | Documentación |
| `refactor` | Cambios internos sin alterar el comportamiento |
| `test` | Incorporación o modificación de pruebas |
| `chore` | Mantenimiento y configuración |

Ejemplos:

```text
feat: añadir registro de gastos
fix: corregir validación de importes
refactor: simplificar gestión de sesiones
```

Los commits deben ser descriptivos y contener cambios relacionados.

## Issues

Utilizar la plantilla correspondiente:

- **Bug Report:** problemas de funcionamiento.
- **Feature Request:** nuevas funcionalidades o mejoras.
- **Task:** mantenimiento, configuración y documentación.

Cuando corresponda, incluir criterios de aceptación y referencias a diseños o documentación.

## Pull Requests

Todas las modificaciones de ramas protegidas se integran mediante Pull Requests.

Cada PR debe:

- Describir los cambios realizados.
- Referenciar la Issue relacionada.
- Documentar la causa raíz cuando se corrige un bug.
- Indicar las comprobaciones realizadas.
- Superar los checks de CI configurados.

### Vinculación con Issues

Utilizamos las siguientes convenciones:

| Referencia | Uso recomendado |
|---|---|
| `Closes #XX` | Finalización de una funcionalidad |
| `Fixes #XX` | Corrección completa de un bug |
| `Resolves #XX` | Finalización de una tarea |
| `Refs #XX` | Referencia sin cierre automático |

Las tres primeras palabras clave pueden cerrar automáticamente una Issue cuando los cambios se integran en la rama predeterminada del repositorio.

### Merge Strategy

- **Squash and merge:** integración habitual de ramas temporales en `develop`.
- **Create a merge commit:** integración de `develop` en `main`.
- **Rebase and merge:** no se utiliza por defecto.

No se permiten pushes directos ni force pushes a las ramas protegidas, cuando los Rulesets estén activos y sean aplicables.

## Code Quality

- Respetar las reglas definidas en `.swiftlint.yml`.
- Mantener funciones y componentes legibles.
- Evitar cambios no relacionados en una misma PR.
- Incorporar pruebas cuando sean relevantes.
- No incluir credenciales ni archivos generados.
- Revisar los resultados de GitHub Actions antes de integrar cambios.
