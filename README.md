# 🤖 Ecosistema de Automatización IA para Clasificación Inteligente de Leads

## Proyecto Final – Arquitectura de Flujos con IA

**Alumno:** Martín Marinelli

---

# Descripción

Este proyecto implementa un ecosistema de automatización desarrollado en **n8n** para la clasificación inteligente de leads comerciales utilizando Inteligencia Artificial.

El flujo recibe automáticamente nuevos correos electrónicos desde Gmail, analiza su contenido mediante un modelo de IA, clasifica cada lead, registra la información en Airtable y solicita una validación humana antes de ejecutar la acción final.

Además, incorpora una ruta de manejo de errores que registra automáticamente cualquier fallo de procesamiento en Airtable para garantizar la resiliencia del flujo.

---

# Tecnologías utilizadas

- n8n
- Gmail
- OpenRouter (IA)
- Airtable
- Human In The Loop (HITL)

---

# Funcionamiento del flujo

1. Se recibe un nuevo correo en Gmail.
2. El contenido es enviado al modelo de IA.
3. La IA analiza y clasifica el lead.
4. Se genera una respuesta estructurada.
5. La información se registra en Airtable.
6. Se envía un correo para aprobación humana.
7. El flujo espera la decisión del usuario.

### Si el lead es aprobado

- Se actualiza el estado en Airtable como **Aprobado**.

### Si el lead es rechazado

- Se actualiza el estado en Airtable como **Rechazado**.

### Si ocurre un error

- El flujo registra automáticamente el incidente en **Airtable - Log Error**.

---

# Arquitectura

```text
Gmail
   │
   ▼
IA (OpenRouter)
   │
   ▼
Structured Output
   │
   ▼
Airtable
   │
   ▼
Human Approval
   │
 ┌───────────────┐
 ▼               ▼
Aprobado     Rechazado
 │               │
 ▼               ▼
Actualizar Airtable
```

---

# Archivos incluidos

- flujo_n8_ecosistema_ia.json
- Arquitectura_Ecosistema_IA.pdf
- Carpeta **/screenshots** con evidencias del flujo:

  - 01_flujo_principal
  - 02_ejecucion_exitosa
  - 03_airtable
  - 04_human_approval
  - 05_log_error

---

# Enlaces

### Repositorio GitHub

https://github.com/tinchodeep-rgb/tp-final-ecosistema-ia-mktcomar

### Base de datos Airtable (modo lectura)

https://airtable.com/appksuKFiTFJWOIn7/shrSUSKhpOs1sSde2

---

# Autor

**Martín Marinelli**

Proyecto Final – Arquitectura de Flujos IA
