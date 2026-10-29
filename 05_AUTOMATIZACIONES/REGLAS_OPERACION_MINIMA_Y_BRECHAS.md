# Operación mínima — no reconstruir lo ya instalado

## Sistemas instalados/observados por auditoría Claude
Shopify Admin + Dropi + Dropify + Mercado Pago en tienda El Protector. Acceso a Drive desde Claude no disponible en corte, integración Mercado Libre en Claude ausente. GitHub canónico para documentos y código.

## Objetivo inmediato
No desplegar nuevas automatizaciones hasta cerrar la trazabilidad de orden pagada: checkout -> pago autorizado -> registro Shopify -> sincronización Dropify -> Dropi -> guía/despacho -> confirmación -> liquidación. Cada evento requiere ID, fecha, estado y evidencia.

## Matriz de brechas
- Publicación Shopify: 2 productos activos, HY300 borrador, siguiente fase de contenido y vinculación.
- Abastecimiento: retail local para Fire TV en ML (decisión), Dropi para SKU explícitamente vinculados de Shopify.
- Stock: no compartir artificialmente cifras entre canales; validar disponibilidad y reserva por operación.
- Finanzas: validar comisión ML Premium/Shopify + Mercado Pago y costo de flete.
- Marketing: medir por separado utilidad hardware y potencial activación autorizada de TVPlay.
- Prueba E2E: pendiente, sin automatización de escrituras no probadas.

## Criterio de salida por producto
PROVEEDOR_VALIDADO -> MARGEN_VALIDADO -> FICHA_VALIDADA -> PUBLICADO -> CHECKOUT_COMPROBADO -> COBRO_REAL_VALIDADO -> DESPACHO_REAL_VALIDADO. Los estados no se infieren unos de otros.
