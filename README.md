# Responsive Dropdown Menu

Un proyecto frontend que implementa un menú de navegación responsivo y desplegable (dropdown) construido con HTML5, CSS3 y Vanilla JavaScript. El diseño incluye un menú de múltiples niveles que se adapta perfectamente tanto a pantallas de escritorio como a dispositivos móviles.

## 🚀 Características

- **Diseño Responsivo**: Cambia fluidamente entre una barra de navegación completa en escritorio y un menú de hamburguesa interactivo en dispositivos móviles (punto de quiebre a los `800px`).
- **Submenús Anidados**: Soporte para subítems dentro del menú principal, revelados mediante clics en móvil y hover (o interacciones ajustadas) en escritorio.
- **Transiciones y Animaciones Suaves**: Uso de `clip-path` y transiciones CSS para mostrar/ocultar los submenús y rotar las flechas indicadoras de manera fluida.
- **Vanilla JavaScript**: Lógica ligera sin dependencias externas para manejar los eventos de clic, recalcular la altura de los submenús dinámicamente y resetear los estilos al redimensionar la ventana.
- **Tipografía Moderna**: Integración con Google Fonts utilizando la familia tipográfica "Poppins".

## 🛠️ Tecnologías Utilizadas

- **HTML5**: Estructura semántica utilizando etiquetas como `<nav>`, `<section>` y listas `<ul>` / `<li>`.
- **CSS3**:
  - Flexbox & Grid para la disposición de elementos.
  - Variables CSS (Custom Properties) para animaciones (`--clip`, `--transform`).
  - Media queries para la adaptabilidad (Mobile/Tablet/Desktop).
- **JavaScript (ES6+)**:
  - Manipulación del DOM.
  - Listeners de eventos (`click`, `resize`).
  - Cálculo dinámico de dimensiones (`scrollHeight`, `clientHeight`).

## 📂 Estructura del Proyecto

```text
menu-responsivo/
├── assets/             # Contiene íconos SVG (hamburguesa, flecha)
├── css/
│   └── estilos.css     # Hoja de estilos principal
├── js/
│   └── app.js          # Lógica de interacciones y responsividad del menú
└── index.html          # Estructura principal de la página
```

## 🧠 Solución Técnica Detallada

El menú resuelve el desafío común de mostrar submenús tanto en interfaces de escritorio como móviles:

1. **En escritorio (> 800px):** Los submenús se revelan flotando sobre el contenido (`position: absolute`) usando `clip-path` y `transform`, evitando saltos bruscos en el diseño.
2. **En móviles (<= 800px):** El menú cambia a una posición fija lateral y utiliza el paradigma del acordeón. JavaScript se encarga de calcular exactamente el alto de los submenús anidados usando `scrollHeight` y aplica esa altura para lograr un despliegue con transición, ya que en CSS nativo transicionar desde `height: 0` a `height: auto` no genera animaciones fluidas.

Adicionalmente, el evento `resize` está controlado en JavaScript para asegurar que los estilos directos agregados para la versión móvil (como la altura forzada de un submenú) se limpien si el usuario agranda la pantalla de vuelta al tamaño de escritorio, evitando "bugs" visuales.

## ⚙️ Instalación y Uso

Este es un proyecto estático, por lo que no requiere de la instalación de paquetes o servidores especiales:

1. Clona este repositorio o descarga los archivos.
2. Abre el archivo `index.html` en tu navegador web de preferencia.
3. ¡Listo! Inspecciona la página o redimensiona tu ventana para ver la versión responsiva en acción.

---

Desarrollado por **SergioDevWeb**.
