
# 🚀 Guía Detallada: Cómo Desplegar un Proyecto en Vercel

## ✅ Requisitos Previos

- Tener una cuenta en Vercel ([https://vercel.com](https://vercel.com)).
- Tener una cuenta en GitHub.
- Tener un proyecto web listo (React, Next.js, Angular, Vue, Node.js, etc.).
- Tener el proyecto subido a GitHub.
- Desplegar o descargar el código fuente que se encuentra en el siguiente enlace: ([Código fuente](https://github.com/rcuello/ac4dem1a/tree/master/sistemas-distribuidos/poke-dex-lab)).

---

## 1. 🗂 Sube tu Proyecto a un Repositorio


Si aún no lo subiste, desde la terminal:

```bash
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/guia/ejemplo.git
git push -u origin main

```
- estos codigos los encuentre en el repositorio credo en GitHub
- Si no reconoce el termino “git” su computador es porque no está instalado el “git”
  
- [descargar git](https://git-scm.com/downloads). 

---

## 2. 🔐 Ingresa a Vercel

1. Ve a [https://vercel.com](https://vercel.com).
2. Inicia sesión con tu cuenta de GitHub, GitLab o Bitbucket.
3. Haz clic en **"Add New Project"**.

---

## 3. 🔍 Selecciona el Repositorio

1. Vercel mostrará una lista de tus repos disponibles.
2. Selecciona el repositorio del proyecto que quieres desplegar.
3. Vercel detectará automáticamente el framework utilizado.

---

## 4. 🚀 Realiza el Despliegue

1. Haz clic en **"Deploy"**.
2. Espera a que Vercel instale las dependencias, compile el proyecto y lo despliegue.
3. Obtendrás una URL pública del tipo:

```
https://nombre-ejemplo-guia.vercel.app
```

---

## 5. 🔁 Actualizaciones Automáticas

Cada vez que hagas `push` a la rama conectada (por ejemplo `main`), Vercel volverá a desplegar automáticamente la nueva versión.

---


## 5. 🌐 extra

-En caso de que las imágenes no carguen bien se modifica el archivo “environment.prod” que se encuentra en la ruta “\src\environments”  
 imagesPath: '/pokedex-angular/assets/images' 
 a 
 imagesPath: ' /assets/images'


-Para aumentar la seguridad de la pagina desplegada se crea un archivo llamado vercel.json 
 Con lo siguiente:

```
{
  "version": 2,
  "headers": [
    {
      "source": "/(.*)",
      "headers": [
        {
          "key": "Content-Security-Policy",
          "value": "default-src 'self'; script-src 'self' 'unsafe-inline' https:; style-src 'self' 'unsafe-inline' https:; img-src 'self' data: https:; font-src 'self' data: https:; connect-src 'self' https:;"
        },
        {
          "key": "X-Frame-Options",
          "value": "SAMEORIGIN"
        },
        {
          "key": "X-Content-Type-Options",
          "value": "nosniff"
        },
        {
          "key": "Referrer-Policy",
          "value": "strict-origin-when-cross-origin"
        },
        {
          "key": "Permissions-Policy",
          "value": "geolocation=(), microphone=(), camera=()"
        },
        {
          "key": "Access-Control-Allow-Origin",
          "value": "https://pokedex-desplegado.vercel.app/"
        },
        {
          "key": "Access-Control-Allow-Methods",
          "value": "GET, POST, OPTIONS"
        },
        {
          "key": "Access-Control-Allow-Headers",
          "value": "Content-Type, Authorization"
        }
      ]
    }
  ]
}
```
-Se guarda en la entrada principal 





## ✅ ¡Listo!

Tu proyecto ahora está corriendo en producción con actualizaciones automáticas en cada commit.
