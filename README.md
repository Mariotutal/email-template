# Email Templates

Repositorio para guardar plantillas HTML reutilizables para newsletters y correos editoriales.

## Estructura

```text
.
├── templates/
│   └── tech-radar-software-ai-homelab.html
├── prompts/
│   └── tech-radar-software-ai-homelab.md
├── examples/
│   └── tech-radar-body-fallback.txt
└── README.md
```

## Template incluido

### Tech Radar: Software, AI & Homelab

Newsletter técnico mobile-first para tendencias de:

- Frontend / JavaScript / TypeScript
- CSS, diseño UI, UX engineering y web platform
- Backend, arquitectura y bases de datos
- DevOps, CI/CD, observabilidad y platform engineering
- IA aplicada a desarrollo
- Homelab / self-hosting
- Repo Radar open source

## Buenas prácticas

- Mantener HTML compatible con clientes de correo.
- Usar CSS simple e inline cuando sea necesario.
- No usar JavaScript dentro del correo.
- Mantener una versión de texto plano como fallback.
- Evitar placeholders visibles antes de enviar.
