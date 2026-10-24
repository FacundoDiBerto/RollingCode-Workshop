# Rolling Code Workshop

Landing page del workshop **"¿Por dónde empiezo a programar?"** de Rolling Code School. Página de una sola vista con información del evento, speakers, agenda, ubicación, venta de entradas y sponsors.

## Stack

- **HTML5** — estructura semántica
- **CSS3** — estilos propios en `css/styles.css`, sobre variables (`:root`) con la paleta de marca
- **Bootstrap 5.3** — grilla, componentes (navbar, carrusel, modal) y utilidades responsive, cargado por CDN
- **Google Fonts** — tipografía Plus Jakarta Sans

Sin frameworks de build ni JavaScript propio: todo lo interactivo (menú colapsable, carrusel de speakers, modal de pago) usa los componentes de Bootstrap vía atributos `data-bs-*`.

## Estructura del proyecto

```
RollingCode-Workshop/
├── index.html              # página principal
├── pages/
│   └── error404.html       # página de error 404
├── css/
│   └── styles.css          # estilos del sitio
├── assets/
│   ├── logo/                # logo en blanco y negro
│   ├── iconos/               # íconos SVG (ubicación, redes, etc.)
│   ├── speakers/              # fotos de los 10 speakers
│   └── img/                  # imágenes de la página 404
└── README.md
```

## Cómo verlo localmente

No necesita instalación. Dos opciones:

1. Abrir `index.html` directo en el navegador.
2. Con la extensión **Live Server** de VS Code, clic derecho sobre `index.html` → "Open with Live Server" (recomendado, para que las rutas relativas de `pages/error404.html` se resuelvan igual que en producción).

## Paleta de colores

| Color | Hex | Uso |
|---|---|---|
| Rojo Rolling | `#e0202a` | Botones, etiquetas, acentos |
| Negro página | `#0b0b0c` | Fondo general |
| Superficie | `#111113` | Tarjetas |
| Blanco | `#ffffff` | Títulos, texto principal |

## Flujo de trabajo del equipo

- **Ramas**: `feature/hu-XXX/nombre-corto`, una por cada tarjeta de HU (historia de usuario). Siempre se crean desde `dev` actualizado.
- **Commits**: convención de prefijos —
  - `feat:` función nueva
  - `fix:` corrección de un bug
  - `style:` cambios de estilo/formato que no afectan la lógica
- **Pull Requests**: `base: dev` ← `compare: feature/...`, con descripción de qué se hizo y qué criterios de aceptación cubre. Se revisan antes de mergear.
- `dev` concentra el trabajo integrado del equipo; `main` queda para versiones estables.

