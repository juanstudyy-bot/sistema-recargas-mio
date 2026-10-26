# Backlog actualizado — CR-01

| ID | Tarea | Origen | Prioridad | Responsable | Criterio de terminación |
|---|---|---|---|---|---|
| PB15 (actualizada) | Manejar pagos rechazados, fallidos o pendientes y evitar que una operación sin confirmar aparezca como exitosa. | RNF06, RF05 y CR-01 | Alta | Equipo del proyecto; asignar una persona responsable | Los escenarios aprobado, rechazado y pendiente conservan el estado correcto. No se muestra éxito sin confirmación. |

## Trazabilidad
- Solicitud de cambio: CR-01.
- Caso de uso: CU01 — Realizar una recarga virtual.
- Requisitos relacionados: RF05, RF06 y RNF06.
- Componentes: Servicio de recargas, Gestión de pagos, Datos y transacciones, Notificaciones e Interfaz.
Actualización del backlog — CR-01

ID: PB15
Cambio relacionado: CR-01 — Control de pagos rechazados o pendientes.
Prioridad: Alta.
Responsable: Equipo del proyecto.
Requisitos relacionados: RF05, RF06 y RNF06.
Componentes afectados: Servicio de recargas, Gestión de pagos, Datos y transacciones y Notificaciones.

Condición para terminar: comprobar que los pagos aprobados, rechazados y pendientes se registren con el estado correcto y que ninguna operación aparezca como exitosa sin confirmación del proveedor.

Trazabilidad: solicitud CR-01 → requisitos RF05, RF06 y RNF06 → arquitectura del sistema → tarea PB15.
## CR-02: Consulta del historial de recargas

- **Historia de usuario:** Como usuario de la tarjeta MÍO, quiero consultar mis recargas anteriores para revisar sus fechas, valores y estados.
- **Requisito relacionado:** RF06.
- **Tareas:**
  1. Documentar la consulta del historial.
  2. Definir la información que se mostrará en cada registro.
  3. Verificar que solo se consulten recargas del usuario autenticado.
  4. Revisar la coherencia entre requisitos, arquitectura y backlog.
- **Criterios de aceptación:** se muestran fecha, valor y estado de cada recarga, y los datos corresponden únicamente al usuario que inició sesión.
- **Prioridad:** Media.
- **Estado:** En revisión.