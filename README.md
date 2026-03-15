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

- **URL**: La app carga `https://www.sportyven.com` en un WebView.
- **App ID**: `com.sportyven.app`
- **Config**: `capacitor.config.json`

## OAuth (Google Login)

Para que el login con Google funcione en la app:

1. En [Supabase Dashboard](https://supabase.com/dashboard) → Authentication → URL Configuration
2. Añadir a **Redirect URLs**: `com.sportyven.app://**` (iOS) y el scheme equivalente para Android

## Iconos y Splash

Los iconos por defecto son los de Capacitor. Para usar los de Sporty:

1. Copiar `icon-192.png` y `icon-512.png` desde el proyecto web (`sports-scheduler/public/icons/`)
2. Usar [@capacitor/assets](https://github.com/ionic-team/capacitor-assets) para generar los tamaños nativos:

```bash
npx @capacitor/assets generate
```

## Repositorio

- **Web**: [sports-scheduler](https://github.com/anmelz/sports-scheduler)
- **App nativa**: Este repositorio
