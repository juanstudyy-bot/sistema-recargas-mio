# Requisitos del proyecto MÍO — Cambio CR-01

## Proyecto
Sistema de recargas virtuales para la tarjeta MÍO.

## Solicitud CR-01
**Nombre:** Control de pagos rechazados o pendientes.

**Problema:** Una recarga no debe mostrarse como exitosa si el proveedor de pago no ha confirmado la operación.

**Requisitos relacionados**
- **RF05:** Mostrar confirmación de recarga exitosa únicamente cuando el pago esté aprobado.
- **RF06:** Guardar y permitir consultar el historial con el estado real de cada operación.
- **RNF06:** Gestionar fallos de la transacción y evitar estados incorrectos.

## Regla de aceptación
- Pago aprobado: guardar la recarga como exitosa y mostrar confirmación.
- Pago rechazado: guardar el estado rechazado y avisar al usuario.
- Sin respuesta definitiva: guardar el estado pendiente de verificación; no mostrar éxito.
- Antes de repetir una operación pendiente, verificar su estado para reducir el riesgo de cobros duplicados.

## Caso de uso relacionado
CU01 — Realizar una recarga virtual de la tarjeta MÍO.
## CR-02: Consulta del historial de recargas

**Descripción:** Se propone agregar una opción para que los usuarios puedan consultar las recargas que han realizado en su tarjeta MÍO.

**Problema:** El usuario no tiene una forma clara de revisar sus recargas anteriores, sus fechas, los valores y el estado de cada operación.

**Requisito funcional RF06:** El sistema debe permitir consultar el historial de recargas del usuario que inició sesión, mostrando la fecha, el valor y el estado de cada recarga.

**Criterios de aceptación:**
- El usuario puede consultar sus recargas anteriores.
- Cada registro muestra la fecha, el valor y el estado de la recarga.
- Solo se muestran las recargas asociadas al usuario que inició sesión.

**Componentes relacionados:** Interfaz de usuario, Servicio de recargas y Datos y transacciones.

**Prioridad:** Media.

**Estado:** En revisión mediante GitHub Pull Request.
