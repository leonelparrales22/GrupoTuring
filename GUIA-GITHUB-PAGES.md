# 📘 Guía Rápida: Publicar en GitHub Pages

## ⚡ Opción Más Rápida (Recomendada para principiantes)

### Método 1: Upload desde GitHub.com

#### Paso 1: Crear cuenta en GitHub
1. Ve a https://github.com
2. Click en "Sign up" (si no tienes cuenta)
3. Completa el registro

#### Paso 2: Crear repositorio
1. Click en el botón `+` (arriba a la derecha) → "New repository"
2. **Repository name**: `grupoturing-landing`
3. **Description**: "Landing page oficial de Grupo Turing"
4. Seleccionar: **Public**
5. ❌ NO marcar "Add a README file"
6. Click en **"Create repository"**

#### Paso 3: Subir archivos
1. En la página del repositorio, click en **"uploading an existing file"**
2. Arrastra TODOS estos archivos a la ventana:
   ```
   ✅ index.html
   ✅ favicon.png
   ✅ LogoEmpresa.jpg
   ✅ robots.txt
   ✅ sitemap.xml
   ✅ CNAME
   ✅ .nojekyll
   ✅ README.md
   ✅ SEO-INSTRUCCIONES.md
   ✅ CHECKLIST-SEO-INMEDIATO.md
   ✅ CAMBIOS-ECUADOR.md
   ```
3. En "Commit changes":
   - Título: `Initial commit - Sitio web Grupo Turing`
4. Click en **"Commit changes"**
5. ⏰ **Espera 1 minuto** mientras se suben los archivos

#### Paso 4: Activar GitHub Pages
1. Ve a la pestaña **"Settings"** (⚙️)
2. En el menú izquierdo, click en **"Pages"**
3. En **"Source"**:
   - Branch: Selecciona `main` (o `master`)
   - Folder: `/root`
4. Click en **"Save"**
5. 🎉 Aparecerá un mensaje: "Your site is ready to be published at..."

#### Paso 5: Ver tu sitio
1. ⏰ **Espera 2-5 minutos** (GitHub necesita tiempo para procesar)
2. Actualiza la página de Settings → Pages
3. Verás: **"Your site is live at https://TU-USUARIO.github.io/grupoturing-landing/"**
4. 🎉 **Click en el enlace** para ver tu sitio publicado

---

## 💻 Método 2: Usando Git (Para usuarios técnicos)

### Prerrequisitos
- Git instalado en tu computadora
- Cuenta de GitHub

### Comandos

```bash
# 1. Navegar a la carpeta del proyecto
cd C:\Users\edwar\Documents\Cursor\GrupoTuring

# 2. Inicializar repositorio Git
git init

# 3. Agregar todos los archivos
git add .

# 4. Hacer el primer commit
git commit -m "Initial commit - Sitio web Grupo Turing Ecuador"

# 5. Crear repositorio en GitHub.com (hazlo desde la web)
# URL: https://github.com/new
# Nombre: grupoturing-landing

# 6. Conectar repositorio local con GitHub
git remote add origin https://github.com/TU-USUARIO/grupoturing-landing.git

# 7. Subir archivos
git branch -M main
git push -u origin main

# 8. Activar GitHub Pages desde Settings → Pages (en la web)
```

---

## 🖥️ Método 3: Usando GitHub Desktop (Visual)

### Paso 1: Descargar GitHub Desktop
1. Ve a https://desktop.github.com/
2. Descarga e instala GitHub Desktop
3. Inicia sesión con tu cuenta de GitHub

### Paso 2: Agregar el proyecto
1. Abre GitHub Desktop
2. **File** → **Add Local Repository**
3. Click en **"Choose..."**
4. Selecciona la carpeta: `C:\Users\edwar\Documents\Cursor\GrupoTuring`
5. Si dice "no es repositorio", click en **"Create a repository here instead"**

### Paso 3: Hacer commit inicial
1. Verás todos los archivos en la lista
2. En "Summary": Escribe `Initial commit`
3. En "Description": `Sitio web oficial de Grupo Turing`
4. Click en **"Commit to main"**

### Paso 4: Publicar en GitHub
1. Click en **"Publish repository"** (arriba)
2. Name: `grupoturing-landing`
3. Description: `Landing page oficial de Grupo Turing Ecuador`
4. ✅ Asegúrate que **NO** esté marcado "Keep this code private"
5. Click en **"Publish repository"**

### Paso 5: Activar GitHub Pages
1. Ve a GitHub.com → Tu repositorio
2. Settings → Pages
3. Source: `main` branch, `/root` folder
4. Save

---

## 🌐 Configurar Dominio Personalizado (grupoturing.com)

### Después de publicar en GitHub Pages:

#### Paso 1: Configurar DNS (En tu proveedor de dominio)

```dns
# Eliminar registros A existentes para @ y www

# Agregar estos 4 registros A:
Tipo: A      Host: @      Valor: 185.199.108.153
Tipo: A      Host: @      Valor: 185.199.109.153
Tipo: A      Host: @      Valor: 185.199.110.153
Tipo: A      Host: @      Valor: 185.199.111.153

# Agregar registro CNAME para www:
Tipo: CNAME  Host: www    Valor: TU-USUARIO.github.io.
```

#### Paso 2: Verificar DNS (Espera 1-24 horas)
- Usa https://dnschecker.org/
- Busca: grupoturing.com
- Verifica que los registros A apunten a GitHub

#### Paso 3: Activar dominio en GitHub
1. GitHub → Repositorio → Settings → Pages
2. Custom domain: `grupoturing.com`
3. Click en "Save"
4. Espera verificación (puede tomar horas)
5. ✅ Marca "Enforce HTTPS" cuando esté disponible

#### Paso 4: El archivo CNAME
- Ya está incluido en tu proyecto
- Contiene: `grupoturing.com`
- GitHub lo usa automáticamente

---

## ✅ Checklist Final

### Antes de publicar:
- [ ] Revisar que todos los archivos estén en la carpeta
- [ ] Verificar que favicon.png y LogoEmpresa.jpg existan
- [ ] Probar index.html localmente (abrir en navegador)

### Después de publicar:
- [ ] Esperar 5 minutos y visitar la URL de GitHub Pages
- [ ] Verificar que el sitio se ve bien
- [ ] Probar en móvil (responsive)
- [ ] Probar todos los botones y enlaces
- [ ] Probar formulario de contacto

### SEO (Primera semana):
- [ ] Configurar Google Search Console
- [ ] Enviar sitemap.xml
- [ ] Configurar Google My Business
- [ ] Instalar Google Analytics
- [ ] Verificar meta tags con https://metatags.io

---

## 🚨 Problemas Comunes y Soluciones

### ❌ "404 - Page not found"
**Solución:**
- Espera 5-10 minutos después de activar Pages
- Verifica que index.html esté en la raíz (no en subcarpeta)
- Verifica que GitHub Pages esté activado (Settings → Pages)

### ❌ "Las imágenes no cargan"
**Solución:**
- Verifica nombres de archivo (case-sensitive en Linux)
- `LogoEmpresa.jpg` debe ser exactamente así
- Verifica que las imágenes estén en el repositorio

### ❌ "El CSS no se aplica"
**Solución:**
- El sitio usa Tailwind CDN, funciona automáticamente
- Verifica tu conexión a internet
- Fuerza refresh: Ctrl + Shift + R (Cmd + Shift + R en Mac)

### ❌ "El dominio personalizado no funciona"
**Solución:**
- Espera 24-48 horas para propagación DNS
- Verifica DNS con dnschecker.org
- Asegúrate que el archivo CNAME esté en el repositorio
- Desactiva y reactiva el dominio en GitHub Pages

### ❌ "El formulario no envía"
**Solución:**
- GitHub Pages no soporta backend
- Opciones:
  1. Formspree: https://formspree.io (gratis, 50 envíos/mes)
  2. EmailJS: https://www.emailjs.com (gratis)
  3. Netlify Forms (si migras a Netlify)

---

## 📊 Verificar que TODO funciona

### Checklist de verificación:

```
✅ URLs a probar:
□ https://TU-USUARIO.github.io/grupoturing-landing/
□ https://TU-USUARIO.github.io/grupoturing-landing/robots.txt
□ https://TU-USUARIO.github.io/grupoturing-landing/sitemap.xml
□ https://TU-USUARIO.github.io/grupoturing-landing/favicon.png

✅ Elementos a verificar:
□ Logo carga correctamente
□ Pantalla de loading aparece
□ Todas las secciones son visibles
□ Botones funcionan (scroll suave)
□ Formulario muestra campos
□ Footer tiene información correcta
□ Responsive en móvil
□ No hay errores en consola (F12)

✅ SEO a verificar:
□ Título en pestaña: "Grupo Turing - Automatización..."
□ Favicon aparece en la pestaña
□ Meta description correcto
□ Open Graph funciona (probar compartir en WhatsApp)
```

---

## 🎯 Próximos Pasos Después de Publicar

### Día 1:
1. Compartir URL con el equipo
2. Probar en diferentes dispositivos
3. Configurar Google Search Console
4. Tomar screenshots para redes sociales

### Semana 1:
1. Configurar Google Analytics
2. Crear Google My Business
3. Registrar en directorios
4. Solicitar primeras reseñas

### Mes 1:
1. Publicar primer artículo de blog
2. Conseguir primeros backlinks
3. Analizar métricas
4. Optimizar basado en datos

---

## 📞 Soporte

### Documentación útil:
- GitHub Pages: https://docs.github.com/pages
- Git básico: https://git-scm.com/book/es/
- Dominios personalizados: https://docs.github.com/pages/configuring-a-custom-domain-for-your-github-pages-site

### Herramientas de verificación:
- PageSpeed: https://pagespeed.web.dev/
- DNS Checker: https://dnschecker.org/
- Meta Tags: https://metatags.io/
- Rich Results: https://search.google.com/test/rich-results

---

## 🎉 ¡Felicitaciones!

Una vez que sigas estos pasos, tu sitio estará en vivo y accesible para todo el mundo. 

**URL típica:** `https://TU-USUARIO.github.io/grupoturing-landing/`

¡Buena suerte con el lanzamiento de Grupo Turing! 🚀🇪🇨

