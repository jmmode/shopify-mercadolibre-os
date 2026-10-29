# Shopify El Protector — activación comercial (2026-10-29)

**Fuente:** consulta en vivo Shopify Admin API y Dropi MCP, 2026-10-29 ≈ 06:45 UTC (Claude). Complementa, sin reemplazar, las fichas EP-V003/004/005 propuestas en PR #1 y el estado consolidado de PR #2.
**Tienda:** El Protector, https://0mnu05-bs.myshopify.com · Basic · COP · sin contraseña de tienda (VALIDADO).

## 1. Estado por producto

| Producto | Shopify ID | Dropi ID / proveedor | Precio | Costo | Stock Dropi | Estado Shopify | Dropify | Estado comercial |
|---|---|---|---:|---:|---:|---|---|---|
| EP-V003 Cable HDMI 3 m | 10332290908246 | 2159816 / 179249 (SKU 0011466s6) | 29.900 | 16.000 | 400 | ACTIVE, publicado en Tienda online | Vinculado (metafield 07-oct) | VENDIBLE; E2E sin validar |
| EP-V004 Repetidor Wi-Fi | 10332291104854 | 2208585 / 75231 (SKU WR16Q3) | 69.900 | 36.900 | 138 | ACTIVE, publicado en Tienda online | Vinculado (metafield 07-oct) | VENDIBLE; E2E sin validar |
| EP-V005 Proyector HY300 | 10344421556310 | 1102487 / 6606 (SKU prov. T0122) | 179.900 | 98.000 | 112 | DRAFT (ya asignado a Tienda online) | **Sin vínculo** | BLOQUEADO por vínculo Dropify |

Enlaces activos:
- https://0mnu05-bs.myshopify.com/products/cable-hdmi-de-3-metros
- https://0mnu05-bs.myshopify.com/products/repetidor-wi-fi-amplificador-de-senal

Visibilidad: la portada usa la colección "all", así que muestra los productos activos. Comprobado por Admin API; el storefront no es accesible desde el entorno de Claude (proxy), por lo que la vista de comprador queda PENDIENTE de una revisión humana.

## 2. Pruebas y evidencia (VALIDADO 29-oct)
- Shopify: único pedido #1001 (06-oct, prueba, Fire TV). Ningún pedido de HDMI, repetidor ni HY300.
- Dropi: 0 pedidos.
- Por tanto **no existe evidencia** de cobro real, paso Shopify → Dropify → Dropi ni despacho. No se encontró prueba posterior en el repo ni en el proyecto.
- Envío Shopify: perfil general, Colombia COP 14.951 (zona "Colombia · Dropi" y "Domestic"); International inactiva.
- Canales de venta instalados: solo Tienda online y Point of Sale. **No** hay Google & YouTube ni Facebook & Instagram.

## 3. Cambios ejecutados por Claude (29-oct, reversibles)
| # | Producto | Cambio | Antes | Después |
|---|---|---|---|---|
| 1 | HDMI | Costo por artículo | vacío | 16.000 |
| 2 | Repetidor | Costo por artículo | vacío | 36.900 |
| 3 | HDMI | Tipo de producto / SEO | "Herramientas" / SEO vacío | "Cables HDMI" / título y meta descripción |
| 4 | Repetidor | Tipo de producto / SEO | "Otro" / SEO vacío | "Repetidores Wi-Fi" / título y meta descripción |
| 5 | HY300 | SEO | vacío | título y meta descripción (sin 4K, lúmenes ni apps de terceros) |
| 6 | HY300 | Canal Tienda online | no asignado | asignado (sigue DRAFT, invisible hasta activarlo) |

No se tocaron precios, inventario, imágenes, estado, Mercado Libre ni pagos. Reversión: restaurar los valores "Antes" en el admin de Shopify.

## 4. Margen y costo máximo de adquisición (ESTIMADO)
Supuestos: el cliente paga envío 14.951; flete Dropi prepago cotizado hoy (origen Bogotá): Bogotá 10.774 (Envía), nacional 14.450–14.610 (Cali/Medellín); comisión Shopify + Mercado Pago ≈ 5,92 % del total + 952 (dato previo, verificar en factura). Sin reserva por devoluciones.

| Producto | Total cliente | Contribución Bogotá | Contribución nacional | CPA máx. (equilibrio) | CPA objetivo (50 %) |
|---|---:|---:|---:|---:|---:|
| HDMI | 44.851 | 14.470 | 10.794 | 10.800 | 5.400 |
| Repetidor | 84.851 | 31.202 | 27.366 | 27.400 | 13.700 |
| HY300 | 194.851 | ≈ 73.600 (inferido) | 69.914 | 69.900 | 35.000 |

Lectura: el HDMI no soporta pauta propia; sirve como complemento o venta orgánica. Repetidor y HY300 sí admiten una prueba pagada pequeña.
Contraentrega: no consta configurada en el checkout. Si se activa, el flete sube ≈ 2.000–3.700 y Interrapidísimo rechaza recaudos menores a 45.000.

## 5. Bloqueos reales
| Bloqueo | Producto | Quién | Acción exacta |
|---|---|---|---|
| B1 Vínculo Dropify | HY300 | Julián | Admin Shopify → Apps → Dropify → importar/sincronizar Dropi 1102487 con el producto existente 10344421556310 (no crear uno nuevo, no sobrescribir precio ni imágenes). Claude verifica el metafield y activa. |
| B2 Flujo E2E sin probar | HDMI, repetidor | Julián (decisión) | Autorizar 1 pedido real controlado del HDMI (≈ 44.851) o aceptar que el primer pedido de cliente sea la prueba con monitoreo en Dropi. |
| B3 Garantía proveedor | los tres | Claude tras vínculo / Julián | Leer garantía en metafield Dropify o panel Dropi; mientras tanto aplica Ley 1480. |

Mejoras opcionales (no bloquean vender):
- Foto del repetidor: el archivo proviene de un CDN de Amazon (sufijo `_AC_SX679`) y otro proveedor Dropi usa la misma. Reemplazar por foto propia o del proveedor antes de pautar (riesgo de rechazo en Meta/Google).
- Inventario repetidor: Shopify 102 vs Dropi 138. No hay riesgo de sobreventa (Shopify muestra menos).
- Botón "View all" de la portada en inglés.

## 6. Captación de bajo costo (sin gasto)
1. Instalar canales gratuitos: **Google & YouTube** (listados gratuitos en Google Shopping) y **Facebook & Instagram** (catálogo, tienda IG, WhatsApp). Requiere a Julián (cuentas propias).
2. Publicaciones orgánicas en Facebook Marketplace / grupos locales de Bogotá para repetidor y HY300 con enlace a la ficha.
3. WhatsApp de El Protector: estado y lista de difusión con los dos enlaces activos.
4. Complemento: ofrecer el HDMI junto al repetidor/HY300 (sube ticket sin costo de adquisición adicional).

## 7. Propuesta de pauta (REQUIERE_DECISION, no ejecutar)
Solo después de B2 (flujo validado) y de cambiar la foto del repetidor: Meta Ads COP 20.000/día × 7 días (COP 140.000) repartidos entre HY300 y repetidor. Corte: si un producto gasta 2× su CPA objetivo sin venta (HY300 70.000; repetidor 27.400), se pausa.

## 8. Siguiente acción
1. Julián: B1 (vínculo HY300) y decisión B2.
2. Claude: verificar vínculo, activar HY300, registrar.
3. Julián: instalar Google & YouTube y Facebook & Instagram; Claude revisa el catálogo sincronizado.
4. Medir: pedidos Shopify y Dropi diarios durante la primera semana.

## 9. Actualización 2026-10-29 18:50 UTC
- **B1 resuelto:** Julián vinculó el HY300 en Dropify (metafield 06:55 UTC) y lo activó (publicado 06:57 UTC). SKU pasó a T0122 (proveedor), costo 98.000, precio 179.900, inventario 112 seguido por Shopify. Ficha activa: https://0mnu05-bs.myshopify.com/products/proyector-portatil-hy300-smart-110v-220v
- **B3 (HY300) resuelto:** garantía del proveedor 6606 (Quality / IMPORTODO), según el metafield: 30 días por defectos de fabricación (reparación o reemplazo); cambios en 3 días con producto sin abrir, flete a cargo del dropshipper; despacho desde bodega Bogotá, guías hasta la 1 p. m. de lunes a viernes.
- Claude añadió la garantía a la descripción del HY300 y quitó la etiqueta `borrador-pendiente-revision`.
- El nombre de la tienda en la integración Dropi es "Mi tienda 2" (dato del metafield): explica la referencia en jumocol-os y corresponde a El Protector.
- Pedidos: Shopify sigue con solo #1001 (prueba) y Dropi con 0. Decisión de Julián (06:44 UTC): el primer pedido de cliente será la prueba E2E, con revisión de Claude cada 12–24 h.
