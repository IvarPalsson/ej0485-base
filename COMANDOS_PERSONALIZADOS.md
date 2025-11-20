# Comandos personalizados para IvarPalsson

## 🔐 PASO 1: Autenticarse en GitHub CLI

**Ejecuta este comando en tu terminal BASH:**

```bash
gh auth login
```

**Sigue las instrucciones:**
1. Selecciona: **GitHub.com** (presiona Enter)
2. Selecciona: **HTTPS** (presiona Enter)
3. Selecciona: **Login with a web browser** (presiona Enter)
4. Presiona **Enter** para abrir el navegador
5. Copia el código que aparece (ej: `ABCD-1234`)
6. Pega el código en el navegador y autoriza GitHub CLI
7. Vuelve a la terminal y presiona **Enter**

---

## 📦 PASO 2: Navegar al directorio

```bash
cd /c/Users/David/Desktop/ejdaw/ej0485/base
```

O en Git Bash:
```bash
cd ~/Desktop/ejdaw/ej0485/base
```

---

## 🆕 PASO 3: Crear repositorio y subir archivos

**Elige un nombre para tu repositorio** (ej: `ej0485-base`, `practica-selectores-css`, etc.)

Luego ejecuta:

```bash
gh repo create ej0485-base --public --source=. --remote=origin --push
```

**Reemplaza `ej0485-base` con el nombre que prefieras.**

Este comando:
- ✅ Crea el repositorio en GitHub bajo tu cuenta (IvarPalsson)
- ✅ Lo conecta con tu repositorio local
- ✅ Sube automáticamente todos los archivos commiteados

---

## ✅ PASO 4: Verificar

```bash
git remote -v
```

Deberías ver:
```
origin  https://github.com/IvarPalsson/ej0485-base.git (fetch)
origin  https://github.com/IvarPalsson/ej0485-base.git (push)
```

**Abre tu repositorio en el navegador:**
```bash
gh repo view --web
```

O visita directamente:
**https://github.com/IvarPalsson/ej0485-base**

---

## 🎯 Resumen completo (copia y pega en orden)

```bash
# 1. Autenticarse (solo la primera vez)
gh auth login

# 2. Ir al directorio
cd /c/Users/David/Desktop/ejdaw/ej0485/base

# 3. Crear y subir (cambia el nombre si quieres)
gh repo create ej0485-base --public --source=. --remote=origin --push

# 4. Verificar
git remote -v
gh repo view --web
```

---

## 📝 Notas importantes

- Tu perfil: **https://github.com/IvarPalsson**
- El repositorio se creará bajo tu cuenta
- Los archivos `base.html` y `css/style.css` se subirán automáticamente
- Si el nombre del repositorio ya existe, elige otro nombre

