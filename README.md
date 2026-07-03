# 🤖 Ecosistema de Automatización IA para Clasificación Inteligente de Leads

## Proyecto Final – Arquitectura de Flujos con IA

**Alumno:** Martín Marinelli

---

# Descripción

Este proyecto implementa un ecosistema de automatización desarrollado en n8n para la clasificación inteligente de leads comerciales utilizando Inteligencia Artificial.

El flujo recibe automáticamente nuevos correos electrónicos desde Gmail, analiza su contenido mediante un modelo de IA, clasifica cada lead, registra la información en Airtable y solicita una validación humana antes de ejecutar la acción final.

---

# Tecnologías utilizadas

- n8n
- Gmail
- OpenRouter
- Airtable
- Human In The Loop (HITL)

---

# Funcionamiento del flujo

1. Se recibe un nuevo correo en Gmail.
2. El contenido es enviado al modelo de IA.
3. La IA clasifica el lead.
4. Se genera una respuesta sugerida.
5. La información se almacena en Airtable.
6. Se envía un correo para aprobación humana.
7. El flujo espera la decisión del usuario.
8. Si el lead es aprobado:
   - Se actualiza el estado en Airtable.
9. Si el lead es rechazado:
   - Se registra el rechazo en Airtable.

---

# Arquitectura

```
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
 ┌─┴───────────┐
 │             │
 ▼             ▼
Aprobado   Rechazado
 │             │
 ▼             ▼
Actualizar Airtable
```

---

# Archivos incluidos

- flujo_n8n.json
- Diagrama_Arquitectura.pdf
- Evidencias.pdf

---

# Autor

Martín Marinelli

Proyecto Final - Arquitectura de Flujos IA
