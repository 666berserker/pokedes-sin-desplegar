
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
git remote add origin https://github.com/usuario/nombre-del-repo.git
git add .
git commit -m "Primer commit"
git push -u origin master
```

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


## 5. 🌐 en caso de que las imágenes no carguen bien 

En caso de que las imágenes no carguen bien se modifica el archivo “environment.prod” que se encuentra en la ruta “\src\environments”  
imagesPath: '/pokedex-angular/assets/images' 
a 
imagesPath: ' /assets/images'

.


## ✅ ¡Listo!

Tu proyecto ahora está corriendo en producción con actualizaciones automáticas en cada commit.
