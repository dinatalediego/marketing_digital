# 13 — Camino mínimo: Google/Maps → reputación → tracking → decisión

Fecha base: 2026-08-23

Objetivo: cerrar un ciclo pequeño y demostrable para Limpia Fast sin ampliar alcance.

La cadena es:

**presencia mínima confiable → descubrimiento local → contacto → cotización → reserva → servicio → reseña → dato → decisión → resultado observado**

No se marca una etapa como completada por haber escrito un documento o configurado una pantalla. Cada etapa exige una evidencia observable.

---

## Estado global

| Etapa | Estado inicial | Evidencia necesaria para declarar completado |
|---|---|---|
| 0. Página Facebook mínimamente confiable | PENDIENTE | Página visible con identidad, propuesta, servicios, WhatsApp y contenido mínimo |
| 1. Google Business Profile / Maps | PENDIENTE | Perfil creado y verificado; configuración de área de servicio visible |
| 2. Primer contacto atribuible a Google | PENDIENTE | Chat/llamada registrado con `source=google` |
| 3. Primera reserva atribuible | PENDIENTE | Reserva registrada con fuente y monto |
| 4. Primera reseña genuina | PENDIENTE | Reseña pública visible después de un servicio real |
| 5. Primera decisión basada en datos | PENDIENTE | Decisión escrita con evidencia y KPI objetivo |
| 6. Resultado observado | PENDIENTE | Medición posterior que confirme/mejore/refute la decisión |

---

# Etapa 0 — Página Facebook mínimamente confiable

Sí: antes de enviar leads pagados, la página debe tener suficiente contenido para no parecer vacía.

No necesitamos esperar semanas ni publicar 30 piezas. El mínimo es:

1. **Foto de perfil:** logo oficial Limpia Fast.
2. **Portada:** propuesta de valor + Huacho + servicios principales.
3. **Bio/presentación:** qué hace Limpia Fast y dónde atiende.
4. **Botón principal:** `Enviar mensaje de WhatsApp`.
5. **Datos básicos:** teléfono, zona de atención, horarios si están definidos.
6. **Contenido mínimo visible:** 4 publicaciones.

### Las 4 publicaciones mínimas

**P1 — Marca / qué hacemos**

- Limpia Fast.
- Sofás, colchones, alfombras y tapicería.
- Huacho.
- CTA a WhatsApp.

**P2 — Transformación**

- Antes/después real o demostrativo claramente presentado.
- Beneficio visual.
- CTA a cotizar.

**P3 — Proceso/confianza**

- Cómo se realiza la limpieza.
- Equipo, cuidado del mueble, extracción, atención profesional.

**P4 — Servicio específico**

- Empezar por sofá o colchón.
- Problema → resultado → CTA.

### Gate de salida

No declarar `COMPLETADO` hasta poder abrir la página como visitante y comprobar que esos elementos están visibles.

---

# Etapa 1 — Google Business Profile / Maps

Para un negocio que visita la casa del cliente, usar el modelo de **empresa de servicio en el área** salvo que exista un local real que reciba clientes con señalización y atención durante el horario publicado.

Google indica que los negocios de servicio pueden definir áreas de atención y que, si no atienden clientes en su dirección, deben ocultarla y mostrar únicamente el área de servicio.

Fuentes oficiales:

- https://support.google.com/business/answer/10514743
- https://support.google.com/business/answer/9157481
- https://support.google.com/business/answer/3038177

## Configuración mínima

- Nombre real de marca: `Limpia Fast`.
- Categoría principal coherente con limpieza del hogar/tapicería disponible en Google.
- Teléfono del negocio.
- Área de servicio: empezar por **Huacho** y solo agregar zonas realmente atendibles.
- Horarios reales.
- Servicios: sofás, colchones, alfombras, tapicería.
- Logo.
- Portada/fotos del trabajo.
- Descripción simple y comercial.

### No hacer todavía

- no crear múltiples perfiles para cubrir más zonas;
- no inventar una dirección comercial;
- no agregar áreas que operación no pueda atender;
- no gastar en Google Ads todavía.

### Gate de salida

`COMPLETADO` únicamente cuando:

1. el perfil esté creado;
2. esté verificado por Google;
3. la información crítica sea correcta;
4. el área de servicio esté configurada;
5. podamos comprobar que el perfil está disponible públicamente.

Si la verificación está pendiente, el estado es `EN_VERIFICACION`, no completado.

---

# Etapa 2 — Tracking mínimo desde la fuente

Archivo operativo:

`data/source_to_reservation_template.csv`

No necesitamos un CRM sofisticado para empezar.

Cada conversación nueva debe registrar al menos:

- fecha;
- fuente;
- campaña/pieza si aplica;
- servicio;
- zona;
- lead calificado sí/no;
- cotización sí/no;
- reserva sí/no;
- monto reservado;
- costo de pauta asociado si aplica;
- motivo de pérdida;
- reseña solicitada/recibida.

## Taxonomía inicial de `source`

Usar únicamente:

- `google`
- `facebook_organic`
- `instagram_organic`
- `meta_paid`
- `referral`
- `direct`
- `unknown`

No crear veinte fuentes al inicio.

### Gate de salida

El tracking está operativo cuando podemos tomar una conversación real y reconstruir:

**de dónde vino → qué pidió → si cotizó → si reservó → cuánto ingresó**.

---

# Etapa 3 — Primera reserva atribuible

No medir éxito por vistas del perfil.

La primera evidencia comercial fuerte es:

**un contacto identificado → una cotización → una reserva**.

Registrar:

- source;
- servicio;
- monto cotizado;
- monto reservado;
- fecha;
- costo publicitario si existió;
- observaciones.

### Gate de salida

Existe al menos una reserva real cuyo origen pueda explicarse razonablemente.

Una reserva no demuestra repetibilidad. Solo demuestra **señal**.

---

# Etapa 4 — Reputación después de servicio real

Después de completar el servicio y confirmar que el cliente está satisfecho:

1. pedir una reseña de forma directa y simple;
2. facilitar el enlace de Google;
3. no escribir la reseña por el cliente;
4. no fabricar reseñas;
5. responder públicamente cuando aparezca.

Fuente oficial sobre gestión de reseñas:

https://support.google.com/business/answer/3474050

## Micro-funnel de reputación

**servicio completado → solicitud de reseña → reseña publicada → respuesta de Limpia Fast → testimonio/evidencia reutilizable con permiso cuando corresponda**

### KPIs iniciales

- servicios completados;
- reseñas solicitadas;
- reseñas recibidas;
- `% servicio → reseña`;
- rating promedio.

### Gate de salida

Primera reseña genuina visible públicamente, originada después de un servicio real.

---

# Etapa 5 — Primera decisión basada en datos

La decisión debe tener esta estructura:

## Observación

¿Qué ocurrió?

Ejemplo:

> De 8 contactos de Google, 5 fueron calificados, 4 cotizados y 2 reservaron.

## Diagnóstico

¿Dónde parece estar la oportunidad o fuga?

## Decisión

Una sola acción.

Ejemplo:

> Aumentar el volumen y calidad de fotos del Perfil de Negocio y mantener el mismo proceso comercial durante 7 días más.

## KPI que debe cambiar

Ejemplo:

- contactos desde Google por semana;
- Google contact → reserva.

## Ventana de observación

Definir antes de ejecutar: por ejemplo, 7 o 14 días.

### Gate de salida

La decisión está escrita antes de observar el siguiente resultado y contiene al menos un KPI objetivo.

---

# Etapa 6 — Resultado observado

Al cerrar la ventana:

comparar **antes vs. después**.

Clasificar:

- `IMPROVED`: mejoró el KPI esperado;
- `NO_CHANGE`: no hubo cambio suficiente;
- `WORSE`: empeoró;
- `INCONCLUSIVE`: muestra/datos insuficientes.

No convertir `INCONCLUSIVE` en victoria o fracaso.

## Decisión siguiente

Solo cuatro posibilidades:

- **SCALE** — repetir/aumentar gradualmente;
- **HOLD** — mantener hasta tener más evidencia;
- **FIX** — corregir una fuga concreta;
- **KILL** — detener el experimento/canal/táctica.

---

# El ciclo mínimo completo

```text
IDEA
  ↓
hipótesis: Google/Maps puede generar demanda local de alta intención
  ↓
PRESENCIA MÍNIMA
Facebook confiable + Google Business Profile
  ↓
SEÑAL
contacto real
  ↓
TRACKING
source + servicio + cotización + reserva
  ↓
VENTA
servicio completado
  ↓
REPUTACIÓN
solicitud → reseña genuina
  ↓
DATO
conversión + ingreso + fuente
  ↓
DECISIÓN
SCALE / HOLD / FIX / KILL
  ↓
OBSERVACIÓN
IMPROVED / NO_CHANGE / WORSE / INCONCLUSIVE
```

---

# Qué NO forma parte de esta fase

Para preservar el alcance, quedan explícitamente fuera por ahora:

- Google Search Ads;
- CRM complejo;
- Conversions API;
- automatización avanzada de WhatsApp;
- programa de referidos sofisticado;
- dashboard BI completo;
- incrementalidad avanzada;
- múltiples perfiles de Google;
- expansión fuera de las zonas realmente atendibles.

Esos temas permanecen en el backlog existente y no bloquean este ciclo mínimo.

---

# Próximo paso operativo

1. Terminar capa mínima de Facebook.
2. Crear/solicitar verificación de Google Business Profile.
3. Empezar a registrar cada lead en `source_to_reservation_template.csv`.
4. Esperar evidencia real.
5. Recién entonces emitir la primera decisión.

**Estado actual del ciclo: PENDIENTE DE EJECUCIÓN EXTERNA.**

El repositorio ya contiene el método y la estructura de datos, pero no demuestra todavía que la página esté completa, que Google haya verificado el perfil, que exista una reserva atribuible ni que haya una reseña real.
