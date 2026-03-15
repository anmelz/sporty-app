# Sporty App (Native)

App nativa iOS y Android para [Sporty](https://www.sportyven.com). Carga la plataforma web en un contenedor nativo con Capacitor.

## Requisitos

- Node.js 18+
- **iOS**: Mac con Xcode
- **Android**: Android Studio

## Instalación

```bash
npm install
```

## Desarrollo

```bash
# Sincronizar cambios a proyectos nativos
npm run cap:sync

# Abrir en Xcode (iOS)
npm run cap:ios

# Abrir en Android Studio (Android)
npm run cap:android
```

## Configuración

- **URL**: La app carga `https://www.sportyven.com` en un WebView
- **App ID**: `com.sportyven.app`
- **Deep link**: `sporty://auth/callback` (para OAuth)
- **Config**: `capacitor.config.json`

## OAuth (Google Login) - Supabase

Para que el login con Google funcione en la app nativa:

1. Ir a [Supabase Dashboard](https://supabase.com/dashboard) → tu proyecto
2. **Authentication** → **URL Configuration**
3. En **Redirect URLs**, añadir:
   - `sporty://auth/callback`
   - `https://www.sportyven.com/auth/callback` (si no está ya)

La app usa el scheme `sporty://` para capturar el redirect de OAuth cuando se abre en navegador externo.

## Iconos y Splash

Los iconos de Sporty están en `resources/` (icon.png, splash.png). Para regenerar los assets nativos:

```bash
npx @capacitor/assets generate
npm run cap:sync
```

## Repositorios

- **Web**: [sports-scheduler](https://github.com/anmelz/sports-scheduler)
- **App nativa**: [sporty-app](https://github.com/anmelz/sporty-app)
