# 🎬 AluraFlix

Una aplicación web desarrollada con React que permite gestionar y visualizar una colección de videos educativos organizados por categorías. Este proyecto fue creado como parte del Challenge React de Alura.

## 📋 Características

- ✨ Interfaz moderna y responsive
- 📺 Reproducción de videos de YouTube
- 🎯 Organización por categorías
- ✏️ CRUD completo de videos
- 💾 Persistencia de datos en localStorage
- 🌙 Tema oscuro moderno

## 🛠️ Tecnologías Utilizadas

- React 18
- Vite
- Tailwind CSS
- Lucide React (iconos)

## 📁 Estructura del Proyecto

```
aluraflix/
├── src/
│   ├── assets/
│   │   └── images/
│   │       └── banner.jpg
│   ├── components/
│   │   ├── Header.jsx
│   │   ├── VideoCard.jsx
│   │   └── FormularioVideo.jsx
│   ├── styles/
│   │   └── index.css
│   ├── App.jsx
│   └── main.jsx
├── public/
│   └── index.html
├── package.json
├── tailwind.config.js
├── postcss.config.js
├── vite.config.js
└── README.md
```

## ⚙️ Requisitos Previos

- Node.js (versión 14 o superior)
- npm o yarn

## 🚀 Instalación

1. **Clonar el repositorio**
```bash
git clone https://github.com/jotaid/AluraFlixJoseIdrobo.git
cd aluraflix
```

2. **Instalar dependencias**
```bash
npm install
```

3. **Instalar dependencias específicas**
```bash
# Instalar Tailwind CSS y sus dependencias
npm install -D tailwindcss postcss autoprefixer

# Instalar Lucide React para los iconos
npm install lucide-react
```

4. **Configurar Tailwind CSS**
```bash
# Generar archivos de configuración
npx tailwindcss init -p
```

5. **Configurar el archivo `tailwind.config.js`**
```javascript
/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {
      colors: {
        background: {
          primary: '#0A0C10',
          secondary: '#161B22',
          tertiary: '#21262D',
          input: '#2D333B',
        }
      }
    },
  },
  plugins: [],
}
```

6. **Configurar el archivo `src/styles/index.css`**
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

## 🖥️ Ejecutar la Aplicación

```bash
# Iniciar en modo desarrollo
npm run dev

# Construir para producción
npm run build

# Previsualizar la versión de producción
npm run preview
```

## 📱 Uso

1. **Agregar un nuevo video**
   - Clic en el botón "Nuevo Video"
   - Completar el formulario con:
     - Título
     - Categoría
     - URL de la imagen
     - URL del video (YouTube)
     - Descripción

2. **Editar un video**
   - Clic en el ícono de edición en la tarjeta del video
   - Modificar los campos deseados
   - Guardar cambios

3. **Eliminar un video**
   - Clic en el ícono de eliminar en la tarjeta del video
   - Confirmar la eliminación

4. **Reproducir un video**
   - Clic en la tarjeta del video
   - El video se reproducirá en un modal

## 🎨 Personalización

### Colores
Los colores principales están definidos en el objeto `THEME` en `App.jsx`:
```javascript
const THEME = {
  background: {
    primary: 'bg-[#0A0C10]',    // Fondo principal
    secondary: 'bg-[#161B22]',   // Header y footer
    tertiary: 'bg-[#21262D]',    // Cards
    input: 'bg-[#2D333B]',       // Inputs
  },
  // ... más configuraciones
};
```

### Categorías
Las categorías se pueden modificar en el array `categoriasIniciales`:
```javascript
const categoriasIniciales = [
  { id: 1, nombre: 'Front End', color: 'bg-violet-600' },
  { id: 2, nombre: 'Back End', color: 'bg-cyan-600' },
  { id: 3, nombre: 'Innovación y Gestión', color: 'bg-rose-600' }
];
```

## 📄 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE.md](LICENSE.md) para más detalles.

## ✨ Contribuir

1. Fork del repositorio
2. Crear una rama para tu característica (`git checkout -b feature/AmazingFeature`)
3. Commit de tus cambios (`git commit -m 'Add: Amazing Feature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abrir un Pull Request

## 👥 Autores

* **Tu Nombre** - *Desarrollo Inicial* - [TuUsuario](https://github.com/jotaid)

## 🎯 Próximas Mejoras

- [ ] Implementar sistema de autenticación
- [ ] Agregar búsqueda de videos
- [ ] Permitir ordenar videos por diferentes criterios
- [ ] Agregar más opciones de personalización
- [ ] Implementar sistema de favoritos

## 🙌 Agradecimientos

* Alura Latam por el challenge
* La comunidad de React por su documentación y recursos
* A todos los que contribuyen al proyecto
