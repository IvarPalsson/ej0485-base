# Instrucciones para crear repositorio en GitHub desde BASH

## 📋 Requisitos previos
- ✅ Git instalado
- ✅ GitHub CLI (gh) instalado
- ✅ Repositorio local con archivos commiteados

---

## 🔐 PASO 1: Autenticarse en GitHub CLI

Ejecuta este comando en tu terminal BASH:

```bash
gh auth login
```

**Sigue las instrucciones interactivas:**
1. Selecciona: **GitHub.com**
2. Selecciona: **HTTPS** (recomendado)
3. Selecciona: **Login with a web browser**
4. Presiona **Enter** para abrir el navegador
5. Copia el código que aparece (ej: `ABCD-1234`)
6. Pega el código en el navegador y autoriza GitHub CLI
7. Vuelve a la terminal y presiona **Enter**

**Verifica que estás autenticado:**
```bash
gh auth status
```

Deberías ver: `✓ Logged in to github.com as IvarPalsson`

---

## 📦 PASO 2: Navegar al directorio del proyecto

```bash
cd /c/Users/David/Desktop/ejdaw/ej0485/base
```

O si estás en Git Bash en Windows:
```bash
cd ~/Desktop/ejdaw/ej0485/base
```

---

## 🆕 PASO 3: Crear repositorio en GitHub desde la terminal

Ejecuta este comando (reemplaza `NOMBRE_REPOSITORIO` con el nombre que quieras):

```bash
gh repo create NOMBRE_REPOSITORIO --public --source=. --remote=origin --push
```

**Opciones del comando:**
- `NOMBRE_REPOSITORIO`: El nombre de tu repositorio (ej: `ej0485-base`)
- `--public`: Repositorio público (usa `--private` si quieres privado)
- `--source=.`: Usa el directorio actual como fuente
- `--remote=origin`: Conecta el repositorio remoto como "origin"
- `--push`: Sube automáticamente los archivos

**Ejemplo completo:**
```bash
gh repo create ej0485-base --public --source=. --remote=origin --push
```

---

## 🔄 Alternativa: Si prefieres hacerlo paso a paso

### 3a. Crear repositorio sin conectar automáticamente:
```bash
gh repo create NOMBRE_REPOSITORIO --public
```

### 3b. Conectar el repositorio local con el remoto:
```bash
git remote add origin https://github.com/IvarPalsson/NOMBRE_REPOSITORIO.git
```

### 3c. Subir los archivos:
```bash
git branch -M main
git push -u origin main
```

---

## ✅ PASO 4: Verificar

Verifica que todo está conectado:

```bash
git remote -v
```

Deberías ver algo como:
```
origin  https://github.com/IvarPalsson/NOMBRE_REPOSITORIO.git (fetch)
origin  https://github.com/IvarPalsson/NOMBRE_REPOSITORIO.git (push)
```

**Abre tu repositorio en el navegador:**
```bash
gh repo view --web
```

---

## 🎯 Resumen rápido (todo en uno)

```bash
# 1. Autenticarse (solo la primera vez)
gh auth login

# 2. Ir al directorio
cd /c/Users/David/Desktop/ejdaw/ej0485/base

# 3. Crear y subir (reemplaza NOMBRE_REPOSITORIO)
gh repo create NOMBRE_REPOSITORIO --public --source=. --remote=origin --push
```

---

## ❓ Solución de problemas

**Error: "repository already exists"**
- El nombre ya está en uso, elige otro nombre

**Error: "authentication required"**
- Ejecuta `gh auth login` de nuevo

**Error: "not a git repository"**
- Asegúrate de estar en el directorio correcto
- O ejecuta: `git init`

---

## 📝 Notas

- El repositorio se creará bajo tu cuenta de GitHub
- Los archivos ya commiteados se subirán automáticamente
- Puedes ver el repositorio en: `https://github.com/IvarPalsson/NOMBRE_REPOSITORIO`

