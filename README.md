# CRM Inmobiliario · Carlos Fuster

App web de una sola página (`index.html`). Los datos se guardan en **Supabase** (proyecto `crm-inmobiliario`) y cada usuario solo ve los suyos tras iniciar sesión.

## Publicar en Vercel (GitHub)

1. En GitHub, crea un repositorio nuevo (mejor **privado**), por ejemplo `crm-inmobiliario`.
2. Pulsa **Add file → Upload files** y sube `index.html`, `README.md` y `.gitignore`.
   ⚠️ **No subas nunca `datos-iniciales.json` ni ninguna copia de seguridad**: contienen datos personales de tus contactos.
3. En [vercel.com](https://vercel.com) → **Add New… → Project** → importa el repositorio → **Deploy**. No hay que configurar nada (Framework: *Other*).
4. Vercel te dará un enlace del tipo `https://crm-inmobiliario.vercel.app`.

*Alternativa sin GitHub:* en Vercel puedes arrastrar la carpeta con `index.html` directamente.

## Configurar Supabase (una sola vez, 1 minuto)

En [supabase.com](https://supabase.com/dashboard) → proyecto **crm-inmobiliario** → **Authentication → URL Configuration**:
- **Site URL:** pega tu enlace de Vercel.
- **Redirect URLs:** añade el mismo enlace.

Así los emails de confirmación y de cambio de contraseña te devuelven al CRM.

## Primer uso

1. Abre tu enlace de Vercel → **Crear cuenta** con tu email y una contraseña.
2. Confirma el email que te llega y vuelve a entrar.
3. Ve a **Ajustes → Importar copia (JSON)** y elige `datos-iniciales.json` (o una copia exportada desde la versión de Claude, si has hecho cambios allí).
4. Recomendado: en Supabase → **Authentication → Sign In / Providers**, desactiva *Allow new users to sign up* cuando ya tengas tu cuenta.

## Copias de seguridad

**Ajustes → Exportar copia (JSON)** descarga todos los datos (con fotos opcionales). Guárdalas fuera de GitHub.
