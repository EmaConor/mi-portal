[Read in English](README.md)

# InnovateStart

Un portal web de una sola pagina (SPA) para un ecosistema de emprendimiento e innovacion. Construido con HTML5, CSS3 y JavaScript vanilla, este proyecto funciona como un sitio informativo para un programa acelerador de startups llamado InnovateStart.

---

## Caracteristicas

- **Aplicacion de una sola pagina (SPA)** — El enrutamiento basado en hash carga el contenido de cada pagina de forma dinamica, sin recargar completamente el navegador. La navegacion se siente fluida y rapida.
- **5 paginas tematicas:**
  - **Inicio** — Banner principal, tarjetas de servicios (mentorias, networking, financiamiento, capacitacion, asesoria legal, marketing digital) y seccion de estadisticas.
  - **Informacion** — Explicacion detallada de las metodologias Lean Startup, Design Thinking y Agile Scaling.
  - **Galeria** — Galeria de imagenes con descripciones y un video de YouTube incrustado.
  - **Tabla de precios** — Tabla comparativa con cuatro planes: Basico (gratuito), Pro ($49), Empresa ($199) y Premium ($499).
  - **Contacto** — Formulario de contacto validado con retroalimentacion en tiempo real y contador de caracteres.
- **Componentes reutilizables** — El encabezado (barra de navegacion) y el pie de pagina se cargan dinamicamente desde archivos HTML separados mediante JavaScript.
- **Diseno responsive** — CSS personalizado con tres puntos de quiebre que garantiza su correcta visualizacion en moviles, tablets y escritorio.
- **Validacion de formularios en el cliente** — Validacion en tiempo real con retroalimentacion visual (clase `is-invalid` de Bootstrap) y una alerta de exito al enviar.
- **Accesibilidad** — Elementos semanticos de HTML5 (`<section>`, `<article>`, `<aside>`, `<figure>`, `<figcaption>`), atributos `aria-label` y texto oculto visualmente para lectores de pantalla.

---

## Tecnologias utilizadas

| Tecnologia | Proposito |
|---|---|
| **HTML5** | Estructura semantica de las paginas |
| **CSS3** | Estilos personalizados, animaciones, diseno responsive |
| **JavaScript (ES6+)** | Enrutamiento SPA, carga dinamica de componentes, validacion de formularios |
| **Bootstrap 5.3** | Componentes de interfaz, sistema de grillas, clases utilitarias (cargado via CDN) |
| **Font Awesome 6.4** | Iconos (cargado via CDN) |

---

## Estructura del proyecto

```
innovate-start/
├── components/
│   ├── header.html          # Barra de navegacion compartida
│   └── footer.html          # Pie de pagina compartido con enlaces y copyright
├── css/
│   └── style.css            # Estilos personalizados (variables, tipografia, responsive)
├── img/                     # Imagenes del sitio
│   ├── 1.png
│   ├── 2.jpg
│   ├── 3.webp
│   ├── 4.jpg
│   ├── 5.png
│   └── 6.jpg
├── js/
│   ├── script.js            # Enrutador SPA, validacion de formularios, actualizacion de titulos
│   └── components.js        # Carga dinamica del encabezado y pie de pagina
├── pages/
│   ├── home.html            # Contenido de la pagina de inicio
│   ├── informacion.html     # Pagina de informacion de metodologias
│   ├── galeria.html         # Pagina de galeria de imagenes
│   ├── tabla.html           # Pagina de tabla comparativa de precios
│   └── contacto.html        # Pagina de formulario de contacto
├── index.html               # Punto de entrada principal (shell SPA)
├── README.md                # Documentacion en ingles (principal)
└── README.es.md             # Esta documentacion en espanol
```

---

## Como empezar

### Requisitos previos

Necesitas un servidor HTTP local para ejecutar este proyecto. La API `fetch()` de JavaScript no funciona con el protocolo `file://`, por lo que abrir `index.html` directamente en el navegador no cargara el contenido correctamente.

### Instalacion

1. **Clona el repositorio:**

   ```bash
   git clone https://github.com/EmaConor/-mi-portal.git
   cd -mi-portal
   ```

2. **Inicia un servidor local** usando uno de estos metodos:

   **Opcion A — Python (recomendada):**

   ```bash
   python -m http.server 8000
   ```

   **Opcion B — Live Server de VS Code:**

   Instala la extension "Live Server", haz clic derecho en `index.html` y selecciona "Open with Live Server".

   **Opcion C — Node.js (npx):**

   ```bash
   npx serve .
   ```

3. **Abre en tu navegador:**

   ```
   http://localhost:8000
   ```

---

## Uso

### Navegacion

La aplicacion utiliza enrutamiento basado en hash (ejemplo: `http://localhost:8000/#/informacion`). Haz clic en cualquier enlace de navegacion del encabezado para cambiar de pagina sin recargar completamente el sitio.

### Rutas

| Ruta hash | Pagina |
|---|---|
| `#/` | Inicio |
| `#/informacion` | Informacion |
| `#/galeria` | Galeria |
| `#/tabla` | Precios |
| `#/contacto` | Contacto |

### Formulario de contacto

Completa los campos obligatorios (nombre, correo electronico, interes, mensaje y aceptacion de terminos). El formulario valida los datos en tiempo real. Al enviarlo correctamente, aparecera una alerta verde confirmando el envio del mensaje.


