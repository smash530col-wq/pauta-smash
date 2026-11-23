# Pauta y redes · SMASH

Informe diario de pauta y segmentación (Meta Ads + WhatsApp) y de redes (Metricool), con inicio de sesión.

- Página estática (`index.html`) publicada con GitHub Pages.
- Datos en Supabase (tabla `pauta_dias`), protegidos con inicio de sesión: solo el usuario autorizado puede leerlos.
- La clave que va en la página es la pública (publishable); quién lee qué lo decide la base de datos.
- Cada noche una tarea programada en el computador del negocio guarda el informe del día en Supabase.
