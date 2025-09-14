# 🍕 Pizza Universitaria - Sistema de Pedidos Online

![React](https://img.shields.io/badge/React-18-blue?logo=react)
![TypeScript](https://img.shields.io/badge/TypeScript-5-blue?logo=typescript)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-3-blue?logo=tailwindcss)
![Vite](https://img.shields.io/badge/Vite-5-purple?logo=vite)
![License](https://img.shields.io/badge/License-MIT-green)

Sistema completo de pedidos de pizza en línea diseñado específicamente para el **Centro Universitario de los Altos (CUAltos)** en Tepatitlán de Morelos, Jalisco.

## 📋 Descripción

Pizza Universitaria es una plataforma web moderna que permite a estudiantes, profesores y personal del campus realizar pedidos de pizza con entrega directa en el campus universitario. El sistema incluye personalización de pizzas, seguimiento en tiempo real y un dashboard para el personal de cocina.

## 🚀 Características Principales

- **🛒 Catálogo de Productos**: Pizzas tradicionales, gourmet y bebidas
- **🎨 Personalización Avanzada**: 3 tamaños, 4 tipos de masa y 15 ingredientes adicionales
- **🛍️ Carrito Inteligente**: Gestión de pedidos con cálculos automáticos
- **📍 Validación Geográfica**: Entrega exclusiva en el campus CUAltos
- **📱 Diseño Responsivo**: Optimizado para móvil, tablet y desktop
- **📊 Seguimiento en Tiempo Real**: Estados del pedido actualizados automáticamente
- **👨‍🍳 Dashboard de Cocina**: Interface para gestión de pedidos del personal
- **🎯 Área de Servicio Específica**: Validación de direcciones del campus

## 🛠️ Tecnologías Utilizadas

- **Frontend**: React 18 + TypeScript
- **Styling**: Tailwind CSS + Shadcn-ui
- **Icons**: Lucide React
- **Build Tool**: Vite
- **Package Manager**: pnpm/npm/yarn
- **Notifications**: Sonner

## 📋 Prerrequisitos Detallados

### Node.js (Requerido)
- **Versión mínima**: Node.js 16.x
- **Versión recomendada**: Node.js 18.x o superior

#### Instalación de Node.js:

**Ubuntu/Debian:**
```bash
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt-get install -y nodejs
```

**Arch Linux:**
```bash
sudo pacman -S nodejs npm
```

**macOS:**
```bash
brew install node
```

**Windows:**
Descargar desde [nodejs.org](https://nodejs.org/)

#### Verificar instalación:
```bash
node --version  # Debe mostrar v16+ o superior
npm --version   # Debe mostrar 8+ o superior
```

### Package Managers (Opcional pero recomendado)

#### pnpm (Recomendado - más rápido):
```bash
npm install -g pnpm
pnpm --version
```

#### Yarn (Alternativa):
```bash
npm install -g yarn
yarn --version
```

## 📦 Instalación Paso a Paso

### 1. Clonar el Repositorio
```bash
git clone https://github.com/[TU-USUARIO]/proyecto-pizza.git
cd proyecto-pizza
```

### 2. Instalar Dependencias

**Con pnpm (Recomendado):**
```bash
pnpm install
```

**Con npm:**
```bash
npm install
```

**Con yarn:**
```bash
yarn install
```

### 3. Iniciar el Servidor de Desarrollo

**Con pnpm:**
```bash
pnpm run dev
```

**Con npm:**
```bash
npm run dev
```

**Con yarn:**
```bash
yarn dev
```

### 4. Abrir en el Navegador
- **URL Local**: http://localhost:5173
- **URL de Red**: Se mostrará en la terminal

## 🚀 Scripts Disponibles

| Script | Comando | Descripción |
|--------|---------|-------------|
| **Desarrollo** | `pnpm run dev` | Inicia servidor de desarrollo en puerto 5173 |
| **Build** | `pnpm run build` | Construye la aplicación para producción |
| **Preview** | `pnpm run preview` | Previsualiza la build de producción |
| **Lint** | `pnpm run lint` | Ejecuta ESLint para verificar código |

## 📁 Estructura del Proyecto

```
proyecto-pizza/                       # Raíz del repositorio
├── src/
│   ├── components/
│   │   ├── ui/                       # Componentes base de Shadcn-ui
│   │   ├── PizzaCustomizer.tsx
│   │   ├── OrderTracking.tsx
│   │   └── KitchenDashboard.tsx
│   ├── pages/
│   │   └── Index.tsx                 # Página principal
│   ├── services/
│   │   └── ApiService.ts             # Simulación de API
│   ├── utils/
│   │   └── geolocation.ts            # Validación de área
│   └── lib/
│       └── utils.ts                  # Utilidades
├── public/
│   └── api/
│       ├── products.json             # Catálogo de productos
│       └── orders.json               # Pedidos de ejemplo
├── package.json                      # Dependencias del proyecto
├── vite.config.ts                    # Configuración de Vite
├── tailwind.config.js                # Configuración de Tailwind
├── README.md                         # Este archivo
├── CONTRIBUTING.md                   # Guía de contribución
└── .gitignore                        # Archivos excluidos
```

## 🔧 Desarrollo y Personalización

### Modificar Productos
Editar `public/api/products.json`:
```json
{
  "id": "12",
  "name": "Pizza Nueva",
  "description": "Descripción de la pizza",
  "price": 150,
  "category": "Traditional",
  "image": "🍕"
}
```

### Personalizar Área de Servicio
Editar `src/utils/geolocation.ts`:
```typescript
const VALID_KEYWORDS = [
  'cualtos',
  'nuevo-edificio',  // Agregar nuevos edificios
  // ...
];
```

### Cambiar Estilos
Los estilos principales están en:
- `src/index.css` - Estilos globales
- Componentes individuales usan Tailwind CSS

## 🌐 Build de Producción

### Construir la Aplicación
```bash
pnpm run build
```

### Archivos Generados
- **Directorio**: `dist/`
- **Tamaño del Bundle**: ~438 kB
- **CSS**: ~67 kB

### Desplegar en Netlify/Vercel
1. Ejecutar `pnpm run build`
2. Subir la carpeta `dist/`
3. Configurar el directorio de build como `dist`

## 🎯 Funcionalidades por Pestaña

### 🍕 Menú
- Catálogo organizado por categorías (Tradicionales, Gourmet, Bebidas)
- Precios dinámicos según personalización
- Botones de agregar al carrito y personalizar

### 🛒 Carrito
- Resumen detallado de pedidos con personalizaciones
- Modificación de cantidades (+/-)
- Proceso de checkout con validación de dirección
- Cálculo automático de totales

### 📍 Seguimiento
- Estados en tiempo real del pedido
- Información del cliente y dirección
- Tiempo estimado de entrega

### 👨‍🍳 Cocina (Staff)
- Lista de pedidos activos con prioridades
- Actualización de estados (Confirmado → Preparando → Horneando → Listo → Entregado)
- Indicadores visuales de urgencia

## 🎨 Personalización Visual

El proyecto utiliza un esquema de colores optimizado para la industria alimentaria:
- **Primario**: Red-600 (#DC2626)
- **Secundario**: Orange-600 (#EA580C)
- **Acentos**: Gradientes complementarios
- **Neutral**: Gray-50 a Gray-900

## 🐛 Solución de Problemas (Troubleshooting)

### Error: "vite: command not found"
```bash
# Instalar dependencias primero
pnpm install
# Luego ejecutar
pnpm run dev
```

### Error: "Could not read package.json"
```bash
# Asegúrate de estar en el directorio raíz del proyecto
ls  # Debe mostrar package.json en la raíz
pwd # Debe mostrar el directorio proyecto-pizza
```

### Error de red durante instalación
```bash
# Limpiar caché de npm
npm cache clean --force
# O usar yarn/pnpm como alternativa
yarn install
```

### Puerto 5173 ocupado
```bash
# Vite automáticamente usará el siguiente puerto disponible
# O especificar un puerto manualmente:
pnpm run dev -- --port 3000
```

### Problemas con dependencias
```bash
# Eliminar node_modules y reinstalar
rm -rf node_modules package-lock.json
pnpm install
```

### Error: "66 archivos nuevos después de npm install"
```bash
# Esto es normal - node_modules/ está en .gitignore
# Solo se subirán los archivos de código fuente
git status  # Verificar que node_modules/ no aparece
```

## 📊 Métricas del Proyecto

- **Bundle Size**: 438.33 kB (comprimido: 136.13 kB)
- **CSS Size**: 66.73 kB (comprimido: 11.45 kB)
- **Componentes**: 4 componentes principales + UI library
- **Productos**: 11 productos (8 pizzas + 3 bebidas)
- **Ingredientes**: 15 opciones de personalización
- **Tiempo de Build**: ~5-6 segundos

## 🎯 Área de Servicio

El sistema está configurado para entregar únicamente en:
- **Campus**: Centro Universitario de los Altos
- **Ciudad**: Tepatitlán de Morelos, Jalisco
- **Edificios**: A, B, C, D, E, F, G, H
- **Áreas**: Biblioteca, Cafetería, Rectoría, Laboratorios

## 📞 Información de Contacto

- **Teléfono**: 378-782-8000
- **Horario**: 08:00 - 20:00
- **Área de Servicio**: Solo Campus CUAltos

## 🤝 Contribuciones

¿Quieres contribuir al proyecto? ¡Genial! Lee nuestra [Guía de Contribución](CONTRIBUTING.md) para comenzar.

## 📄 Licencia

Este proyecto está bajo la Licencia MIT. Ver el archivo `LICENSE` para más detalles.

---

**Desarrollado con ❤️ para la comunidad universitaria de CUAltos**

### 🚀 Enlaces Útiles
- [Documentación de React](https://react.dev/)
- [Documentación de Vite](https://vitejs.dev/)
- [Documentación de Tailwind CSS](https://tailwindcss.com/)
- [Shadcn-ui Components](https://ui.shadcn.com/)