# Integración Claude + ejecución comercial — propuesta para revisión
Fecha de decisión: 2026-10-28 (Bogotá). Estado: PROPUESTO PARA MERGE. Origen: instrucciones expresas del responsable + auditoría Claude v2 (2026-10-28 noche / 2026-10-29 UTC).

## Decisiones nuevas expresas
1. **EP-V002 Mercado Libre Fire TV Stick 4K**: abastecimiento inicial mediante compra minorista local en Alkosto, Éxito u otro proveedor verificable. NO se abastece automáticamente desde Dropi ni se vincula a la ficha HD en Shopify.
2. Modelo inicial de compra por pedido, sujeto a existencia, plazos, facturación, política de entrega, margen y garantías. Futuro: stock mayorista, importación o proveedor de EE. UU. (PROPUESTO).
3. El objetivo del Fire Stick incluye adquisición de clientes potenciales para TVPlay, incluso con baja utilidad del hardware; no se admiten pérdidas desconocidas ni promoción que infrinja políticas del marketplace o derechos de distribución.
4. En Shopify, aprovechar productos e integraciones ya configurados. No duplicar infraestructura: encontrar y cerrar brechas de checkout, cobro, pedido, despacho, comisiones y disponibilidad.

## Dos fuentes complementarias
- GitHub: gobierno, SOP EP-V001 Mercado Libre y expediente 4K EP-V002.
- Claude: resultados Shopify + Dropi + Dropify, SOP de lanzamiento de 10 pasos, candidatos HDMI/repetidor/HY300. **Auditoría v2 confirmada** con acceso de solo lectura al repositorio; no trasladar secretos ni JWT.
- Datos de plataforma en vivo tienen prioridad frente a snapshots documentados.

## Riesgos P0 (antes de vender)
- Fire TV ML #3884220784: 1.000 unidades visibles sin stock ni proveedor asegurado. Corregir inventario o pausar hasta poder cumplir dentro de las condiciones publicadas; acción en plataforma requiere aprobación y verificación.
- GPS ML #2847967396: descuento 5 % activo según captura; costo, comisión Premium y envío real no medidos. Validar margen o decidir detener promoción.
- Shopify: 0 cobros/despachos reales validados en auditoría Claude; no confundir publicaciones activas con operación E2E comprobada.
- No afirmar que ventas o capacidades están listas sin evidencia.

## Cambios documentales recomendados en PR posterior
- Conservar AGENTS, MASTER y DECISIONES; incorporar como decisión versionada tras revisión de este PR.
- Publicar copias íntegras D1-D10 desde Claude como fuentes originales después de verificar ausencia de secretos.
- Migrar SOP de 10 pasos y proceso Dropify, con enlaces a fuente; no copiar el valor del metafield `dropi._dropi_product` (JWT).
- Actualizar ESTADO_PROYECTO con fecha y resultados reales; mantener comparativa histórica.

## Criterio de cierre de integración
Evidencia original integrada, catálogo con SKU/canal y fuente, riesgos de venta no despachable resueltos, checkout y logística verificados, expedientes EP-V003..005 preparados para ejecución.
