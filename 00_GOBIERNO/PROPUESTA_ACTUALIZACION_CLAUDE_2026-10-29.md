# Integración de hallazgos Claude v2 y decisiones comerciales
Estado: PROPUESTA EN PR, no actualiza main. Fuentes: AUDITORIA_CLAUDE_INTEGRACION_ECOMMERCE_2026-10-28 v2 aportada por el usuario (corte 29-oct UTC) y aclaración expresa del propietario en la conversación.

## Decisión comercial del propietario — Fire TV Mercado Libre
- La publicación de **Fire TV Stick 4K de Mercado Libre** corresponde a una estrategia de compra física en **Costco** y posterior despacho; **NO depende de Dropi/Dropify/Shopify**. Es intención operativa confirmada por el propietario, **no** prueba de compra o existencia.
- Objetivo económico: margen del hardware modesto; desarrollar reputación del vendedor y usar la experiencia de entrega para ofrecer, con información clara, **un primer mes promocional de TVPlay**. Cualquier promoción o material de TVPlay requiere comprobar autorización de distribución, derechos aplicables y políticas de Mercado Libre; nunca ocultar condiciones, condicionar la compra del dispositivo o introducir publicidad engañosa.
- Fase futura: comprar lotes de Fire TV originales de proveedor verificado en Estados Unidos/Amazon/importador, con cálculo de impuestos, aranceles, garantía, importación y logística. PROPUESTO, no ejecutado.
- El inventario **1000 mostrado en ML no es real comprobado**. BLOQUEADO para nuevas ventas hasta corregir stock o pausar publicación según capacidad real de surtido, disponibilidad en Costco y plazo de despacho. Disponibilidad Costco, referencia exacta 4K, precio y despacho por operación siguen PENDIENTES.
- Distinguir **Fire TV 4K ML (EP-V002)** de **Fire TV HD borrador Shopify (Dropi ID 2120729, 0 stock en snapshot)**. No sincronizar SKUs ni inventarios entre ambos.

## Hallazgos operativos Claude v2
- Shopify: HDMI 3m ACTIVE, repetidor Wi-Fi ACTIVE; HY300 DRAFT pendiente vínculo Dropify. Estado auditado al 29-oct UTC, puede cambiar.
- Ningún cobro real ni despacho real Shopify/Dropi está validado en el informe; el pedido #1001 fue prueba. Por tanto **activo/publicado** no equivale a **listo para operar E2E**.
- Stock Shopify repetidor 102 vs Dropi 138 (snapshot); falta definir regla de sincronización.
- Precios/costos/stock y comisiones son fechados. No prometer margen neto sin comisión y logística verificadas.
- En Mercado Libre GPS EP-V001 tiene promoción 5% ACTIVA según captura 28-oct, pero faltan costo de compra, comisión Premium y envío real; REQUIERE_DECISION revisar o pausar si no es rentable.

## Propuesta de decisiones nuevas
- DEC-007: EP-V002 Fire TV 4K ML se abastece bajo modalidad compra física Costco contra pedido/stock confirmado. APROBADA COMO ESTRATEGIA; NO VALIDADA COMO OPERACIÓN.
- DEC-008: Shopify / Dropi es un flujo comercial independiente del Fire TV de Mercado Libre. APROBADA.
- DEC-009: TVPlay es oportunidad de adquisición asociada al hardware; beneficio promocional requiere reglas claras y revisión legal/plataforma. ESTRATEGIA APROBADA / EJECUCIÓN CONDICIONADA.
- DEC-010: priorizar publicar y vender productos investigados, sin crear un sistema nuevo antes de cerrar brechas de checkout, fulfillment, stock y margen. APROBADA.

## Recomendaciones para segundo PR
Actualizar DECISIONES, ESTADO_PROYECTO, RIESGOS_Y_BLOQUEOS y ECOMMERCE_MASTER por separado después de revisar este PR. Mantener registros históricos sin sobrescribir fuentes.
