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