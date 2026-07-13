# Psicología Social LATAM — Mobile-first email template

Template para la alerta semanal de artículos académicos sobre psicología social en contextos latinoamericanos.

## Archivos

- `mobile-first.html`: versión HTML real, optimizada para Gmail móvil.
- `plain-text.txt`: versión de respaldo en texto plano para el campo `body`.

## Uso esperado con Gmail

Al enviar el correo, usar dos cuerpos:

```js
Gmail.send_email({
  to: 'saracarmelina@gmail.com',
  subject: `Alerta semanal: Psicología Social LATAM – ${date}`,
  body: renderedPlainText,
  html_body: renderedHtml
})
```

Reglas importantes:

- No colocar HTML en `body`.
- El HTML debe ir únicamente en `html_body`.
- No usar JavaScript; Gmail lo bloquea.
- Mantener exactamente 2 artículos por edición.
- Priorizar el render en móvil: una sola columna, botones full-width, tarjetas compactas y síntesis en bloques apilados.

## Placeholders principales

### Generales

- `{{subject}}`
- `{{date}}`
- `{{review_range}}`
- `{{editorial_title}}`
- `{{editorial_subtitle}}`
- `{{editorial_summary}}`
- `{{coverage_note}}`

### Por artículo

Para cada artículo hay placeholders con prefijo `article_1_` y `article_2_`:

- `title`
- `subtitle`
- `quick_title`
- `quick_description`
- `context_label`
- `authors`
- `journal`
- `year`
- `link`
- `link_label`
- `pdf_url_or_note`
- `pdf_button`
- `abstract`
- `question`
- `method`
- `finding`
- `relevance`
- `selection_reason`
- `badge_1`
- `badge_2`
- `badge_3`

## PDF button

Si hay PDF libre, renderizar este bloque en `{{article_N_pdf_button}}`:

```html
<a class="button secondary" href="PDF_URL" style="display:block; width:100%; box-sizing:border-box; text-align:center; background:#3d3026; color:#fff7ec !important; text-decoration:none; font-size:15px; line-height:1.25; font-weight:700; border-radius:12px; padding:14px 14px; margin:9px 0 0 0;">Ver PDF</a>
```

Si no hay PDF libre confirmado, usar un string vacío para `{{article_N_pdf_button}}` y explicar la ausencia en `{{article_N_pdf_url_or_note}}` dentro del texto plano.
