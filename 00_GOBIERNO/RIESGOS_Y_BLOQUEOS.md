# Riesgos y bloqueos

| Riesgo | Severidad | Medida |
|---|---|---|
| Stock ficticio de proveedor o plataforma | Alta | Confirmar inventario y despacho antes de vender |
| Rentabilidad no calculada | Alta | Margen por SKU con comisiones, envíos, descuentos y devoluciones |
| Venta no despachable | Alta | Bloquear catálogo sin abastecimiento confirmado |
| Automatización duplicando pedidos | Alta | Idempotencia, logs y pruebas antes de habilitar escritura |
| Estado de publicación sin evidencia actual | Media | Validación desde panel y conservación de fecha/captura |
| Fuga de credenciales o datos personales | Alta | Secret manager externo y no almacenar secretos en Git |
| Dependencia de un único agente o chat | Media | Documentación versionada, AGENTS.md y PRs |
