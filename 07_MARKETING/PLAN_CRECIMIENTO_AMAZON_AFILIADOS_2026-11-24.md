# Plan de crecimiento — Amazon Associates (elprotector-20)

**Fecha:** 24 de noviembre de 2026 (America/Bogotá).
**Estado:** PROPUESTO. No ejecuta cambios en Amazon, Shopify, Mercado Libre ni ninguna cuenta externa. Toda acción en plataforma requiere confirmación explícita de Julián.
**Cuenta:** tienda `elprotector-20`, marketplace Estados Unidos.
**Fuente de métricas (VALIDADO):** lectura de solo consulta del panel de Amazon Associates, 24 de noviembre de 2026, y de la página de Creators API a las 3:40 a. m. (America/Bogotá) del mismo día.
**Fuentes de captación:** documentos del repositorio citados en la sección 2 (algunos viven en ramas, no en `main`).
**Política Associates (consulta web, misma fecha):** Operating Agreement actualizado el 15 de octubre de 2025; Program Policies actualizadas el 14 de abril de 2026; tema de ayuda “Offline Use of Associates Links and Ads”.

Este plan no inventa ventas, comisiones ni productos vendidos. Las cifras hacia adelante están marcadas como **meta (TARGET)** y no son hechos observados.

---

## Línea base — VALIDADO al 24 de noviembre de 2026

| Indicador | Valor observado |
|---|---|
| Clics (últimos 30 días) | 22 |
| Artículos pedidos | 4 (valor pedido USD 113,36) |
| Artículos enviados | 2 (ingresos por enviados USD 59,38; 19 de noviembre de 2026) |
| Artículos pedidos pendientes de envío | 2 (23 de noviembre de 2026; USD 53,98). Aún no generan comisión. |
| Ganancias | USD 2,38 (todas del mes en curso; comisión 4,01 % sobre los enviados) |
| Conversión clics → artículos pedidos | 18,18 % |
| Devoluciones | 0 |
| Categoría visible | “Other” (el detalle por producto está oculto por bajo volumen) |
| Origen del tráfico | 100 % fuera de Amazon, Estados Unidos |
| Próximo pago | USD 0 |
| Impuestos EE. UU. | Completos |
| Impuestos Canadá | Incompletos |
| Método de pago | No verificado en la revisión |
| Lista de incorporación (onboarding) | Pendiente |
| Aprobación final de la cuenta de asociados | VALIDADO: no cumplida. La página de Creators API (24 de noviembre de 2026, 3:40 a. m., America/Bogotá) muestra una X roja en el requisito «Tienes una cuenta de asociados aprobada». Amazon suele revisar las cuentas nuevas después de 3 ventas calificadas en 180 días. |
| PA-API / Creators API | Bloqueada por dos requisitos independientes: (1) la aprobación final de la cuenta de asociados, hoy no cumplida, y (2) al menos 10 ventas calificadas en los últimos 30 días. Al desbloquearse: hasta 2 aplicaciones, con 2 juegos de credenciales cada una. |

Herramientas ya disponibles en la cuenta: SiteStripe, verificador de enlaces, Native Shopping Ads, códigos promocionales, Creator Connections, programa Bounty, recompensas para creadores y gestión de tracking IDs.

Derivados de la línea base (no son datos nuevos del panel):

- EPC observado = 2,38 / 22 = **USD 0,108 por clic**.
- Valor medio por artículo pedido ≈ USD 28,34; por artículo enviado ≈ USD 29,69.
- De los 4 pedidos, solo 2 ya cuentan como enviados. Las 2 unidades del 23 de noviembre solo pasarán a “venta calificada” cuando se envíen y se paguen, según las reglas de Qualifying Purchases de Amazon (clic en un Special Link, compra en la ventana de sesión y envío/pago dentro de 180 días).
- Con 2 enviados, la cuenta aún está por debajo del umbral habitual de 3 ventas calificadas en 180 días que Amazon usa para revisar cuentas nuevas. Si los 2 pedidos pendientes se envían y se pagan, podría alcanzarse ese piso; eso no implica aprobación automática ni una fecha.

Lectura: la conversión 18,18 % es alta, pero con solo 22 clics no es estable. El cuello de botella actual es el volumen de clics, no la tasa. El mercado de la cuenta es Estados Unidos; eso condiciona qué captaciones del repo sirven para Afiliados y cuáles sirven para la tienda Shopify en Colombia.

---

## 1. Acciones inmediatas (Afiliados)

Objetivo: subir clics sin romper la conversión, medir cada fuente con un tracking ID propio y usar solo herramientas ya abiertas. Nada de esto se ejecuta sin confirmación de Julián. Estado de este bloque: PROPUESTO.

### 1.1 Higiene de la cuenta (antes de escalar)

1. Completar la lista de incorporación del panel.
2. Verificar y dejar documentado el método de pago. El próximo pago aparece en USD 0; Amazon no gira hasta alcanzar el mínimo de la cuenta (el umbral exacto queda PENDIENTE de lectura en el panel).
3. Completar la información fiscal de Canadá si se va a promocionar ese marketplace; si el foco sigue siendo solo EE. UU., dejarlo anotado y no bloquear el resto del plan por ese ítem.
4. Revisar enlaces existentes con el verificador de enlaces (Link checker).

### 1.2 Tracking IDs por canal

Crear un tracking ID adicional por fuente, bajo la tienda `elprotector-20`, para dejar de mezclar todo el tráfico en un solo tag. Propuesta de nomenclatura (TARGET, no IDs ya creados):

| Tracking ID propuesto | Uso |
|---|---|
| `elprotector-sitestripe` | Enlaces generados con SiteStripe |
| `elprotector-nativos` | Native Shopping Ads en el sitio |
| `elprotector-blog` | Entradas o fichas en elprotector / Shopify |
| `elprotector-youtube` | YouTube y Google |
| `elprotector-facebook` | Facebook (orgánico, no Marketplace de Bogotá; ver sección 2) |
| `elprotector-instagram` | Instagram |
| `elprotector-creator` | Creator Connections y Bounty |
| `elprotector-promo` | Códigos promocionales |

No usar un mismo ID para canales distintos. No hace falta crearlos todos el mismo día: bastan los de los canales que sí se vayan a usar en la primera semana.

### 1.3 SiteStripe

SiteStripe es la barra del navegador que genera Special Links (y short links) desde cualquier página de Amazon.com, con el tag correcto.

Acciones:

1. Activar SiteStripe en el navegador con el que se revisa Amazon y confirmar que el tag por defecto sea `elprotector-20` o el ID del canal.
2. Preparar una lista corta de Special Links de productos complementarios a lo que El Protector ya vende en Shopify, pero que la tienda no surte para el comprador de EE. UU.: accesorios de Fire TV Stick (control, alargador de control, soporte, Ethernet), cables y adaptadores HDMI de especificación distinta a la ficha colombiana, soportes o fundas para proyector, extensores o sistemas mesh Wi-Fi que no correspondan al SKU WR16Q3, y el Fire TV Stick oficial en Amazon.com cuando no se esté vendiendo ese dispositivo desde inventario propio (ver sección 2).
3. Publicar esos enlaces solo en propiedades que Amazon reconozca como Site (sitio, blog, redes asociadas), siempre con la divulgación obligatoria (sección 2.4).
4. No invitar a guardar el Special Link como favorito; el clic debe salir del Site.

### 1.4 Native Shopping Ads

Los anuncios nativos de Amazon se incrustan en el sitio y muestran productos de Amazon.com con el tag de la cuenta. Sirven para convertir visitas ya existentes del sitio sin armar ficha por ficha.

Acciones:

1. Colocar unidades nativas en páginas de El Protector donde tenga sentido un complemento (por ejemplo, cerca de las fichas del repetidor, el HDMI o el HY300, o en una página de “accesorios recomendados”), usando el tracking ID `elprotector-nativos`.
2. No mostrar precios ni disponibilidad “a mano”: si se citan, deben venir de las herramientas de Amazon o, más adelante, de la API, con la frecuencia de actualización que exija la licencia.
3. Comprobar que el anuncio no se confunda con el catálogo propio de Shopify (el visitante debe entender cuándo va a Amazon y cuándo compra en El Protector).
4. Medir clics y pedidos de ese ID durante 14 días antes de añadir más unidades.

Ojo: el tráfico actual de Afiliados es 100 % de EE. UU. Si la tienda Shopify recibe sobre todo visitas de Colombia, los anuncios nativos en esa vitrina pueden aportar poco a `elprotector-20`. En ese caso, priorizar un Site o una página en inglés orientada a EE. UU. (PROPUESTO; no existe aún en el repo).

### 1.5 Creator Connections, Bounty y códigos promocionales

1. **Creator Connections:** revisar campañas abiertas de marcas alineadas con streaming, Wi-Fi, cables y proyección. Postular solo a las que se puedan cumplir con contenido real (foto o video propio, no recortes de Amazon ni fotos de terceros; ver la foto del repetidor en la sección 2). Usar el ID `elprotector-creator`.
2. **Amazon Bounty:** priorizar acciones con bono fijo (cuenta, Prime, apps o dispositivos, según lo que el panel muestre como elegible ese día). No asumir montos: copiar la tarifa vigente del programa al registrar cada campaña.
3. **Códigos promocionales:** usarlos solo cuando Amazon los ofrezca para una campaña concreta, con el ID `elprotector-promo`, y sin inventar descuentos propios de Amazon.
4. **Recompensas para creadores:** dejarlas como complemento; no construir el plan alrededor de un premio no confirmado.

Estas tres palancas no sustituyen el tráfico propio. Sirven para acelerar clics calificados cuando ya hay un Site y divulgación correcta.

### 1.6 Orden de la primera semana (TARGET de ejecución, no de resultados)

1. Higiene de cuenta y tracking IDs de los canales que sí se usarán.
2. SiteStripe + lista corta de Special Links complementarios.
3. Una unidad de Native Shopping Ads en un Site con visitas de EE. UU., o documentar que el sitio actual no las tiene (PENDIENTE de medición).
4. Revisión de Creator Connections y Bounty, sin postular a ciegas.
5. Solo después, las captaciones del repo (sección 2), separando con claridad lo que vende El Protector en Colombia y lo que apunta a Afiliados en EE. UU.

---

## 2. Captaciones gratuitas ya documentadas en el repositorio

Las acciones de esta sección ya están escritas en el repo como captación de bajo costo para **Shopify El Protector** (Colombia, COP). No son, por sí solas, un plan de Amazon Associates. Aquí se citan con su fuente y se indica cómo se pueden cruzar —con cuidado— con Special Links de Afiliados.

### 2.1 Qué dice el repo (citas)

**A. Canales gratuitos de Shopify, Marketplace, grupos de Bogotá, WhatsApp y HDMI como complemento**

Fuente: `01_CANALES/SHOPIFY/ACTIVACION_COMERCIAL_2026-10-29.md`, rama `claude/activacion-comercial-shopify-2026-10-29`, sección 6 (“Captación de bajo costo (sin gasto)”), corte 29 de octubre de 2026. El documento no está en `main` a la fecha de este plan.

1. Instalar canales gratuitos: **Google & YouTube** (listados gratuitos en Google Shopping) y **Facebook & Instagram** (catálogo, tienda de Instagram, WhatsApp). Requiere a Julián (cuentas propias).
2. Publicaciones orgánicas en Facebook Marketplace y grupos locales de Bogotá para el repetidor y el HY300, con enlace a la ficha de Shopify.
3. WhatsApp de El Protector: estado y lista de difusión con los dos enlaces activos de Shopify (en esa fecha: HDMI y repetidor; el HY300 se activó el mismo día más tarde, sección 9 del mismo documento).
4. Complemento: ofrecer el HDMI junto al repetidor o al HY300 para subir el ticket sin costo de adquisición adicional.

La misma fuente, sección 2, deja constancia de que al 29 de octubre de 2026 los canales de venta instalados eran solo Tienda online y Point of Sale: **no** había Google & YouTube ni Facebook & Instagram. La sección 8 pide a Julián instalarlos y a Claude revisar el catálogo sincronizado. Ese estado posterior no se revalidó el 24 de noviembre de 2026 (queda PENDIENTE).

**B. Foto del repetidor Wi-Fi**

Misma fuente, sección 5, mejoras opcionales: el archivo de la foto del repetidor proviene de un CDN de Amazon (sufijo `_AC_SX679`) y otro proveedor Dropi usa la misma imagen. Reemplazarla por foto propia o del proveedor antes de pautar, por riesgo de rechazo en Meta/Google.

Confirmado también en:

- `03_PRODUCTOS/EP-V004_REPETIDOR_WIFI/FICHA_EP-V004.md`, rama `integracion/claude-brechas-comerciales-2026-10-28`: “fotos de tercero pendientes” y “derechos sobre fotografías pendientes”.
- `00_GOBIERNO/MATRIZ_BRECHAS_EJECUCION_2026-10-29.md`, misma rama: acción mínima del repetidor incluye “corregir […] activos visuales”.

**C. Captación orgánica, sin pauta paga**

Fuente: `01_CANALES/SHOPIFY/CIERRE_3_PRODUCTOS_ACTIVOS_2026-10-29.md`, rama `shopify/cierre-3-productos-activos-2026-10-29`, seguimiento punto 4: “Captación orgánica para 3 productos; ningún presupuesto pagado ni campaña lanzados.”

La propuesta de pauta Meta (COP 20.000/día × 7 días) en la sección 7 de `ACTIVACION_COMERCIAL_2026-10-29.md` está en estado REQUIERE_DECISION y **no forma parte de este plan**. Este documento solo retoma las captaciones gratuitas.

### 2.2 Cómo se cruzan con Amazon Afiliados

Regla de separación: los enlaces de las fichas de Shopify (HDMI, repetidor, HY300) venden el catálogo propio de El Protector. Los Special Links de `elprotector-20` mandan al comprador a Amazon.com (EE. UU.). No intercambiar unos por otros ni poner un tag de Afiliados sobre un producto que El Protector está vendiendo en su propia tienda.

Usos compatibles (PROPUESTO):

| Captación del repo | Uso para Shopify (Colombia) | Uso para Afiliados (EE. UU.) |
|---|---|---|
| Instalar Google & YouTube y Facebook & Instagram en Shopify | Publicar el catálogo propio (HDMI, repetidor, HY300) en Shopping, catálogo e Instagram Shop | Esos canales no generan por sí solos clics a Amazon.com. Sí pueden, más adelante, alojar contenido del Site con divulgación y Special Links de **complementos que El Protector no surte**, dirigidos a audiencia de EE. UU. |
| Facebook Marketplace y grupos de Bogotá | Enlazar fichas Shopify del repetidor y el HY300 | No son un canal natural para `elprotector-20`: la cuenta de Afiliados vende en Amazon.com y el tráfico actual es 100 % de EE. UU. No poner Special Links en grupos locales de Bogotá esperando comisiones de Amazon EE. UU. |
| WhatsApp de El Protector | Estado y difusión de las fichas Shopify, con las reservas de la sección 2.4 si alguna vez se mezclaran Special Links | Ver 2.4. Special Links en chats o listas de difusión solo si hay opt-in previo y baja sencilla. |
| Cambiar la foto del repetidor | Desbloquea captación orgánica y, si un día se aprueba, pauta en Meta/Google | Evita reutilizar material de Amazon o de terceros en creatividades, también en Creator Connections. |
| HDMI como complemento | Ofrecer el HDMI de El Protector junto al repetidor o al HY300 | En el Site de EE. UU., recomendar por Afiliados accesorios que la tienda no tiene: cables de otra especificación, switches HDMI, soportes de proyector, accesorios oficiales de Fire TV Stick. |
| Fire TV Stick (EP-V002) | En `main`, EP-V002 sigue BLOQUEADO para promoción propia hasta auditar abastecimiento, costos y rentabilidad (`03_PRODUCTOS/EP-V002_FIRE_TV_STICK/FICHA_EP-V002.md`). En Shopify hay un Fire TV Stick HD en DRAFT, sin inventario comprobado (`CIERRE_3_PRODUCTOS_ACTIVOS_2026-10-29.md`). | Mientras El Protector no venda ese dispositivo con inventario validado hacia EE. UU., un Special Link al Fire TV Stick oficial en Amazon.com (y accesorios) es un complemento legítimo del relato de streaming de la marca, con divulgación. No presentarlo como stock de El Protector. |

DEC-005 (no promocionar sin confirmar inventario y margen) sigue aplicando a las ventas propias. No impide publicar Special Links de Amazon, porque esos pedidos los cumple Amazon, no el inventario de El Protector.

### 2.3 Orden práctico de las captaciones gratis (TARGET)

1. Cambiar la foto del repetidor **antes** de usarla en Marketplace, grupos, Instagram, YouTube o Creator Connections.
2. Instalar en Shopify los canales Google & YouTube y Facebook & Instagram (pendiente de confirmación de Julián; no se toca la tienda desde este plan).
3. Publicar en Marketplace y grupos de Bogotá solo fichas Shopify del repetidor y el HY300, con foto propia.
4. Usar el WhatsApp de El Protector para las fichas Shopify, no para Special Links, salvo que se cumpla la sección 2.4.
5. En paralelo, y solo para audiencia de EE. UU., construir el tráfico de Afiliados con SiteStripe, anuncios nativos y, si se abre, una página o perfil en inglés con divulgación.

### 2.4 Reglas de Amazon Associates que condicionan WhatsApp, correo y mensajes privados

Consulta web del 24 de noviembre de 2026. Fuentes oficiales:

- [Associates Program Operating Agreement](https://affiliate-program.amazon.com/help/operating/agreement) (actualizado el 15 de octubre de 2025), sección 5: en el Site o en cualquier lugar donde Amazon autorice usar contenido del programa debe aparecer, de forma clara y destacada, la frase *“As an Amazon Associate I earn from qualifying purchases.”* o una sustancialmente equivalente permitida antes. Fuera de esa divulgación, no hay que presentar a Amazon como patrocinador ni embellecer la relación.
- [Associates Program Policies](https://affiliate-program.amazon.com/help/operating/policies/) (actualizadas el 14 de abril de 2026), limitaciones promocionales: no se permiten actividades promocionales fuera de línea (material impreso, correo postal, solicitud oral, etc.). Sí se pueden incluir Special Links en correos, SMS y mensajes directos de los Sites de redes sociales, **siempre que esas comunicaciones sean solicitadas (opt-in del destinatario)** y cumplan el Acuerdo, las Trademark Guidelines y las Amazon Brand Usage Guidelines. Amazon puede pedir muestras y una certificación escrita. Quien envía el mensaje es el “Sender” para efectos de normas como CAN-SPAM.
- [Offline Use of Associates Links and Ads](https://affiliate-program.amazon.com/help/node/topic/GQ5CMSPVXBXSFDFV): los Special Links solo pueden usarse en correos, SMS o publicaciones en redes hacia destinatarios que hayan dado opt-in y que tengan una forma fácil de darse de baja.

Implicación para el WhatsApp de El Protector (BLOQUEADO para Special Links hasta cumplir las condiciones):

- La idea del repo (estado y lista de difusión con los enlaces de Shopify) es válida para el catálogo propio, porque esos no son Special Links.
- Un chat 1:1 o una lista de difusión de WhatsApp se trata, a efectos del Acuerdo, como mensaje directo o asimilable a SMS. **No** se deben enviar Special Links de Amazon a contactos que no hayan pedido expresamente recibir esas recomendaciones, ni en mensajes en frío.
- Si en el futuro se usa WhatsApp para Afiliados, hace falta: (1) opt-in documentado, (2) baja fácil en cada envío, (3) divulgación clara junto al enlace, (4) tag correcto. Un canal o estado al que la persona se suscribe de forma voluntaria se acerca más a una publicación en un Site, pero WhatsApp no está nombrado de forma explícita en la política; ante la duda, aplicar el criterio más estricto (opt-in + divulgación) y no improvisar.
- Tampoco usar Special Links en material impreso, ni dictarlos de forma oral como solicitud comercial.

---

## 3. Estrategia para desbloquear la API

Meta (TARGET): abrir PA-API / Creators API. Hay **dos requisitos independientes**, no uno solo:

1. **Paso 0:** aprobación final de la cuenta de asociados (hoy no cumplida; ver línea base).
2. **Después:** al menos 10 ventas calificadas en una ventana móvil de 30 días.

Cumplir el segundo sin el primero no desbloquea la API.

Estado al 24 de noviembre de 2026: 2 artículos enviados el 19 de noviembre (cuentan si se confirman como Qualifying Purchases) y 2 pedidos del 23 de noviembre que **aún no cuentan** hasta que se envíen y se paguen. En el mejor caso, al enviarse esos 2, la cuenta iría en 4 calificadas en 180 días (suficiente, en la práctica habitual, para que Amazon revise la cuenta) y seguiría por debajo de las 10 en 30 días. Para el umbral de la API, faltarían **6 ventas calificadas más** en la ventana de 30 días. Además, las del 19 de noviembre saldrán de esa ventana de 30 días hacia el 19 de diciembre de 2026: hay que reponerlas, no solo sumar.

No se proyecta aquí qué producto se venderá: el panel oculta el detalle por bajo volumen.

### 3.0 Paso 0 — lograr la aprobación final de la cuenta

VALIDADO (página de Creators API, 24 de noviembre de 2026, 3:40 a. m., America/Bogotá): el requisito «Tienes una cuenta de asociados aprobada» aparece con una X roja. La cuenta **no** tiene todavía la aprobación final.

Amazon suele revisar las cuentas nuevas después de **3 ventas calificadas en 180 días**. Esa revisión es un paso distinto, y previo, al umbral de 10 ventas en 30 días.

Acciones (TARGET; no se ejecuta nada en la plataforma sin confirmación de Julián):

1. Priorizar que los pedidos pendientes del 23 de noviembre se conviertan en ventas calificadas (envío y pago) y, si hace falta, completar una tercera venta calificada dentro de 180 días para entrar en la revisión habitual.
2. No solicitar la API ni dar por desbloqueada la cuenta mientras el panel siga mostrando esa X roja, aunque se acumulen clics o pedidos.
3. Cuando Amazon apruebe la cuenta, dejar constancia fechada en el seguimiento semanal y solo entonces avanzar al umbral de 10 ventas calificadas en 30 días (sección 3.1) como requisito adicional de la API.
4. La aprobación la decide Amazon; llegar a 3 ventas calificadas no garantiza ni el resultado ni la fecha.

### 3.1 Rampa semanal (TARGET, no pronóstico)

Partir de la línea base de 22 clics y 4 pedidos en 30 días (~5–6 clics y ~1 pedido por semana). La conversión 18,18 % se usa solo como referencia; si cae al subir el volumen, se prioriza calidad del clic sobre cantidad.

| Semana | Periodo objetivo | Meta de clics | Meta de artículos pedidos | Meta acumulada de enviados en 30 días | Foco |
|---|---|---:|---:|---:|---|
| Base | 25 oct – 24 nov 2026 (observado) | 22 (hecho) | 4 (hecho) | 2 enviados + 2 pendientes | Línea base VALIDADA |
| 1 | 25 nov – 1 dic 2026 | 40 | 3–4 | 4–6 (si llegan los pendientes del 23 nov) | Higiene, IDs, SiteStripe, primera unidad nativa, foto del repetidor; apuntar a 3 ventas calificadas en 180 días (paso 0) |
| 2 | 2–8 dic 2026 | 60 | 4–5 | 6–8 | Creator Connections / Bounty si hay encaje; contenido en Site de EE. UU.; canales Shopify ya instalados para el catálogo propio |
| 3 | 9–15 dic 2026 | 70 | 4–5 | 8–10 | Doblar lo que tenga mejor EPC por tracking ID; pausar fuentes con clics y 0 pedidos |
| 4 | 16–22 dic 2026 | 80 | 5–6 | ≥ 10, reponiendo las ventas del 19 nov que salen de la ventana | Cierre del umbral de API; no relajar divulgación ni opt-in |

Si en la semana 2 no hay al menos el doble de clics que en la base semanal, el problema es de distribución, no de API: no tiene sentido esperar el desbloqueo sin un Site que ya reciba visitas de EE. UU.

Criterio de corte (TARGET): si un tracking ID acumula 30 clics en 14 días sin un solo artículo pedido, se revisa el destino del enlace y el mensaje antes de seguir usándolo.

### 3.2 Qué hacer cuando se desbloquee la API

Solo cuando la cuenta tenga la aprobación final **y** se hayan alcanzado las 10 ventas calificadas en 30 días:

1. Solicitar el acceso a PA-API / Creators API desde el panel (no antes).
2. Crear como máximo lo autorizado: hasta 2 aplicaciones, con hasta 2 juegos de credenciales cada una. Guardar claves fuera de GitHub (AGENTS.md: el repo no almacena tokens ni credenciales).
3. Usos de mayor valor, en este orden:
   - Generar Special Links y catálogos en lote (publicación masiva de complementos, no del inventario Shopify).
   - Armar fichas o comparativas en el Site con título, imagen y disponibilidad/precio tomados de la API, respetando la frecuencia de actualización de la licencia (si el precio no se refresca al menos cada hora, hay que mostrar fecha y hora).
   - Mantener un ID de seguimiento por canal también en las llamadas de la API.
4. No usar la API para alertas de precio ni para prácticas prohibidas en las Program Policies.
5. Seguir midiendo ventas calificadas en la ventana móvil: si bajan de 10, el acceso se puede perder. El objetivo posterior (TARGET) es sostener ≥ 10 enviados / 30 días, no hacer un pico único.
6. Cualquier automatización de escritura o publicación masiva sigue las fases de `00_GOBIERNO/ECOMMERCE_MASTER.md` (primero lectura, luego pruebas autorizadas) y DEC-006. Este plan no autoriza a conectar la API ni a publicar en masa.

---

## 4. Métricas semanales

Cadencia: revisión cada semana, el lunes, con el reporte de Associates (y, cuando existan, los desgloses por tracking ID). No guardar en este repo capturas con datos personales de compradores ni credenciales.

Fórmulas:

- Conversión = artículos pedidos / clics.
- EPC = ganancias en USD / clics.
- Se siguen por separado pedidos y enviados: la comisión y la venta calificada dependen del envío y del pago, no del pedido solo.

### 4.1 Plantilla

Copiar una fila por semana. La primera fila es la línea base VALIDADA (últimos 30 días al 24 de noviembre de 2026), no una semana aislada.

| Semana | Periodo | Clics | Pedidos (artículos) | Enviados | Conversión | Ganancias USD | EPC USD | Ventas calificadas en 30 días móviles | Tracking ID destacado (clics / pedidos / ganancias) | Canal / fuente | Notas |
|---|---|---:|---:|---:|---:|---:|---:|---:|---|---|---|
| Base 30d | 25-oct a 24-nov-2026 | 22 | 4 | 2 | 18,18 % | 2,38 | 0,108 | 2 (2 pendientes de envío) | Sin IDs desagregados (PENDIENTE) | 100 % off-Amazon, EE. UU. | Categoría “Other” 4,01 %; detalle por producto oculto |
| 1 | 25-nov a 1-dic-2026 |  |  |  |  |  |  |  |  |  |  |
| 2 | 2-dic a 8-dic-2026 |  |  |  |  |  |  |  |  |  |  |
| 3 | 9-dic a 15-dic-2026 |  |  |  |  |  |  |  |  |  |  |
| 4 | 16-dic a 22-dic-2026 |  |  |  |  |  |  |  |  |  |  |

Columnas mínimas a rellenar también cuando ya haya IDs: una nota o una tabla anexa por tracking ID (`elprotector-sitestripe`, `elprotector-nativos`, `elprotector-blog`, `elprotector-youtube`, `elprotector-facebook`, `elprotector-instagram`, `elprotector-creator`, `elprotector-promo`) con clics, pedidos, enviados, conversión, ganancias y EPC.

Otros controles semanales, sin inventar umbrales no vistos en el panel:

- Pedidos del periodo que siguen sin enviarse.
- Devoluciones (base: 0).
- Próximo pago y si el método de pago ya quedó verificado.
- Estado de aprobación de la cuenta (requisito «Tienes una cuenta de asociados aprobada»: sí / no) y conteo de ventas calificadas en 180 días, de cara al paso 0.
- Estado de la API (bloqueada / desbloqueada) y conteo de ventas calificadas en 30 días.
- Cumplimiento de divulgación y de opt-in en cualquier mensaje.

### 4.2 Qué decidir con esas cifras

- Si los clics suben y la conversión se sostiene cerca de la base, mantener el canal y reforzar el de mejor EPC.
- Si los clics suben y la conversión se derrumba, revisar pertinencia del enlace y la promesa del contenido; no “llenar” de anuncios nativos.
- Si hay pedidos que no se envían, no contarlos como avance hacia las 10 ventas calificadas.
- Si al 22 de diciembre de 2026 no se llega a 10 calificadas, no forzar pauta paga desde este documento: volver a la decisión ya abierta de Meta Ads en el repo, que sigue en REQUIERE_DECISION y es para Shopify, no para Afiliados.

---

## 5. Fuera de alcance y reversión

- Este archivo no modifica Amazon Seller Central, Shopify, Mercado Libre, Meta, Google ni WhatsApp.
- No publica productos, no crea campañas y no solicita la API.
- No actualiza `DECISIONES.md` ni el estado del proyecto: no hay decisión nueva aprobada.
- Reversión documental: retirar este archivo (y su mención en `07_MARKETING/README.md`) mediante un commit o el cierre del pull request, si se incorporó por PR.

## Referencias

- Lectura de solo consulta del panel Amazon Associates, tienda `elprotector-20`, 24 de noviembre de 2026 (America/Bogotá).
- Lectura de solo consulta de la página de Creators API, 24 de noviembre de 2026, 3:40 a. m. (America/Bogotá): X roja en «Tienes una cuenta de asociados aprobada».
- `01_CANALES/SHOPIFY/ACTIVACION_COMERCIAL_2026-10-29.md` (rama `claude/activacion-comercial-shopify-2026-10-29`).
- `01_CANALES/SHOPIFY/CIERRE_3_PRODUCTOS_ACTIVOS_2026-10-29.md` (rama `shopify/cierre-3-productos-activos-2026-10-29`).
- `03_PRODUCTOS/EP-V004_REPETIDOR_WIFI/FICHA_EP-V004.md` y `00_GOBIERNO/MATRIZ_BRECHAS_EJECUCION_2026-10-29.md` (rama `integracion/claude-brechas-comerciales-2026-10-28`).
- `03_PRODUCTOS/EP-V002_FIRE_TV_STICK/FICHA_EP-V002.md` y `00_GOBIERNO/DECISIONES.md` en `main`.
- [Operating Agreement](https://affiliate-program.amazon.com/help/operating/agreement), [Program Policies](https://affiliate-program.amazon.com/help/operating/policies/), [Offline Use of Associates Links and Ads](https://affiliate-program.amazon.com/help/node/topic/GQ5CMSPVXBXSFDFV).
