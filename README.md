# 🛍️ Vue Router Shopping Demo

![Vue.js](https://img.shields.io/badge/Vue.js-4FC08D?style=for-the-badge&logo=vue.js&logoColor=white)
![Vue Router](https://img.shields.io/badge/Vue_Router-4FC08D?style=for-the-badge&logo=vue.js&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white)

## 📝 Descripción

Este proyecto es una demostración de una tienda en línea implementada con Vue.js y Vue Router. Incluye navegación entre diferentes vistas, gestión de productos y un formulario de contacto.

[Vista previa del proyecto](https://desafio-vue-router-seven.vercel.app/)

## ✨ Características

- 🔄 Navegación fluida entre páginas usando Vue Router
- 🏷️ Sistema de productos con props dinámicas
- 📱 Diseño responsive con Bootstrap
- 💅 Componentes reutilizables
- 🚀 Lazy loading para mejor rendimiento

## 🛠️ Tecnologías Utilizadas

- Vue.js 3
- Vue Router 4
- Bootstrap 5
- HTML5
- CSS3
- JavaScript

## 📋 Prerrequisitos

Antes de comenzar, asegúrate de tener instalado:

- Node.js (versión 14 o superior)
- npm (normalmente viene con Node.js)

## 🚀 Instalación

1. Clona el repositorio:

```bash
git clone https://github.com/FideoKojima/DesafioVueRouter.git
```

2. Navega al directorio del proyecto:

```bash
cd DesafioRouterVue
```

3. Instala las dependencias:

```bash
npm install
```

4. Inicia el servidor de desarrollo:

```bash
npm run dev
```

## 📁 Estructura del Proyecto

```
vue-router-shop/
├── src/
│   ├── components/
│   │   ├── Card.vue
│   │   ├── Footer.vue
│   │   ├── MediosPago.vue
│   │   └── Navbar.vue
│   ├── views/
│   │   ├── Home.vue
│   │   ├── Productos.vue
│   │   └── Contacto.vue
│   ├── router/
│   │   └── index.js
│   ├── App.vue
│   └── main.js
├── public/
├── package.json
└── README.md
```

## 🖥️ Vistas Disponibles

### 🏠 Home

- Página principal
- Muestra productos destacados
- Incluye medios de pago y footer

### 🛍️ Productos

- Listado de productos
- Detalles de cada producto
- Precios y disponibilidad

### 📞 Contacto

- Formulario de contacto
- Información de la empresa
- Botón de retorno al inicio

## ⚙️ Configuración de Rutas

Las rutas están configuradas en `src/router/index.js`:

```javascript
const routes = [
  {
    path: "/",
    name: "Home",
    component: () => import("../views/Home.vue"),
  },
  {
    path: "/productos",
    name: "Productos",
    component: () => import("../views/Productos.vue"),
  },
  {
    path: "/contacto",
    name: "Contacto",
    component: () => import("../views/Contacto.vue"),
  },
];
```

## 🎯 Props en Vista Productos

La vista de productos recibe las siguientes props:

| Prop        | Tipo   | Descripción           |
| ----------- | ------ | --------------------- |
| nombre      | String | Nombre del producto   |
| descripcion | String | Descripción detallada |
| precio      | Number | Precio en dólares     |
| cantidad    | Number | Stock disponible      |

## 🤝 Contribuir

1. Fork el proyecto
2. Crea una nueva rama (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 👥 Autores

- **Luis Suarez** - _Trabajo Inicial_ - [Fideo Kojima](https://github.com/FideoKojima)

## 🎉 Agradecimientos

- Desafío Latam por proporcionar el código base
- Comunidad Vue.js
- Todos los contribuidores que participan en este proyecto

---

⌨️ con ❤️ por [Luis Suarez](https://github.com/FideoKojima) 😊
