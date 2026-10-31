# 🔨 Ferretería Los Maestros

Plataforma web de comercio electrónico para una ferretería de La Serena y Coquimbo. Permite explorar el catálogo de productos, armar un carrito de compras con retiro en tienda o despacho a domicilio, consultar la zona de cobertura y administrar pedidos, usuarios y stock desde un panel de administración.

Proyecto académico desarrollado en equipo para la asignatura **Desarrollo Fullstack II (DSY1104)** de **Duoc UC**, construido en dos fases: primero con HTML, CSS y JavaScript puro, y luego migrado a **React**.

---

## 📁 Estructura del repositorio

```
Ferreteria-Los-Maestros/
├── Fase--1/   → Versión HTML5 + CSS3 + Bootstrap + JavaScript (Vanilla JS)
└── Fase--2/   → Versión React + Vite + React-Bootstrap (versión actual)
```

---

## ✨ Funcionalidades

| Módulo | Descripción |
|---|---|
| **Inicio** | Página principal con banner, categorías destacadas e información de la tienda. |
| **Catálogo** | Listado de productos con buscador y filtros por categoría (Construcción, Herramientas, Electricidad, Plomería, Pinturas, Jardinería) y por precio. |
| **Carrito de compras** | Agregar, modificar cantidades (1 a 10) y eliminar productos, cálculo del total en CLP, elección de retiro en tienda o despacho a domicilio y pago con crédito o cuenta corriente. |
| **Cobertura** | Zonas de despacho y mapa interactivo con la ubicación del local. |
| **Login y registro** | Creación de cuentas con validación de RUT chileno, correo y contraseña; sesión persistente. |
| **Mi cuenta** | Datos del cliente e historial de compras (ruta protegida para usuarios). |
| **Panel de administración** | Gestión de pedidos, usuarios, stock y ventas, con tablas adaptadas a celular (ruta protegida para administradores). |

Los datos (productos, usuarios, carrito y pedidos) se guardan en `localStorage`, que funciona como base de datos simulada.

---

## 🛠️ Tecnologías

**Fase 1**
- HTML5, CSS3, Bootstrap 5
- JavaScript (Vanilla JS)
- LocalStorage

**Fase 2**
- React 19 + Vite
- React Router (rutas públicas y protegidas)
- React-Bootstrap y Bootstrap Icons
- React Hook Form (validación de formularios)
- Context API (`AuthContext` y `CarritoContext`)
- Vitest + Testing Library (pruebas unitarias)
- Oxlint

---

## 🚀 Cómo ejecutar el proyecto

### Fase 1 (HTML)
No necesita instalación: basta con abrir `Fase--1/index.html` en el navegador (o usar la extensión **Live Server** de VS Code).

### Fase 2 (React)
Requisitos: **Node.js 20 o superior**.

```bash
cd Fase--2
npm install
npm run dev
```

Luego abre `http://localhost:5173` en el navegador.

Otros comandos disponibles:

```bash
npm run build     # Genera la versión de producción en /dist
npm run preview   # Sirve localmente la versión de producción
npm test          # Ejecuta las pruebas unitarias con Vitest
npm run lint      # Revisa el código con Oxlint
```

### 🔑 Usuario administrador de prueba

| Correo | Contraseña |
|---|---|
| `admin@losmaestros.cl` | `admin123` |

---

## 🧪 Pruebas unitarias

La Fase 2 incluye pruebas con **Vitest** sobre:
- Lógica del carrito (agregar, cambiar cantidades, total y registro de compra)
- Filtros del catálogo
- Formato de precios en pesos chilenos
- Renderizado de la página de Cobertura y de la aplicación

```bash
cd Fase--2
npm test
```

---

## 👤 Autor

**Kevin González**: Analista Programador, Duoc UC
GitHub: [@KevinYulianG](https://github.com/KevinYulianG)

Mis aportes principales al proyecto fueron el **carrito de compras** y la **página de cobertura** en ambas fases, las pruebas unitarias del carrito y los ajustes de diseño responsive para celular.

> Proyecto académico sin fines comerciales. Los productos, precios y datos de la tienda son ficticios.
