
# 🚀 Guía Detallada: Cómo Desplegar un Proyecto en Vercel

## ✅ Requisitos Previos

- Tener una cuenta en Vercel ([https://vercel.com](https://vercel.com)).
- Tener una cuenta en GitHub.
- Tener un proyecto web listo (React, Next.js, Angular, Vue, Node.js, etc.).
- Tener el proyecto subido a GitHub.

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

## 4. ⚙️ Configuración del Proyecto

- **Framework Preset**: elige el framework si no se detecta automáticamente.
- **Root Directory** (opcional): si tu código está dentro de una carpeta (ej. `/frontend`).
- **Build Command**:
  - Angular: `ng build --configuration production`
  - React: `npm run build`
  - Vue: `npm run build`
- **Output Directory**:
  - Angular: `dist/nombre-del-proyecto`
  - React/Vue/Next.js: normalmente `build` o `.next`

---

## 5. 🧪 Agrega Variables de Entorno (si aplica)

1. En la sección "Environment Variables", agrega las necesarias.

```env
API_URL=https://api.midominio.com
```

---

## 6. 🚀 Realiza el Despliegue

1. Haz clic en **"Deploy"**.
2. Espera a que Vercel instale las dependencias, compile el proyecto y lo despliegue.
3. Obtendrás una URL pública del tipo:

```
https://nombre-proyecto.vercel.app
```

---

## 7. 🌐 Agrega tu Dominio Personalizado (opcional)

1. Ve a tu panel de Vercel.
2. En **Settings > Domains**, añade tu dominio.
3. Sigue las instrucciones para configurar los registros DNS.

---

## 8. 🔁 Actualizaciones Automáticas

Cada vez que hagas `push` a la rama conectada (por ejemplo `main`), Vercel volverá a desplegar automáticamente la nueva versión.

---

## ✅ ¡Listo!

Tu proyecto ahora está corriendo en producción con actualizaciones automáticas en cada commit.
