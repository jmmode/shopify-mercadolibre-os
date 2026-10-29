# ECOMMERCE_MASTER — SHOPIFY Y MERCADO LIBRE
Versión GitHub inicial 1.1 — 2026-10-28. Este documento gobierna el modelo híbrido y referencia el expediente EP-V001; no sustituye sus evidencias.

## 0. Convenciones
- **VALIDADO:** evidencia verificable y fecha.
- **PENDIENTE:** requiere verificación de plataforma o fuente.
- **PROPUESTO:** arquitectura deseada, aún no implementada.
- **BLOQUEADO:** prohibida ejecución hasta resolver condición.
- **REQUIERE_DECISION:** solicita autorización explícita.
Nunca confundir propuestas de automatización con conectores operativos.

## 1. Misión y objetivos
Construir un negocio comercial multicanal rentable con intervención humana progresivamente menor. Prioridades: utilidad neta verificable, disponibilidad real, cumplimiento comercial, operaciones replicables, automatización controlada y autonomía por excepción.

## 2. Modelo comercial híbrido — VALIDADO
- **Inventario propio:** productos seleccionados con abastecimiento controlado.
- **Proveedores externos:** ampliación del catálogo únicamente con stock, despacho, garantía y costos confirmados.
- **Regla:** no activar publicaciones o promociones sobre stock ficticio, abastecimiento no validado o utilidad desconocida.
- **Canales:** Shopify (tienda propia) y Mercado Libre (marketplace). Ambos deben compartir reglas y catálogo, manteniendo las restricciones propias de cada canal.

## 3. Arquitectura funcional — PROPUESTA
Dirección y gobierno -> núcleo de catálogo, inventarios, proveedores, rentabilidad y pedidos -> Shopify / Mercado Libre -> pagos, logística, servicio posventa y analítica. Automatizaciones mediante integraciones autorizadas y mecanismos de seguimiento, idempotencia y reversión.

**GitHub es fuente canónica de documentación y código, no una base de datos de pedidos, saldos, compradores ni stock en tiempo real.**

## 4. Estructura documental
- 00_GOBIERNO: documento maestro, decisiones, estado y riesgos.
- 01_CANALES: configuración y operación por canal.
- 02_CATALOGO: esquema maestro por SKU.
- 03_PRODUCTOS: evidencia y SOP por producto (EP-V001, EP-V002...).
- 04_OPERACIONES: cumplimiento, postventa y garantías.
- 05_AUTOMATIZACIONES: conectores, flujos, pruebas y excepciones.
- 06_FINANZAS_Y_DATOS: indicadores y conciliación.
- 07_MARKETING: campañas y creatividades.

## 5. Estado inicial
### VALIDADO
- Se aprobó el modelo híbrido y la independencia de JUMOCOL OS.
- EP-V001 documentó una promoción de Mercado Libre de 5 % para el GPS Tracki 4G Mini desde 2026-10-28 hasta 2026-11-03, con precio inicial COP 199.000 y final COP 189.050; publicación #2847967396 y SKU TRK-GPS-4G-EP01, según capturas.
- La promoción aparecía ACTIVA en la evidencia de conversación.

### PENDIENTE
- Aceptación definitiva del video del GPS, puntaje de calidad posterior, costos y margen, ventas atribuibles a promoción.
- EP-V002 Fire TV Stick: stock mostrado 1.000 no comprobado, costos, proveedor, garantía, despacho.
- Auditoría del estado en vivo de Shopify, pagos, inventarios, productos y checkout.

### PROPUESTO
- Catálogo maestro compartido, automatización comercial multicanal, alertas de inventario, analítica y tablero de rentabilidad.
- No declarar estos sistemas funcionales hasta probarlos.

## 6. Pipeline y compuertas
0. Selección, proveedor y stock real.
1. Viabilidad financiera y margen antes/después de descuentos.
2. Calidad de ficha, título, fotografías, atributos y garantía.
3. Multimedia real, validación técnica y aceptación de plataforma.
4. Recomendaciones concretas de calidad.
5. Promoción controlada solo si pasa márgenes y abastecimiento.
6. Resultado posterior: visitas, conversión, órdenes, devoluciones y utilidad.
Cada compuerta conserva evidencia y estado.

## 7. Modelo mínimo por SKU — PROPUESTO
id_proceso, sku, canal, publicación, proveedor, referencia, costo, stock real, fecha de verificación, precio, comisiones, envío, otros cargos, garantía, devolución esperada, plazo de despacho, margen neto, estado de ficha, promoción, evidencia y responsable. El sistema de registro transaccional se decidirá aparte de GitHub.

## 8. Finanzas
Utilidad neta estimada por operación = cobro efectivamente recibido - comisiones - costo del producto - envío del vendedor - otros cargos - costos atribuibles. Si el cobro ya refleja descuento, no descontarlo de nuevo. Medir utilidad real por canal y por SKU, no solo facturación.

## 9. Automatizaciones — PROPUESTO
Fase 1: observación y lectura sin modificar plataformas.
Fase 2: alertas y reportes basados en estados fiables.
Fase 3: escrituras en entorno controlado con autorización, auditoría, reintentos e idempotencia.
Fase 4: operación supervisada por excepciones y límites de riesgo.
No activar operaciones de venta, precio o pedidos basándose solo en este documento.

## 10. Indicadores
Utilidad neta por SKU/canal; margen; conversión; costo de adquisición; devoluciones/reclamos; porcentaje de pedidos sin intervención manual; tiempo humano por pedido; utilidad por hora operativa. Cadencia propuesta: seguimiento semanal y decisión mensual sobre catálogo.

## 11. Backlog
P0: completar costos y calidad del GPS, auditar Fire TV Stick y estado de Shopify.
P1: catálogo maestro y reglas de rentabilidad con inventario real.
P2: conectores de lectura, reportes, alertas.
P3: automatizaciones de escritura probadas y autorizadas.

## 12. Gobierno y control multiagente
- GitHub privado independiente: jmmode/shopify-mercadolibre-os.
- Leer AGENTS.md, ESTADO_PROYECTO.md y DECISIONES.md al comenzar.
- Cambios mediante commits pequeños o PR con motivo, evidencia, pruebas y reversión.
- Nunca incorporar credenciales, datos de clientes, claves ni adjuntos financieros sensibles al control de versiones.
- Los archivos multimedia grandes y capturas sensibles permanecen en almacenamiento externo con referencias y permisos adecuados.
- No tocar jumocol-os ni life-os-runtime.

## 13. Fuente de evidencia
Consultar el expediente `03_PRODUCTOS/EP-V001_GPS_TRACKI/EP_V001_CIERRE_Y_SOP_PUBLICACIONES_MERCADO_LIBRE_2026-10-28.md` para cifras, procedimiento y limitaciones. Los datos comerciales fechados no sustituyen una revisión actual del panel.
