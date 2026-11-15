# Requisitos funcionales — Finmo

## 1. Introducción

Este documento recoge los requisitos funcionales de Finmo, una aplicación iOS para la gestión de finanzas personales.

Los requisitos se organizan por áreas funcionales y se identifican mediante códigos únicos para facilitar su seguimiento durante el desarrollo.

Su implementación será progresiva, siguiendo las versiones definidas en el roadmap.

## 2. Gestión de movimientos

### RF-01 — Registrar movimientos

El usuario podrá registrar ingresos y gastos manualmente.

Cada movimiento incluirá:

- Tipo: ingreso o gasto.
- Importe.
- Categoría.
- Fecha.
- Descripción opcional.

El sistema actualizará automáticamente el balance calculado al registrar un movimiento.

### RF-02 — Consultar movimientos

El usuario podrá consultar el historial de movimientos registrados.

Cada elemento mostrará su información principal, incluyendo importe, categoría y fecha.

### RF-03 — Editar movimientos

El usuario podrá modificar los datos de un movimiento existente.

Los cambios se reflejarán automáticamente en los cálculos financieros.

### RF-04 — Eliminar movimientos

El usuario podrá eliminar movimientos registrados, previa confirmación.

El balance y los resúmenes se actualizarán para reflejar la eliminación.

### RF-05 — Registrar movimientos recurrentes

El usuario podrá configurar ingresos y gastos periódicos, indicando su frecuencia y fecha de inicio.

La aplicación permitirá gestionar estas recurrencias y generar los movimientos correspondientes según la programación definida.

## 3. Balance y resumen financiero

### RF-06 — Configurar saldo inicial

El usuario podrá introducir y modificar un saldo inicial de referencia.

Este importe servirá como punto de partida para calcular su balance personal.

### RF-07 — Consultar balance

La pantalla de inicio mostrará el balance calculado a partir del saldo inicial y los movimientos registrados.

**Balance = Saldo inicial + Ingresos − Gastos**

El balance representa exclusivamente la información registrada en Finmo y no necesariamente el saldo real de una cuenta bancaria.

### RF-08 — Consultar resumen del período

El usuario podrá visualizar un resumen de ingresos, gastos y ahorro neto correspondiente al período seleccionado.

## 4. Categorías y organización

### RF-09 — Utilizar categorías predefinidas

La aplicación proporcionará categorías iniciales para clasificar ingresos y gastos.

### RF-10 — Personalizar categorías

El usuario podrá crear, editar y gestionar categorías personalizadas.

### RF-11 — Organizar mediante etiquetas

El usuario podrá asignar etiquetas a sus movimientos para facilitar su organización.

### RF-12 — Buscar y filtrar movimientos

El usuario podrá localizar movimientos mediante búsquedas y filtros por criterios como tipo, categoría, fecha, importe y etiquetas.

## 5. Análisis financiero

### RF-13 — Analizar gastos por categoría

La aplicación mostrará la distribución de los gastos mediante gráficos y resúmenes por categoría.

### RF-14 — Consultar evolución financiera

El usuario podrá visualizar la evolución de ingresos, gastos y ahorro neto a lo largo del tiempo.

### RF-15 — Comparar períodos

El usuario podrá comparar los resultados financieros de distintos meses.

### RF-16 — Seleccionar período de análisis

El usuario podrá cambiar el período temporal utilizado para consultar los datos y gráficos financieros.

## 6. Presupuestos

### RF-17 — Crear presupuestos mensuales

El usuario podrá establecer límites de gasto mensuales para categorías específicas.

### RF-18 — Consultar progreso de presupuestos

La aplicación mostrará el importe gastado, el límite establecido y el presupuesto restante.

### RF-19 — Recibir alertas de presupuesto

La aplicación podrá avisar al usuario cuando el gasto de una categoría alcance determinados umbrales o supere su presupuesto.

## 7. Planificación financiera

### RF-20 — Crear objetivos de ahorro

El usuario podrá definir objetivos indicando una cantidad económica y, opcionalmente, una fecha objetivo.

### RF-21 — Consultar progreso de objetivos

La aplicación permitirá registrar aportaciones y consultar el progreso de cada objetivo de ahorro.

### RF-22 — Consultar previsiones de balance

La aplicación podrá estimar la evolución futura del balance utilizando la información financiera registrada y los movimientos recurrentes previstos.

Las previsiones serán orientativas y no representarán saldos bancarios garantizados.

## 8. Configuración y experiencia

### RF-23 — Utilizar la aplicación sin cuenta

El usuario podrá utilizar las funcionalidades locales sin necesidad de registrarse o iniciar sesión.

### RF-24 — Persistir información localmente

La aplicación conservará los movimientos, categorías, presupuestos y demás información del usuario en almacenamiento local persistente.

### RF-25 — Proteger el acceso mediante Face ID

El usuario podrá activar protección biométrica para acceder a la aplicación, cuando el dispositivo lo permita.

### RF-26 — Seleccionar apariencia

La aplicación permitirá utilizar una apariencia clara u oscura.

### RF-27 — Configurar moneda

El usuario podrá seleccionar la moneda utilizada para representar los importes financieros.

### RF-28 — Sincronizar información opcionalmente

En una versión futura, el usuario podrá crear una cuenta y sincronizar sus datos entre dispositivos compatibles.

La sincronización no será obligatoria para utilizar Finmo.

## 9. Restricciones funcionales

- Finmo no realizará operaciones bancarias ni transferencias de dinero real.
- Los movimientos se introducirán manualmente.
- No se requerirá conexión con entidades financieras.
- La aplicación no incluirá datos financieros ficticios precargados.
- La gestión de múltiples cuentas financieras no forma parte del alcance prioritario.
- Las funcionalidades avanzadas se incorporarán progresivamente y no serán necesarias para utilizar las funciones básicas.

## 10. Trazabilidad

Cada requisito funcional podrá vincularse con una o varias Issues de GitHub.

Las Issues definirán las tareas concretas de implementación y sus criterios de aceptación.

La distribución de funcionalidades por versiones se documentará en [`roadmap.md`](roadmap.md).
