# Shopify El Protector — estado consolidado de auditoría Claude v2
**Origen:** auditoría recibida `AUDITORIA_CLAUDE_INTEGRACION_ECOMMERCE_2026-10-28(1).md`, revisión del 29-oct ~03:00 UTC. **Snapshot histórico, no consulta actual.**

Tienda: El Protector, `0mnu05-bs.myshopify.com`; Basic, COP. Envío configurado COP 14.951; internacional inactivo.

| Producto | Shopify ID | Estado | Precio COP | Dropi ID | Costo COP | Stock Dropi en consulta | Dropify | Bloqueo |
|---|---|---|---:|---|---:|---:|---|---|
| Cable HDMI 3m | 10332290908246 | ACTIVE | 29.900 | 2159816 | 16.000 | 400 | vinculado | Checkout, cobro y despacho sin validar |
| Repetidor Wi-Fi | 10332291104854 | ACTIVE | 69.900 | 2208585 | 36.900 | 138 | vinculado | Shopify muestra 102; no sincronización continua |
| Proyector HY300 | 10344421556310 | DRAFT | 179.900 | 1102487 | 98.000 | 112 | sin vínculo | Vincular vía panel Dropi, revisar garantía |
| Fire TV Stick HD | 10318067531862 | DRAFT | 190.000 | 2120729 | — | 0 (snapshot 07-oct) | vínculo no despachable | Producto distinto al EP-V002 4K ML |

Hallazgos: pedido #1001 fue de prueba, sin transacción real despachada; Dropi reportó 0 pedidos. No hay evidencia de `COBRO_REAL_VALIDADO` ni `DESPACHO_REAL_VALIDADO`.

**Integraciones existentes:** Shopify MCP (lectura/escritura según Claude), Dropi MCP (consulta de productos y órdenes, cotización y potencial create_order), Dropify instalado. El vínculo Dropify no se crea manualmente escribiendo el metafield con JWT; se realiza en panel autorizado. Integración instalada ≠ ciclo E2E probado.

**Finanzas:** comisiones estimadas de Shopify + Mercado Pago ≈ 5,92 % del total + COP 952; revisar factura y pasarela; transporte Dropi estimado por ciudad de snapshots anteriores. No asumir margen definitivo.

## Brechas reales para operar
1. Probar checkout y pago real controlado (requiere autorización).
2. Verificar que orden pagada llega correctamente a Dropify/Dropi y se despacha.
3. Resolver política de disponibilidad y sincronización (Shopify 102 vs Dropi 138 para repetidor).
4. Completar vinculación y garantía HY300 sin inventar prestaciones.
5. Preparar fichas y material aprobado para Mercado Libre con tarifas por categoría verificadas.
