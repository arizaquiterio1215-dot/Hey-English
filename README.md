# Hey! English · Learn. Play. Speak.

PWA personal para estudiar inglés estadounidense desde un iPhone, desarrollada con HTML, CSS y JavaScript sin frameworks, servicios de pago ni claves API.

## Funciones reales de esta entrega (v2.0)

- Evaluación diagnóstica orientativa de 12 preguntas (A1–B1).
- Ruta A1–C2 visible, **8 lecciones completas** de A1, A2 y B1, con 40 expresiones, 24 preguntas, ejemplos y consejos pedagógicos.
- Audio por síntesis de voz `speechSynthesis` configurada para `en-US` y velocidad reducida opcional. La disponibilidad de voces y el modo sin conexión dependen de Safari/iOS.
- Tres juegos funcionales: parejas, identificar imágenes con emoji y ordenar oraciones.
- Seis cuentos originales con lectura por frase y completa, vocabulario y pregunta de comprensión.
- Cuatro escenarios de conversación ramificada con Alex, con reproducción de audio.
- Grabación de voz opcional para autoescucha mediante `MediaRecorder`, si Safari ofrece permiso y soporte. **No evalúa automáticamente la pronunciación.**
- Recomendaciones culturales por nivel; no se alojan ni reproducen películas o canciones.
- Seguimiento local de clases, cuentos, conversaciones, juegos y días practicados. Exportación/importación de copia JSON.
- Service worker con caché para interfaz y contenido estático. Los archivos pueden funcionar sin conexión tras la primera carga y almacenamiento correctos. El audio y el micrófono no se garantizan offline.

## Archivos

```
Hey_English_PWA/
  index.html
  manifest.webmanifest
  service-worker.js
  css/styles.css
  js/content.js
  js/app.js
  assets/icon-192.png
  assets/icon-512.png
  README.md
```

## Probar en Visual Studio Code

1. Descomprime el ZIP y abre la carpeta `Hey_English_PWA` en Visual Studio Code.
2. Instala la extensión gratuita **Live Server**, o usa `python -m http.server 5500` desde la carpeta.
3. Abre la dirección local en el navegador y prueba diagnóstico, lecciones, juegos, cuentos y chat.
4. Para probar en el iPhone, publica **el contenido de esta carpeta** en un sitio HTTPS como GitHub Pages.

## Publicar gratis con GitHub Pages

1. Crea un repositorio **público** en GitHub, por ejemplo `hey-english`.
2. Sube todos los archivos y carpetas de este proyecto a la **raíz** del repositorio (no el ZIP).
3. En `Settings → Pages → Build and deployment`, elige `Deploy from a branch`, rama `main`, carpeta `/ (root)`.
4. Espera a que se publique `https://TU_USUARIO.github.io/hey-english/`.
5. En el iPhone, abre esa dirección en **Safari**, usa Compartir → **Agregar a Inicio** y, si aparece, **Abrir como app web**.
6. Abre Hey! English desde el ícono de la pantalla de inicio. Conéctate a internet al menos la primera vez para permitir que se guarden los recursos.

## Importante sobre privacidad y limitaciones

- La app no solicita cuenta ni envía progreso a un servidor; utiliza `localStorage` en el navegador. Exporta copias periódicas desde Perfil.
- GitHub Pages para repositorios públicos deja el código y el contenido visibles. No guardes contraseñas, secretos ni datos sensibles en el proyecto.
- La evaluación inicial es orientativa, no certifica un nivel MCER.
- Los niveles B2–C2 están diseñados en la ruta, pero aún no contienen lecciones. A1–B1 tienen contenido inicial, **no currículos completos de esos niveles**.
- El mentor Alex usa diálogos prediseñados, no IA. No entiende texto libre ni corrige espontáneamente mensajes.
- La grabación de voz no analiza ni puntúa pronunciación; permite autoescucha únicamente. El permiso de micrófono requiere HTTPS y compatibilidad del dispositivo.
- No se requiere suscripción ni API de pago. La publicación es gratuita dentro de las condiciones de GitHub Pages.
- Si cambias el código, el service worker puede tardar una recarga en mostrar los archivos actualizados; actualiza el nombre de CACHE para nuevas versiones.

## Cómo ampliar

- Nuevas clases: agrega objetos a `HEY_DATA.lessons` en `js/content.js`.
- Nuevos cuentos: agrega objetos a `HEY_DATA.stories`.
- Nuevos diálogos: agrega nodos en `HEY_DATA.chats`.
- Estilos y paleta: `css/styles.css` (variables `:root`).

Contenido de práctica redactado para esta app. Las recomendaciones de obras son referencias educativas y no implican afiliación con sus titulares.
