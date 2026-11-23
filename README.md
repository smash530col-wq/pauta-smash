# Pauta y redes · SMASH

Informe diario de pauta y segmentación (Meta Ads + WhatsApp) y de redes (Metricool), con inicio de sesión.

- Página estática (`index.html`) publicada con GitHub Pages.
- Datos en Supabase (tabla `pauta_dias`), protegidos con inicio de sesión: solo el usuario autorizado puede leerlos.
- La clave que va en la página es la pública (publishable); quién lee qué lo decide la base de datos.
- Cada noche una tarea programada en el computador del negocio guarda el informe del día en Supabase.

## Apps de celular

- **Android:** en *Releases* está `pauta.apk`. Se descarga desde el celular y se instala (puede pedir permitir "apps de origen desconocido").
- **iPhone:** `pauta-iphone-sin-firmar.ipa` necesita la firma de Apple para instalarse (cuenta de Apple Developer, o Sideloadly/AltStore con una cuenta de Apple gratis, que vence cada 7 días). Mientras tanto, en iPhone se puede usar la app web: Safari → Compartir → "Agregar a inicio".
- Las dos apps abren la versión publicada (`/app/`), así que los cambios llegan solos sin reinstalar.
- Se compilan solas en GitHub Actions (`.github/workflows/apps-moviles.yml`) cuando cambia la carpeta `movil/`, o a mano desde la pestaña *Actions*.
