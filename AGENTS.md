# AGENTS.md — Guía para agentes de desarrollo

## Contexto del proyecto

Landing page personal para **Nieves Muriel García**, escritora, poeta, investigadora y profesora en la Universidad de Málaga. El sitio debe transmitir elegancia literaria, seriedad académica y calidez personal.

## Directrices de diseño

### Estética

- **Tono visual**: Editorial literario, refinado y femenino sin ser cursi. Inspiración en revistas literarias europeas y portadas de editoriales independientes.
- **Ambiente**: Sobrio, culto, acogedor. Como entrar en una librería bien iluminada.
- **NO hacer**: Diseños corporativos fríos, estética tech/startup, colores chillones, animaciones excesivas.

### Paleta de colores (OBLIGATORIA)

```css
:root {
  --color-primary: #0D7377;        /* Turquesa oscuro — enlaces, acentos principales */
  --color-primary-light: #14A3A8;  /* Turquesa medio — hover states */
  --color-accent: #7FDBDA;         /* Turquesa claro — detalles decorativos, bordes suaves */
  --color-bg: #FAFAF8;             /* Fondo principal — blanco cálido */
  --color-bg-alt: #E8F6F6;         /* Fondo alternativo — secciones alternas */
  --color-text: #2D3436;           /* Texto principal */
  --color-text-secondary: #636E72; /* Texto secundario, descripciones */
  --color-border: #B2DFDB;         /* Bordes y separadores suaves */
}
```

### Tipografía

- **Títulos (h1, h2, h3)**: `'Playfair Display', Georgia, serif` — Elegante, literaria
- **Cuerpo**: `'Source Sans 3', 'Segoe UI', sans-serif` — Limpia, legible
- **Citas o destacados**: Playfair Display en itálica

### Layout

- Single page con scroll suave entre secciones
- Ancho máximo de contenido: `900px`
- Espaciado generoso (mínimo `2rem` entre secciones)
- Mobile-first responsive design
- Navegación fija sutil en la parte superior

## Estructura de secciones

### 1. Header / Navegación
- Logo o nombre "Nieves Muriel García" en tipografía Playfair
- Menú: Sobre mí | Libros | Editoriales | Colaboraciones
- Fondo transparente que se opacifica al hacer scroll

### 2. Hero — Sobre ella
- Layout: Foto a la izquierda (circular o con bordes suaves), texto a la derecha
- En móvil: Foto arriba centrada, texto debajo
- Contenido de la bio (ver README.md para datos completos):
  - Nombre completo
  - Lugar y año de nacimiento: Melilla, 1977
  - Formación: Doctora por la UGR, Licenciada en Filología Hispánica, Máster en Estudios de la Diferencia Sexual (UB)
  - Posición actual: Profesora en la Universidad de Málaga
  - Especialidad: Escritura femenina y poesía española contemporánea
  - Premios destacados: Beca Miguel Fernández (2013), Premio María Telo (2016), II Premio Juana Castro
- Foto: usar placeholder SVG hasta que se proporcione la imagen real (`assets/img/foto-nieves.jpg`)

### 3. Libros publicados
- Tarjetas o lista estilizada con:
  - Título del libro (enlazado si hay URL)
  - Año de publicación
  - Editorial
  - Breve descripción o tipo (poesía, ensayo, investigación)
  - Premios asociados si los tiene
- Orden cronológico inverso (más reciente primero)
- Libros a incluir (consultar README.md para lista completa):
  1. A mi querido Abdelaziz... de tu Conchita (2023, Icaria)
  2. Solo lo cierto cuenta (2022, Sabina Editorial)
  3. Esta flor secreta (2020, Sabina Editorial)
  4. Madrid (2019, Sabina Editorial)
  5. Carta de la sirena (2016, Editorial Renacimiento)
  6. La pequeña llama (2013)
  7. La luz de las palabras (2013, UNED)

### 4. Editoriales
- Enlaces con icono o logo estilizado a:
  - Editorial Renacimiento
  - Icaria Editorial
  - Sabina Editorial
  - Todos tus libros (perfil de autora)
- Cada enlace debe abrirse en nueva pestaña (`target="_blank"`)

### 5. Colaboraciones y enlaces
- Enlaces a perfiles académicos e institucionales:
  - Universidad de Málaga (ficha docente)
  - Portal de Investigación UMA
  - Dialnet
  - Tesis doctoral en repositorio UGR
- Formato similar a la sección de editoriales

### 6. Footer
- Nombre y copyright
- Año actual
- Opcionalmente enlace de contacto (email)

## Reglas técnicas

### HTML
- Semántico: usar `<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`
- Cada sección con `id` correspondiente para navegación con anclas
- Atributos `alt` descriptivos en imágenes
- `lang="es"` en el `<html>`

### CSS
- Variables CSS para todos los colores y fuentes
- Media queries para responsive (breakpoint principal: `768px`)
- Sin frameworks CSS — CSS puro/vanilla
- Transiciones suaves en hover (0.3s ease)
- Scroll behavior: smooth

### JavaScript (mínimo)
- Solo para: scroll suave si no se usa CSS, y opacidad del header al scroll
- NO usar jQuery ni frameworks JS
- Vanilla JS únicamente

### Accesibilidad
- Contraste suficiente (ratio mínimo 4.5:1)
- Navegación por teclado funcional
- Textos alternativos en imágenes
- Jerarquía correcta de headings (h1 > h2 > h3)

### Rendimiento
- Google Fonts con `display=swap`
- Imágenes optimizadas
- Sin dependencias externas innecesarias
- Carga rápida: objetivo < 1s en first paint

## Archivos esperados

```
nieves-muriel-landing/
├── README.md
├── AGENTS.md
├── index.html
└── assets/
    ├── css/
    │   └── styles.css
    └── img/
        └── placeholder.svg
```

## Notas importantes

- La foto de perfil NO está disponible aún. Usar un placeholder SVG elegante con las iniciales "NM" en turquesa.
- Todos los datos biográficos y bibliográficos han sido verificados con fuentes públicas.
- El sitio debe funcionar perfectamente sin JavaScript habilitado (progressive enhancement).
- Priorizar legibilidad y elegancia sobre efectos visuales complejos.
