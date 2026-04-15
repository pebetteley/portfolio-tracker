# 🚀 Guía Paso a Paso: Subir Portfolio Tracker a GitHub

## 📋 **Pasos Previos**

### 1. Crear cuenta en GitHub (si no tienes)
- Ve a https://github.com
- Clic en "Sign up"
- Completa el registro

### 2. Instalar Git (si no tienes)

**Windows:**
- Descarga: https://git-scm.com/download/win
- Instala con opciones por defecto

**Mac:**
```bash
brew install git
# o desde: https://git-scm.com/download/mac
```

**Linux:**
```bash
sudo apt-get install git  # Ubuntu/Debian
sudo yum install git      # CentOS/RedHat
```

### 3. Configurar Git (primera vez)
```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu_email@ejemplo.com"
```

---

## 📦 **Opción 1: Crear Repositorio desde GitHub (MÁS FÁCIL)**

### Paso 1: Crear repositorio en GitHub
1. Ve a https://github.com
2. Clic en el **+** arriba a la derecha → "New repository"
3. Configuración:
   - **Repository name**: `portfolio-tracker`
   - **Description**: "Sistema profesional de seguimiento de portfolios con análisis técnico en tiempo real"
   - **Public** (para que otros lo vean) o **Private** (solo tú)
   - ✅ Marcar "Add a README file"
   - ✅ Marcar "Add .gitignore" → Template: None
   - ✅ Marcar "Choose a license" → MIT License
4. Clic en **"Create repository"**

### Paso 2: Clonar repositorio a tu computadora
```bash
# Reemplaza TU_USUARIO con tu nombre de usuario de GitHub
git clone https://github.com/TU_USUARIO/portfolio-tracker.git
cd portfolio-tracker
```

### Paso 3: Agregar los archivos
Copia todos los archivos descargados a la carpeta `portfolio-tracker`:
- `portfolio-tracker-advanced.html` (versión con API)
- `portfolio-tracker-pro.html` (versión básica)
- `README.md` (documentación)
- `LICENSE` (licencia MIT)
- `.gitignore` (archivos a ignorar)
- `CONTRIBUTING.md` (guía para contribuidores)
- `CHANGELOG.md` (historial de versiones)

**Renombrar archivo:**
```bash
# Renombrar gitignore a .gitignore
mv gitignore .gitignore
```

### Paso 4: Subir archivos a GitHub
```bash
# Agregar todos los archivos
git add .

# Crear commit
git commit -m "feat: versión inicial con API de Yahoo Finance"

# Subir a GitHub
git push origin main
```

### Paso 5: Verificar
Ve a `https://github.com/TU_USUARIO/portfolio-tracker` y verás todos tus archivos!

---

## 📦 **Opción 2: Subir Proyecto Existente desde Terminal**

### Paso 1: Crear repositorio VACÍO en GitHub
1. Ve a https://github.com
2. Clic en **+** → "New repository"
3. Nombre: `portfolio-tracker`
4. **NO marques ninguna opción** (README, .gitignore, License)
5. Clic en "Create repository"

### Paso 2: Inicializar Git en tu carpeta local
```bash
# Ir a la carpeta donde descargaste los archivos
cd /ruta/a/tus/archivos

# Inicializar Git
git init

# Renombrar gitignore a .gitignore
mv gitignore .gitignore

# Agregar todos los archivos
git add .

# Crear primer commit
git commit -m "feat: versión inicial del Portfolio Tracker"

# Renombrar rama a main (si es necesario)
git branch -M main

# Conectar con GitHub (reemplaza TU_USUARIO)
git remote add origin https://github.com/TU_USUARIO/portfolio-tracker.git

# Subir todo a GitHub
git push -u origin main
```

---

## 🌐 **Activar GitHub Pages (Para tener URL pública)**

### Paso 1: Configurar GitHub Pages
1. Ve a tu repositorio: `https://github.com/TU_USUARIO/portfolio-tracker`
2. Clic en **Settings** (arriba derecha)
3. En el menú izquierdo → **Pages**
4. En "Source":
   - Branch: `main`
   - Folder: `/ (root)`
5. Clic en **Save**

### Paso 2: Esperar deployment (1-2 minutos)
GitHub te mostrará un mensaje: "Your site is published at..."

### Paso 3: Acceder a tu app
Tu Portfolio Tracker estará disponible en:
```
https://TU_USUARIO.github.io/portfolio-tracker/portfolio-tracker-advanced.html
```

**URLs de ejemplo:**
- Versión Advanced: `https://TU_USUARIO.github.io/portfolio-tracker/portfolio-tracker-advanced.html`
- Versión Basic: `https://TU_USUARIO.github.io/portfolio-tracker/portfolio-tracker-pro.html`

---

## 📝 **Actualizar el README con tu información**

Edita `README.md` y reemplaza:
- `TU_USUARIO` → tu nombre de usuario de GitHub
- `tu_email@ejemplo.com` → tu email
- Agrega capturas de pantalla en carpeta `screenshots/`

---

## 🎨 **Agregar Capturas de Pantalla (Opcional pero recomendado)**

### Paso 1: Crear carpeta screenshots
```bash
mkdir screenshots
```

### Paso 2: Tomar capturas
1. Abre `portfolio-tracker-advanced.html` en tu navegador
2. Toma capturas de:
   - Dashboard principal
   - Panel de recomendaciones
   - Tabla con análisis técnico
   - Gráficos

### Paso 3: Guardar imágenes
Guarda las imágenes como:
- `screenshots/dashboard.png`
- `screenshots/recommendations.png`
- `screenshots/technical-analysis.png`
- `screenshots/charts.png`

### Paso 4: Actualizar README.md
Reemplaza las líneas de capturas:
```markdown
### Dashboard Principal
![Dashboard](screenshots/dashboard.png)

### Panel de Recomendaciones
![Recomendaciones](screenshots/recommendations.png)
```

### Paso 5: Subir cambios
```bash
git add screenshots/
git add README.md
git commit -m "docs: agregar capturas de pantalla"
git push
```

---

## 🏷️ **Crear Primera Release (Opcional)**

### Paso 1: Crear tag
```bash
git tag -a v2.0.0 -m "Versión 2.0.0 - API Real y Análisis Técnico"
git push origin v2.0.0
```

### Paso 2: Crear Release en GitHub
1. Ve a tu repo → **Releases** → **Create a new release**
2. Tag: `v2.0.0`
3. Title: `Portfolio Tracker v2.0.0`
4. Description: Copia el changelog de `CHANGELOG.md`
5. Adjunta archivos ZIP (opcional)
6. Clic en **Publish release**

---

## 🔧 **Comandos Git Útiles**

```bash
# Ver estado de archivos
git status

# Ver historial de commits
git log --oneline

# Ver cambios antes de commit
git diff

# Deshacer cambios no guardados
git checkout -- archivo.html

# Deshacer último commit (mantiene cambios)
git reset --soft HEAD~1

# Actualizar desde GitHub
git pull

# Ver ramas
git branch

# Crear nueva rama
git checkout -b feature/nueva-funcionalidad

# Cambiar de rama
git checkout main
```

---

## 🎯 **Siguientes Pasos Recomendados**

1. ✅ Personalizar README.md con tu info
2. ✅ Agregar capturas de pantalla
3. ✅ Activar GitHub Pages
4. ✅ Crear primera Release (v2.0.0)
5. ✅ Compartir URL con amigos
6. ✅ Agregar topics en GitHub:
   - `portfolio-management`
   - `stock-tracker`
   - `technical-analysis`
   - `yahoo-finance`
   - `javascript`
   - `chartsjs`

### Para agregar topics:
1. Ve a tu repositorio
2. Clic en el ⚙️ junto a "About"
3. Agrega los topics mencionados
4. Clic en "Save changes"

---

## 🆘 **Solución de Problemas Comunes**

### Error: "Permission denied"
```bash
# Configurar autenticación con Personal Access Token
# 1. Ve a GitHub → Settings → Developer settings → Personal access tokens
# 2. Generate new token → Marca "repo"
# 3. Copia el token
# 4. Usa como contraseña cuando Git te la pida
```

### Error: "Updates were rejected"
```bash
# Actualizar primero desde GitHub
git pull origin main --rebase
git push origin main
```

### Error: "Not a git repository"
```bash
# Asegúrate de estar en la carpeta correcta
cd /ruta/correcta
git init
```

---

## 📧 **¿Necesitas Ayuda?**

- 📖 [Git Documentation](https://git-scm.com/doc)
- 📖 [GitHub Guides](https://guides.github.com/)
- 💬 Pregunta en Issues del repo

---

**¡Listo! Tu Portfolio Tracker está en GitHub y listo para compartir! 🚀**
