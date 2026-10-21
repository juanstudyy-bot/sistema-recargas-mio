# Arquitectura básica — Cambio CR-01

## Proyecto
Sistema de recargas virtuales para la tarjeta MÍO.

## Componentes afectados
1. **Interfaz de usuario:** recibe la solicitud y muestra el resultado.
2. **Servicio de recargas:** valida la solicitud y decide el estado final según la respuesta del pago.
3. **Gestión de pagos:** solicita el procesamiento al proveedor externo y devuelve su respuesta.
4. **Proveedor externo (Nequi o banco):** responde si el pago fue aprobado, rechazado o no tiene resultado definitivo.
5. **Datos y transacciones:** guarda el resultado y el estado real de la recarga.
6. **Notificaciones y comprobantes:** informa el estado y genera comprobante solo para una recarga aprobada.

## Flujo
Usuario → Interfaz → Servicio de recargas → Gestión de pagos → Proveedor externo

Después de recibir la respuesta:
- Servicio de recargas → Datos y transacciones
- Servicio de recargas → Notificaciones y comprobantes → Interfaz

## Regla CR-01
El Servicio de recargas solo marca una operación como **exitosa** después de una confirmación de pago aprobada. Si el pago se rechaza, se guarda como **rechazado**. Si no hay respuesta definitiva, queda **pendiente de verificación**. La interfaz no debe mostrar una operación pendiente o rechazada como exitosa.

## Criterio de comprobación
Revisar los escenarios de pago aprobado, rechazado y sin respuesta. En cada caso, el estado guardado y el mensaje mostrado deben coincidir con el resultado del proveedor.
