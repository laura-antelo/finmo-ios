# Roadmap — Finmo

## 1. Introducción

Este documento define la evolución funcional prevista de Finmo, una aplicación iOS para la gestión de finanzas personales.

El desarrollo se organizará mediante versiones incrementales. Cada versión deberá ofrecer funcionalidades completas, utilizables y verificadas antes de su publicación.

Las versiones no estarán asociadas a fechas de entrega fijas. Su publicación dependerá del cumplimiento de los objetivos y criterios de aceptación definidos.

## 2. Estrategia de versionado

Finmo seguirá una estrategia de versionado semántico:

**MAJOR.MINOR.PATCH**

- **MAJOR:** cambios incompatibles o evolución significativa del producto.
- **MINOR:** incorporación de nuevas funcionalidades compatibles.
- **PATCH:** correcciones de errores y ajustes menores.

La primera versión funcional y estable será **v1.0.0**.

Las versiones posteriores ampliarán progresivamente sus capacidades.

Cada versión publicada se identificará mediante una etiqueta Git y, cuando corresponda, una GitHub Release.

## 3. Versiones previstas

### v1.0.0 — Mis movimientos

**Objetivo:** ofrecer una aplicación funcional para registrar y consultar las finanzas personales.

**Funcionalidades:**

- Registro manual de ingresos y gastos.
- Consulta del historial de movimientos.
- Edición y eliminación de movimientos.
- Categorías predefinidas.
- Configuración del saldo inicial.
- Cálculo automático del balance.
- Resumen básico de ingresos y gastos.
- Persistencia local de la información.
- Navegación entre Inicio y Movimientos.

**Criterios de finalización:**

- El usuario puede completar el ciclo de vida de un movimiento.
- Los cambios se reflejan correctamente en el balance.
- Los datos permanecen disponibles después de cerrar y volver a abrir la aplicación.
- La aplicación puede utilizarse sin crear una cuenta.
- Las pantallas principales funcionan sin errores conocidos que impidan su uso.

### v1.1.0 — Entender mis finanzas

**Objetivo:** permitir al usuario analizar y comprender su información financiera.

**Funcionalidades:**

- Nueva sección Análisis.
- Distribución de gastos por categoría.
- Evolución de ingresos, gastos y ahorro neto.
- Comparación entre meses.
- Selección de períodos de análisis.

**Criterios de finalización:**

- Los gráficos representan correctamente los movimientos registrados.
- El usuario puede cambiar el período de consulta.
- Las comparaciones muestran resultados coherentes con los datos disponibles.
- Los períodos sin movimientos se representan mediante estados vacíos adecuados.

### v1.2.0 — Controlar mis gastos

**Objetivo:** incorporar herramientas para establecer y supervisar límites de gasto.

**Funcionalidades:**

- Nueva sección Planificación.
- Creación de presupuestos mensuales por categoría.
- Edición y eliminación de presupuestos.
- Seguimiento del gasto acumulado.
- Visualización del importe restante.
- Identificación de presupuestos superados.

**Criterios de finalización:**

- El usuario puede gestionar presupuestos por categoría.
- Los gastos registrados actualizan el progreso correspondiente.
- Los importes y porcentajes se calculan correctamente.
- Los presupuestos se conservan entre sesiones.

### v1.3.0 — Organización personalizada

**Objetivo:** ofrecer mayor flexibilidad para organizar y localizar movimientos.

**Funcionalidades:**

- Creación y edición de categorías personalizadas.
- Gestión de categorías.
- Creación y asignación de etiquetas.
- Búsqueda de movimientos.
- Filtros avanzados por tipo, categoría, fecha, importe y etiquetas.

**Criterios de finalización:**

- El usuario puede organizar movimientos mediante categorías y etiquetas.
- Las modificaciones de categorías mantienen la integridad de los movimientos asociados.
- La búsqueda y los filtros permiten localizar correctamente los movimientos.
- La personalización se conserva entre sesiones.

### v1.4.0 — Planificación avanzada

**Objetivo:** ampliar las herramientas de planificación y seguimiento financiero.

**Funcionalidades:**

- Creación y gestión de objetivos de ahorro.
- Registro de aportaciones a objetivos.
- Seguimiento del progreso de ahorro.
- Configuración de movimientos recurrentes.
- Previsiones orientativas de balance.
- Alertas por umbrales y superación de presupuestos.

**Criterios de finalización:**

- Los objetivos reflejan correctamente las aportaciones registradas.
- Los movimientos recurrentes siguen la frecuencia configurada sin generar duplicados.
- Las previsiones utilizan los datos registrados y distinguen los movimientos previstos de los confirmados.
- Las alertas se generan según las condiciones establecidas.

### v1.5.0+ — Experiencia avanzada

**Objetivo:** mejorar la personalización, seguridad y continuidad de uso de Finmo.

**Funcionalidades previstas:**

- Protección mediante Face ID.
- Compatibilidad con modo oscuro.
- Configuración de moneda.
- Cuenta de usuario opcional.
- Sincronización de datos entre dispositivos compatibles.

Estas funcionalidades podrán distribuirse entre varias versiones menores según su complejidad y prioridad.

La gestión de múltiples cuentas financieras podrá valorarse posteriormente, sin formar parte del alcance prioritario.

## 4. Desarrollo y publicación

El proyecto seguirá un flujo de trabajo basado en GitFlow.

- `main`: código estable.
- `develop`: integración del desarrollo.
- `feature/*`: nuevas funcionalidades.
- `fix/*`: correcciones de errores.
- `docs/*`: documentación.
- `refactor/*`: mejoras internas.
- `chore/*`: mantenimiento y configuración.

Las funcionalidades se desarrollarán mediante ramas temporales y se integrarán en `develop` a través de Pull Requests.

Una vez completados y verificados los objetivos de una versión, los cambios se integrarán en `main` y se creará la etiqueta de versión correspondiente.

## 5. Seguimiento en GitHub

Cada versión prevista tendrá su propio Milestone.

Las funcionalidades se descompondrán en Issues que podrán incluir:

- Descripción del comportamiento esperado.
- Requisitos funcionales relacionados.
- Criterios de aceptación.
- Prioridad.
- Versión objetivo.

El seguimiento se realizará mediante GitHub Projects, utilizando los estados:

- Todo.
- In Progress.
- In Review.
- Blocked.
- Done.

## 6. Evolución del roadmap

El roadmap representa una planificación inicial y podrá modificarse conforme avance el desarrollo.

Se podrán ajustar prioridades, dividir funcionalidades o introducir versiones intermedias cuando sea necesario.

Los cambios deberán mantener el objetivo principal de Finmo: ofrecer una experiencia sencilla, clara y progresivamente más completa para gestionar las finanzas personales.

## 7. Documentación relacionada

- [Visión del producto](product-vision.md)
- [Requisitos funcionales](functional-requirements.md)
- [Navegación y estructura](navigation.md)
