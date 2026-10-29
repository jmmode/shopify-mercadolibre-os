# Contrato multiagente — SHOPIFY Y MERCADO LIBRE OS

## Lectura obligatoria
1. README.md
2. 00_GOBIERNO/ECOMMERCE_MASTER.md
3. 00_GOBIERNO/ESTADO_PROYECTO.md
4. 00_GOBIERNO/DECISIONES.md
5. SOP y expediente del producto correspondiente.

## Estados de evidencia
- VALIDADO: evidencia directa, fecha y fuente.
- PENDIENTE: requiere comprobación.
- PROPUESTO: diseño aún no implementado.
- BLOQUEADO: no ejecutar hasta resolver condiciones.
- REQUIERE_DECISION: necesita aprobación explícita.

## Seguridad y ejecución
- GitHub no es el inventario transaccional, ERP ni sistema de pagos.
- Nunca guardar tokens, claves, datos personales de compradores ni información financiera sensible.
- No inventar stock, costos, comisiones, autorizaciones ni estados de pedidos.
- No activar precios, descuentos, anuncios, compras, despacho o publicaciones sin validar rentabilidad, inventario, permisos y aprobación requerida.
- Para operaciones externas: verificar estado en vivo, idempotencia, registro, reversión y monitoreo.
- Toda modificación documentada debe indicar evidencia, decisión, impacto, prueba y estado resultante.
- Preferir cambios pequeños y revisables mediante ramas y pull requests.
- No modificar jumocol-os ni life-os-runtime para tareas de este proyecto.

## Prioridad de fuentes
Sistema comercial en vivo (para datos transaccionales) > evidencia fechada > expediente vigente > propuestas. Ante conflicto, marcar PENDIENTE y no inventar reconciliaciones.

## Convención de expedientes
EP-V001 corresponde al GPS Tracki 4G Mini; EP-V002 al Fire TV Stick 4K. Nuevos expedientes usan EP-VNNN. Mantener el histórico sin sobrescribir evidencias.
