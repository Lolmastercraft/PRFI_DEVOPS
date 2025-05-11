# 🎶 Proyecto de Vinilos Clásicos

Este proyecto es una tienda en línea para discos de vinilo, desarrollada con **Flask** y **DynamoDB** para el backend, y HTML/CSS/JS para el frontend.

---

## 📂 Estructura del Proyecto

```
proyecto/
├── backend/
│   ├── app.py                # Servidor Flask
│   ├── models.py             # Operaciones DynamoDB
│   ├── routes.py             # Rutas del API
│   ├── .env                  # Variables de entorno
│   └── requirements.txt      # Dependencias
│
├── public/
│   ├── index.html            # Página principal
│   ├── login.html            # Inicio de sesión
│   ├── register.html         # Registro de usuarios
│   ├── carrito.html          # Carrito de compras
│   ├── admin.html            # Panel de administración
│   ├── css/
│   │   ├── style.css         # Estilos generales
│   │   ├── login.css         # Estilos de login
│   │   ├── register.css      # Estilos de registro
│   │   └── admin.css         # Estilos de administración
│   └── js/
│       ├── api.js            # Cliente API para JS
│       └── toast.js          # Notificaciones
│
└── Dockerfile                # Contenedor Docker
```

---

## 🛠️ Configuración Rápida

1. **Clonar el repositorio:**
```
git clone <URL_DEL_REPOSITORIO>
cd proyecto
```

2. **Crear entorno virtual:**
```
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate   # Windows
```

3. **Instalar dependencias:**
```
pip install -r backend/requirements.txt
```

4. **Configurar variables de entorno:**
Crea un archivo `backend/.env` con el siguiente contenido:
```
AWS_PROFILE=academy
AWS_REGION=us-east-1
USERS_TABLE=Usuarios
PRODUCTS_TABLE=Productos
FLASK_RUN_PORT=5000
FLASK_ENV=development
ADMIN_EMAIL=adminluried@gmail.com
ADMIN_PASS=1234
SECRET_KEY=03112010
```

5. **Ejecutar el servidor:**
```
python backend/app.py
```

6. **Verificar que funcione:**  
   Visita `http://localhost:5000` en tu navegador.

---

## 🚀 Opción con Docker

Si prefieres usar Docker:

```
docker build -t vinilos-app .
docker run -d -p 5000:5000 vinilos-app
```

---

## 📦 Funcionalidades Principales

- **Autenticación:** Login y registro de usuarios
- **CRUD de Productos:** Crear, leer, actualizar y eliminar productos
- **Carrito de Compras:** Añadir y eliminar ítems
- **Pedidos:** Gestión de órdenes de compra
- **Notificaciones:** Mensajes de éxito y error con `toast.js`

---

## 📋 Notas Importantes

- Asegúrate de que las tablas DynamoDB (`Usuarios`, `Productos`, `Carrito`, `Orders`) estén creadas en tu cuenta de AWS.
- Nunca subas tu archivo `.env` a un repositorio público sin encriptar.

---

¡Gracias por usar este proyecto! 🎶