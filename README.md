# Aplucativo web de gestion de productos

# Aplicativo web de gestión de productos

**Desarrollado por:**
- Andrés Felipe Ramírez

Aplicativo web de gestión de productos de un restaurante, utilizando Full Stack MERN (React + Vite, Node.js + Express, MongoDB), diseñado para la gestión de productos y autenticación de usuarios con roles. Incluye:

- **Autenticación JWT** (login/registro) con recuperación de contraseña por correo.
- **Roles**: Administrador y usuario con layouts y rutas protegidas.
- **Órdenes** en panel administrativo.
- **CRUD de productos** con carga y vista previa de imágenes.
- **Interfaz responsiva** con TailwindCSS.

---

## 📂 Estructura del Proyecto

```
.
├── backend-mongodb/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── config/
│   └── server.js
│
└── frontend-auth/
    ├── src/
    │   ├── assets/
    │   ├── components/
    │   ├── context/
    │   ├── pages/
    │   ├── App.jsx
    │   └── main.jsx
```
---

## ⚙️ Instalación y Ejecución

1. **Clonar repositorio**
   ```bash
   git clone https://github.com/Andres2389/prueba_tecnica.git
   cd prueba_tecnica
   ```

### 2. Instalar dependencias del backend y frontend

```bash
npm install
```

### 3. Variables de entorno

### 📧 Configuración de envío de correos (Gmail)

Este proyecto utiliza **Gmail con clave de aplicación** para el envío de correos electrónicos (por ejemplo, confirmación de cuenta o recuperación de contraseña). Para que funcione correctamente:

1. Accede a tu cuenta de Gmail.
2. Activa la **verificación en dos pasos**.
3. Ve a [https://myaccount.google.com/apppasswords](https://myaccount.google.com/apppasswords).
4. Genera una nueva **clave de aplicación** (elige "Correo" y "Otro").
5. Copia la clave generada (16 caracteres) y úsala como valor de `EMAIL_APP_PASS`.

#### Backend (`backend-mongodb/.env`)

```env
PORT=5000
MONGO_URI=mongodb+srv://Andres2389:Andres2389@prueba.9ysbmii.mongodb.net/?retryWrites=true&w=majority&appName=prueba
JWT_SECRET=tu_clave_secreta
EMAIL_USER=tu_correo@gmail.com
EMAIL_APP_PASS=tu_contraseña_app
```

4. Abrir en el navegador `http://localhost:5173`

---

## 🚀 Características

- **Autenticación y roles**: Admin/User con rutas protegidas.
- **CRUD Usuarios y Productos**: con modales, validación y notificaciones.
- **Productos**: gestión completa desde dashboard.
- **Recuperación de contraseña**: envío de link, formulario de reseteo.
- **UI/UX**: responsive.
- **Feedback**: alertas con React Toastify y diálogos con SweetAlert2.

---

## 📋 API Endpoints Principales

### Autenticación
| Método | Ruta                          | Descripción                          |
|--------|-------------------------------|--------------------------------------|
| POST   | `/api/register`               | Registro de usuario                  |
| POST   | `/api/login`                  | Inicio de sesión                     |
| POST   | `/api/forgot-password`        | Solicitar link de recuperación       |
| POST   | `/api/reset-password/:token`  | Restablecer contraseña               |

### Usuarios (Admin)
| Método | Ruta                   | Descripción            |
|--------|------------------------|------------------------|
| GET    | `/api/users`           | Listar usuarios        |
| PUT    | `/api/users/:id`       | Actualizar usuario     |
| DELETE | `/api/users/:id`       | Eliminar usuario       |

### Productos (Admin)
| Método | Ruta                       | Descripción           |
|--------|----------------------------|-----------------------|
| GET    | `/api/productos`           | Listar productos      |
| POST   | `/api/productos`           | Crear producto        |
| PUT    | `/api/productos/:id`       | Editar producto       |
| DELETE | `/api/productos/:id`       | Eliminar producto     |

### Préstamos
| Método | Ruta                          | Descripción                     |
|--------|-------------------------------|---------------------------------|
| GET    | `/api/orders`              | Listar  (Admin)        |
| POST   | `/api/orders/:id`              | editar
---

## 📸 Capturas de Pantalla
![Home](./img/home.png)

---

![Admin Panel](./img/adminpanel.png)

---

![Admin Usuarios](./img/usuarios.png)

---

![Admin Productos](./img/productos.png)

---

![Admin Pedidos](./img/pedidos.png)

---

![Admin Pedidos modal](./img/pedidomodal.png)

---

![Admin user](./img/adminuser.png)

---
![User producto](./img/modal.png)

---

![User Carrito](./img/carrito.png)

---


