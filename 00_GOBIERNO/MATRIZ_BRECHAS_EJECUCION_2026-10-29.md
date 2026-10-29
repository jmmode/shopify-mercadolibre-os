# Matriz de brechas para activar ingresos — Shopify + Mercado Libre
**Fuentes:** Auditoría Claude v2 (reverificaciones 29-oct UTC); documento EP-V001 (capturas 28-oct); aclaración actual del propietario. Estado del canal NO consultado ahora en vivo.
**Prioridad:** corregir riesgo de venta no despachable -> validar pipeline de cobro y despacho -> publicar productos previamente investigados.

| Canal | Producto | Estado según evidencia | Bloqueo concreto | Acción mínima | Gate de salida |
|---|---|---|---|---|---|
| Mercado Libre | Fire TV Stick 4K EP-V002 | Publicación #3884220784, precio 239.900, stock visible 1000 NO verificado | Falso inventario; modelo de compra Costco contra disponibilidad | Pausar o corregir stock a unidades realmente disponibles; validar Costco, modelo original, costo y plazo de compra/envío; después reactivar | Stock cumplible y margen de hardware calculado, garantías y despacho claros |
| Mercado Libre | GPS Tracki 4G EP-V001 | Publicado, promoción 5 % según captura, final 189.050 | Costo/comisión Premium/envío sin comprobar | Revisar detalle ML y costo de adquisición; decidir promoción | Margen neto real, stock y calidad final confirmados |
| Shopify | Cable HDMI 3 m EP-V003 | ACTIVE y vinculado Dropify según Claude, Dropi 2159816 | Checkout, pago real, pedido a Dropi, despacho no probados | Revalidar stock, garantía y checkout; prueba E2E autorizada sin órdenes duplicadas | Cobro/pedido/despacho/liquidación comprobados |
| Shopify | Repetidor Wi-Fi EP-V004 | ACTIVE; Dropi 2208585 | Inventario discordante Shopify 102 vs Dropi 138, fotos y E2E | Corregir política stock, activos visuales, probar checkout | Inventario fiable y E2E validado |
| Shopify | Proyector HY300 EP-V005 | DRAFT a COP 179.900; Dropi 1102487 | Falta vincular Dropify y confirmar garantía | Vincular en panel sin alterar SKU manualmente ni pegar token; validar ficha y stock; pasar de borrador solo al cerrar gates | Vínculo, proveedor, inventario, garantía, ficha y checkout |
| Ambos | Nuevas publicaciones | Candidatas HDMI/repetidor/HY300 | Tarifas ML, envío y margen por canal desconocidos | Calcular rentabilidad por canal; reutilizar fichas y SOP probados | Publicación nueva con inventario y margen verificables |

## Lo que NO hay que reconstruir
- No rehacer los expedientes EP-V001 / EP-V002 ni las investigaciones Claude.
- No volver a diseñar el modelo comercial: híbrido aprobado.
- No confundir los flujos Costco Fire TV ML y Dropi Shopify.
- No asumir que la conexión técnica Dropify implica pedido y entrega verificadas.

## Orden ejecutivo
1. Mitigar inventario ficticio Fire TV ML y validar margen del GPS.
2. Cerrar checkout/cobro/Dropi/despacho del HDMI bajo autorización expresa; no ejecutar compras automáticamente.
3. Resolver stock y medios del repetidor.
4. Sincronizar HY300 mediante Dropify y publicar tras revisión.
5. Evaluar HDMI/repetidor/HY300 para ML únicamente con comisión real y stock/despacho viable.
6. Estandarizar los pasos completados en GitHub, sin sobreconstruir nuevos módulos.
