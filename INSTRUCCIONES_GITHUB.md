# Instrucciones para subir archivos a GitHub

## ✅ Paso 1: COMPLETADO
- Git está instalado
- Repositorio inicializado
- Archivos commiteados

## 📝 Paso 2: Crear repositorio en GitHub

1. Ve a https://github.com e inicia sesión
2. Haz clic en el botón **"+"** (arriba derecha) → **"New repository"**
3. Completa:
   - **Repository name**: `ej0485-base` (o el nombre que prefieras)
   - **Description**: "Práctica de selectores CSS"
   - **Visibility**: Public o Private (tu elección)
   - ⚠️ **NO marques** las opciones de README, .gitignore o license
4. Haz clic en **"Create repository"**

## 🔗 Paso 3: Conectar y subir archivos

Después de crear el repositorio, GitHub te mostrará comandos. Ejecuta estos comandos en PowerShell:

### Si es la primera vez que usas Git en este equipo:

```powershell
git config --global user.name "Tu Nombre"
git config --global user.email "tu-email@ejemplo.com"
```

### Conectar el repositorio remoto:

```powershell
cd C:\Users\David\Desktop\ejdaw\ej0485\base
git remote add origin https://github.com/TU_USUARIO/NOMBRE_REPOSITORIO.git
```

**Reemplaza:**
- `TU_USUARIO` → Tu nombre de usuario de GitHub
- `NOMBRE_REPOSITORIO` → El nombre que le diste al repositorio

### Subir los archivos:

```powershell
git branch -M main
git push -u origin main
```

Si te pide autenticación:
- **Usuario**: Tu nombre de usuario de GitHub
- **Contraseña**: Usa un **Personal Access Token** (no tu contraseña normal)

## 🔑 Crear Personal Access Token (si es necesario)

1. GitHub → Tu perfil → **Settings**
2. **Developer settings** (abajo a la izquierda)
3. **Personal access tokens** → **Tokens (classic)**
4. **Generate new token** → **Generate new token (classic)**
5. Nombre: "Mi PC" (o el que prefieras)
6. Selecciona: **repo** (todos los permisos de repositorio)
7. **Generate token**
8. **Copia el token** (solo se muestra una vez)
9. Úsalo como contraseña cuando Git te la pida

## ✅ Verificar

Ve a tu repositorio en GitHub y deberías ver:
- `base.html`
- `css/style.css`

¡Listo! 🎉

