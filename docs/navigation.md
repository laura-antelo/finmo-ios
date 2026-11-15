# Navegación y estructura — Finmo

## 1. Introducción

Este documento define la estructura de navegación de Finmo, las pantallas principales y las relaciones entre ellas.

La navegación evolucionará progresivamente conforme se incorporen nuevas funcionalidades.

El objetivo es ofrecer una experiencia intuitiva, manteniendo accesibles las operaciones más frecuentes y evitando introducir complejidad innecesaria.

## 2. Navegación principal

Finmo utilizará una barra de navegación inferior para acceder a las secciones principales de la aplicación.

La estructura completa prevista será:

| Sección | Propósito |
|---|---|
| Inicio | Consultar el balance y el resumen financiero |
| Movimientos | Consultar y gestionar ingresos y gastos |
| Análisis | Explorar estadísticas y evolución financiera |
| Planificación | Gestionar presupuestos y objetivos de ahorro |

La acción de registrar un movimiento tendrá un acceso destacado mediante un botón `+`.

La pantalla de Ajustes será accesible desde un acceso secundario, sin ocupar una pestaña principal.

## 3. Pantallas principales

### 3.1. Inicio

Será la pantalla principal al abrir Finmo.

Mostrará:

- Balance personal calculado.
- Resumen de ingresos y gastos del período.
- Acceso a los movimientos recientes.
- Acceso rápido para registrar un movimiento.

En versiones posteriores podrá incorporar información resumida de presupuestos y objetivos de ahorro.

### 3.2. Movimientos

Permitirá consultar y gestionar el historial de ingresos y gastos.

Incluirá:

- Listado de movimientos ordenados por fecha.
- Identificación visual de ingresos y gastos.
- Información de importe, categoría y descripción.
- Acceso al detalle de cada movimiento.
- Opciones de edición y eliminación.

Posteriormente incorporará búsquedas y filtros avanzados.

### 3.3. Análisis

Permitirá comprender cómo evolucionan las finanzas personales.

Incluirá:

- Resumen financiero del período seleccionado.
- Distribución de gastos por categoría.
- Gráficos de evolución de ingresos, gastos y ahorro.
- Comparación entre períodos.

Esta sección se incorporará en la versión v0.2.

### 3.4. Planificación

Agrupará las funcionalidades destinadas al control y la planificación financiera.

Inicialmente permitirá:

- Crear presupuestos mensuales por categoría.
- Consultar el progreso de los presupuestos.
- Identificar importes disponibles y límites superados.

Posteriormente incorporará:

- Objetivos de ahorro.
- Seguimiento de aportaciones.
- Previsiones financieras.

Esta sección se incorporará en la versión v0.3.

## 4. Pantallas secundarias

### 4.1. Registrar movimiento

Permitirá introducir un ingreso o gasto.

Contendrá:

- Selector de tipo de movimiento.
- Importe.
- Categoría.
- Fecha.
- Descripción opcional.
- Acción para guardar.

Se accederá mediante el botón `+` disponible en la navegación principal.

### 4.2. Detalle de movimiento

Mostrará la información completa de un movimiento registrado.

Permitirá acceder a las acciones de edición y eliminación.

### 4.3. Editar movimiento

Permitirá modificar los datos de un movimiento existente utilizando un formulario coherente con el registro de movimientos.

### 4.4. Ajustes

Agrupará las preferencias generales de la aplicación.

Inicialmente incluirá la configuración del saldo de referencia.

En versiones posteriores podrá incorporar:

- Gestión de categorías personalizadas.
- Preferencias de apariencia.
- Protección mediante Face ID.
- Configuración de moneda.
- Cuenta y sincronización opcional.

### 4.5. Gestión de categorías

Permitirá consultar, crear y modificar categorías personalizadas.

Se incorporará en la versión v0.4.

### 4.6. Detalle y edición de presupuestos

Permitirá consultar y modificar los límites de gasto asociados a una categoría.

Se incorporará en la versión v0.3.

### 4.7. Detalle y edición de objetivos

Permitirá consultar el progreso de un objetivo de ahorro, registrar aportaciones y modificar su configuración.

Se incorporará en la versión v0.5.

## 5. Evolución de la navegación

### v1.1.0 — Mis movimientos

La navegación principal incluirá únicamente:

- Inicio.
- Movimientos.
- Botón `+` para registrar movimientos.

También estarán disponibles las pantallas secundarias necesarias para gestionar movimientos y configurar el saldo inicial.

### v1.2.0 — Entender mis finanzas

Se incorporará la sección Análisis.

La navegación principal pasará a incluir:

- Inicio.
- Movimientos.
- Análisis.
- Botón `+`.

### v1.3.0 — Controlar mis gastos

Se incorporará la sección Planificación, inicialmente centrada en presupuestos.

La navegación principal incluirá:

- Inicio.
- Movimientos.
- Análisis.
- Planificación.
- Botón `+`.

### v1.4.0 — Organización personalizada

Se ampliarán las capacidades de organización y búsqueda sin añadir nuevas pestañas principales.

### v1.5.0 — Planificación avanzada

La sección Planificación incorporará objetivos de ahorro y funcionalidades de previsión.

### v1.6.0+ — Experiencia avanzada

Se ampliará la configuración con nuevas opciones de personalización, seguridad y sincronización.

## 6. Principios de navegación

- **Accesibilidad:** las funciones principales estarán disponibles con pocos pasos.
- **Consistencia:** los patrones de navegación serán coherentes entre pantallas.
- **Jerarquía:** las funciones secundarias no competirán visualmente con las principales.
- **Progresividad:** las nuevas funcionalidades se incorporarán sin reorganizaciones innecesarias.
- **Claridad:** no se mostrarán secciones vacías correspondientes a funcionalidades futuras.
- **Rapidez:** registrar un ingreso o gasto será una acción destacada y accesible.

## 7. Relación con el diseño

La estructura descrita servirá como referencia para elaborar los wireframes y las pantallas definitivas en Figma.

Las decisiones sobre componentes, distribución visual y transiciones se concretarán durante la fase de diseño.

La implementación seguirá las versiones definidas en [`roadmap.md`](roadmap.md).
