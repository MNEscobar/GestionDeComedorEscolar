# Requisitos – Sistema de Gestión de Stock para Comedor Escolar

## 1. Introducción
El presente documento describe los requisitos funcionales y no funcionales del **Sistema de Gestión de Stock para Comedor Escolar**.  
El sistema será utilizado por un único usuario (ecónomo/a del comedor) para gestionar el inventario de alimentos y suministros, registrando entradas y salidas y manteniendo actualizado el stock automáticamente.

---

## 2. Objetivo del sistema
Facilitar y automatizar el control de stock del comedor escolar, evitando el trabajo manual de actualización en planillas y reduciendo errores en los cálculos.

---

## 3. Alcance
El sistema permitirá:
- Registrar productos con su información básica.
- Registrar entradas y salidas de stock.
- Actualizar el stock automáticamente.
- Consultar el stock actual.
- Visualizar un historial de movimientos.

El sistema **no** está pensado para múltiples usuarios ni para conexión a internet; funcionará de forma local en una sola computadora.

---

## 4. Requisitos funcionales

### RF-01 – Gestión de productos
- RF-01.1: Agregar un nuevo producto con:
  - Nombre.
  - Unidad de medida (kg, litros, unidades, etc.).
  - Cantidad inicial.
- RF-01.2: Editar datos de un producto.
- RF-01.3: Eliminar un producto del sistema.

### RF-02 – Registro de entradas
- RF-02.1: Seleccionar un producto existente.
- RF-02.2: Indicar la cantidad que ingresa.
- RF-02.3: Registrar automáticamente la fecha (editable si es necesario).
- RF-02.4: Permitir agregar observaciones.
- RF-02.5: Sumar la cantidad ingresada al stock actual.

### RF-03 – Registro de salidas
- RF-03.1: Seleccionar un producto existente.
- RF-03.2: Indicar la cantidad que se retira.
- RF-03.3: Validar que el stock disponible sea suficiente.
- RF-03.4: Registrar automáticamente la fecha (editable si es necesario).
- RF-03.5: Permitir agregar observaciones.
- RF-03.6: Descontar la cantidad retirada del stock actual.

### RF-04 – Consulta de stock
- RF-04.1: Mostrar la lista de productos con sus cantidades actualizadas.
- RF-04.2: Permitir ordenar y buscar por nombre de producto.

### RF-05 – Historial de movimientos
- RF-05.1: Listar todos los movimientos (entradas y salidas) con:
  - Fecha.
  - Tipo de movimiento (entrada/salida).
  - Producto.
  - Cantidad.
  - Observaciones.
- RF-05.2: Permitir filtrar por fecha y/o producto (funcionalidad opcional en el MVP).

---

## 5. Requisitos no funcionales
- RNF-01: El sistema debe ser una aplicación de escritorio desarrollada en **Java** con **SQLite** como base de datos local.
- RNF-02: Debe funcionar sin conexión a internet.
- RNF-03: La interfaz debe ser simple, clara y de fácil uso para usuarios no técnicos.
- RNF-04: El sistema debe guardar los datos de forma persistente en un archivo de base de datos SQLite.
- RNF-05: No debe requerir instalación compleja; bastará con ejecutar el programa.

---

## 6. Datos iniciales
El stock inicial podrá ser cargado manualmente por el usuario o importado desde un archivo Excel (opcional en esta primera versión).

---

## 7. Criterios de aceptación del MVP
- El usuario puede registrar, editar y eliminar productos.
- El usuario puede registrar entradas y salidas.
- El stock se actualiza automáticamente en cada movimiento.
- Se puede consultar el stock actualizado en todo momento.
- Existe un historial básico de movimientos.

---

## 8. Futuras mejoras (fuera del alcance inicial)
- Exportar historial a Excel o
