# tp-final-ecosistema-ia-mktcomar
Proyecto Final - Ecosistema de Automatización IA para clasificación inteligente de leads con n8n, Airtable, IA y Gmail.
# TP Final - Ecosistema de Automatización IA

## Descripción

Este proyecto corresponde a la entrega final del curso de Arquitectura de Flujos con Inteligencia Artificial.

Se desarrolló un ecosistema de automatización utilizando n8n, Airtable, Gmail e Inteligencia Artificial para clasificar automáticamente leads comerciales y asistir en la generación de respuestas antes del contacto con el cliente.

---

## Tecnologías utilizadas

- n8n
- OpenRouter (LLM)
- Gmail
- Airtable
- Human in the Loop (HITL)

---

## Funcionamiento del flujo

1. Llega un nuevo email a Gmail.
2. El flujo se activa automáticamente.
3. La IA analiza el contenido del correo.
4. Clasifica el lead como:
   - VIP
   - Estándar
   - Descartar
5. Genera una respuesta sugerida.
6. Guarda toda la información en Airtable.
7. Envía un correo de aprobación al operador (Human in the Loop).
8. El operador puede aprobar o rechazar la propuesta antes de contactar al cliente.

---

## Arquitectura

Gmail Trigger

↓

IA (Clasificación y generación de respuesta)

↓

Structured Output Parser

↓

Airtable (Base de datos)

↓

Human Approval (Gmail)

↓

Actualización de estado

---

## Funcionalidades

- Clasificación automática de leads
- Generación de respuesta sugerida mediante IA
- Registro automático en Airtable
- Validación humana antes de enviar respuestas
- Manejo de estados del proceso
- Arquitectura preparada para ampliaciones futuras

---

## Archivos incluidos

- flujo_n8n.json
- Diagrama de Arquitectura.pdf
- Capturas de pantalla
- README.md

---

## Autor

Martín Marinelli

MKT.COM.AR
