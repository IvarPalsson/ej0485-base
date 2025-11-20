# 📄 Instrucciones para publicar tu página en GitHub Pages

## ✅ Preparación completada

- ✅ Ruta del CSS corregida a relativa (`css/style.css`)
- ✅ Archivo renombrado a `index.html` (requerido por GitHub Pages)
- ✅ Repositorio conectado: `https://github.com/IvarPalsson/ej0485-base`

---

## 🚀 PASO 1: Hacer commit de los cambios

Primero, necesitas subir los cambios que acabamos de hacer:

```bash
cd C:\Users\David\Desktop\ejdaw\ej0485\base
git add .
git commit -m "Preparar para GitHub Pages: renombrar a index.html y corregir ruta CSS"
git push origin main
```

---

## 🌐 PASO 2: Habilitar GitHub Pages desde la terminal

**Opción A: Usando GitHub CLI (más rápido)**

```bash
gh repo edit IvarPalsson/ej0485-base --enable-pages --pages-source=main
```

**Opción B: Desde la interfaz web de GitHub**

1. Ve a tu repositorio: **https://github.com/IvarPalsson/ej0485-base**
2. Haz clic en **Settings** (Configuración) en el menú superior del repositorio
3. En el menú lateral izquierdo, busca y haz clic en **Pages**
4. En la sección **Source** (Fuente):
   - Selecciona **Deploy from a branch** (Desplegar desde una rama)
   - En **Branch** (Rama), selecciona **main**
   - En **Folder** (Carpeta), selecciona **/ (root)** o **/root**
   - Haz clic en **Save** (Guardar)

---

## ⏳ PASO 3: Esperar el despliegue

- GitHub Pages tarda **1-2 minutos** en desplegar tu sitio
- Verás un mensaje verde: *"Your site is live at..."* (Tu sitio está en vivo en...)
- La URL será: **https://ivarpalsson.github.io/ej0485-base/**

---

## 🔍 PASO 4: Verificar que está funcionando

**Opción A: Desde la terminal**

```bash
gh repo view IvarPalsson/ej0485-base --web
```

Luego ve a la pestaña **Settings** → **Pages** para ver la URL.

**Opción B: Desde el navegador**

1. Ve a: **https://github.com/IvarPalsson/ej0485-base**
2. Haz clic en **Settings** → **Pages**
3. Verás la URL de tu sitio: **https://ivarpalsson.github.io/ej0485-base/**

---

## 📝 PASO 5: Acceder a tu página web

Una vez desplegado, tu página estará disponible en:

**🌐 https://ivarpalsson.github.io/ej0485-base/**

---

## 🔄 Actualizar tu página

Cada vez que hagas cambios y los subas a GitHub:

```bash
git add .
git commit -m "Descripción de los cambios"
git push origin main
```

GitHub Pages se actualizará automáticamente en 1-2 minutos.

---

## ❓ Solución de problemas

**La página no carga o muestra 404:**
- Espera 2-3 minutos después de habilitar Pages
- Verifica que el archivo se llame `index.html` (no `base.html`)
- Verifica que la ruta del CSS sea relativa: `css/style.css` (no `/css/style.css`)

**Los estilos no se cargan:**
- Verifica que la ruta del CSS en `index.html` sea: `href="css/style.css"`
- Asegúrate de que el archivo `css/style.css` esté en el repositorio

**Ver el estado del despliegue:**
```bash
gh api repos/IvarPalsson/ej0485-base/pages
```

---

## ✅ Resumen rápido (todo en uno)

```bash
# 1. Subir cambios
cd C:\Users\David\Desktop\ejdaw\ej0485\base
git add .
git commit -m "Preparar para GitHub Pages"
git push origin main

# 2. Habilitar GitHub Pages
gh repo edit IvarPalsson/ej0485-base --enable-pages --pages-source=main

# 3. Esperar 1-2 minutos y visitar:
# https://ivarpalsson.github.io/ej0485-base/
```

---

## 🎉 ¡Listo!

Tu página estará disponible públicamente en:
**https://ivarpalsson.github.io/ej0485-base/**

