⚙️ Funcionalidades desarrolladas en esta entrega
Esta entrega implementa un sistema completo de autenticación y autorización de usuarios mediante JWT, Passport y cookies.

Funciones principales:
✅ Registro de usuarios (/api/sessions/register)

Crea usuarios con contraseña encriptada (bcrypt)

Guarda cart asociado y rol por defecto (user)

✅ Login con JWT (/api/sessions/login)

Devuelve un token JWT alojado en una cookie segura (jwtCookie)

Valida contraseña hasheada

✅ Ruta protegida /current (/api/sessions/current)

Extrae el JWT desde la cookie

Autentica el usuario con estrategia Passport-JWT

Devuelve los datos del usuario logueado


IMPORTANTE :Los archivos que no llevan ✅, no son necesarios para la entrega pero funcionan de contencion para todo el proyecto (no es necesario chequearlos)
 

├── config/
│   └── passport.js               # ✅Configuración de Passport con JWT
├── models/
│   ├── cart.js                   # Modelo de carrito
│   ├── product.js                # Modelo de producto
│   └── user.js                   # ✅ Modelo de usuario (importante)
├── routes/
│   ├── carts.js                  # Rutas de carritos
│   ├── products.js               # Rutas de productos
│   ├── sessions.js               # ✅ Rutas de autenticación y JWT
│   └── views.js                  # Rutas para vistas (no relevantes)
├── utils/
│   └── hash.js                   # ✅ Funciones de hash para contraseñas
├── views/                        # Vistas con Handlebars (no necesarias para esta entrega)
├── public/                       # Archivos estáticos (no necesarios para esta entrega)
├── .gitignore
├── app.js                        # ✅ App principal con configuración de middlewares y rutas
├── package.json
├── README.md

⚙️ Funcionalidades desarrolladas en esta entrega
Esta entrega implementa un sistema completo de autenticación y autorización de usuarios mediante JWT, Passport y cookies.

Funciones principales:
✅ Registro de usuarios → POST /api/sessions/register

Crea un nuevo usuario con contraseña encriptada utilizando bcrypt

Valida que el email no exista previamente

Asocia un carrito vacío al usuario y asigna el rol por defecto (user)

✅ Login con JWT → POST /api/sessions/login

Verifica credenciales con validación de contraseña hasheada

Si son correctas, genera un token JWT

Devuelve el token alojado en una cookie segura (jwtCookie)

✅ Ruta protegida /current → GET /api/sessions/current

Extrae el token JWT desde la cookie

Autentica al usuario con estrategia jwt de Passport

Devuelve los datos del usuario autenticado

💡 Todas las rutas son testeables desde Postman. No es necesario contar con interfaz visual para esta entrega.

📁 Archivos relevantes para la entrega
⚠️ IMPORTANTE: Los archivos que no llevan el ícono ✅ no son requeridos para esta entrega, pero forman parte estructural del proyecto general. No es necesario chequearlos para corregir.

php
Copiar
Editar
├── config/
│   └── passport.js               # ✅ Configuración de Passport con JWT
├── models/
│   ├── cart.js                   # Modelo de carrito
│   ├── product.js                # Modelo de producto
│   └── user.js                   # ✅ Modelo de usuario con hashing y validaciones
├── routes/
│   ├── carts.js                  # Rutas de carritos
│   ├── products.js               # Rutas de productos
│   ├── sessions.js               # ✅ Rutas de autenticación y JWT
│   └── views.js                  # Rutas para vistas (no utilizadas en esta entrega)
├── utils/
│   └── hash.js                   # ✅ Funciones de hash y comparación de contraseñas
├── views/                        # Vistas con Handlebars (no necesarias para esta entrega)
├── public/                       # Archivos estáticos (no necesarios para esta entrega)
├── .gitignore
├── app.js                        # ✅ App principal con configuración de rutas y middlewares
├── package.json
├── README.md
