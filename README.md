# Numerín

App de matemáticas para niños con discalculia (de 3º de Primaria a 2º de ESO):
foto del ejercicio explicada con dibujos paso a paso, exámenes por curso, premios,
historial y repasos que mezclan lo que se ha fallado.

Usa la IA gratuita de Google (Gemini). Todo el progreso se guarda en el propio dispositivo.

## Archivos

| Archivo | Para qué sirve |
|---|---|
| `index.html` | La app entera |
| `manifest.webmanifest` | Nombre, colores e iconos para poder instalarla |
| `sw.js` | Hace que abra sin internet (los exámenes funcionan offline) |
| `icon-192.png`, `icon-512.png`, `icon-maskable-512.png`, `apple-touch-icon.png` | Iconos |
| `.nojekyll` | Le dice a GitHub que publique los archivos tal cual |

## 1. Subirla a GitHub (una vez)

1. Crea una cuenta gratis en https://github.com (si no la tienes).
2. Pulsa **New repository** (botón verde o el `+` de arriba a la derecha).
   - Nombre: `numerin`
   - Marca **Public**.
   - Pulsa **Create repository**.
3. En la página del repositorio pulsa **uploading an existing file**
   (o **Add file → Upload files**).
4. Arrastra **todos los archivos de esta carpeta** (también `.nojekyll`; si tu ordenador
   lo oculta, no pasa nada, la app funciona sin él).
5. Abajo pulsa **Commit changes**.

## 2. Publicarla con GitHub Pages

1. En el repositorio: **Settings → Pages**.
2. En **Source** elige **Deploy from a branch**.
3. Branch: **main** y carpeta **/ (root)**. Pulsa **Save**.
4. Espera 1-2 minutos y recarga. Aparecerá la dirección, del estilo:
   `https://TU-USUARIO.github.io/numerin/`

Esa es la dirección que se manda por WhatsApp.

## 3. Instalarla como app

- **Android (Chrome):** abre la dirección → menú ⋮ → **Instalar app** (o **Añadir a pantalla de inicio**).
  También puede salir el botón **Instalar app** arriba, dentro de Numerín.
- **iPhone / iPad (Safari):** abre la dirección → botón **Compartir** → **Añadir a pantalla de inicio**.

Se queda con su icono, se abre a pantalla completa y funciona sin internet
(menos la parte de leer fotos, que necesita conexión).

## 4. Conseguir la clave gratis de Google

1. Abre https://aistudio.google.com/apikey con una cuenta de Google.
2. Pulsa **Create API key** (Crear clave de API).
3. Copia la clave (empieza por `AIza`).
4. En Numerín: toca el nombre de arriba → **Ajustes para mayores** → pega la clave →
   **Guardar y probar**. Debe salir «✓ Conectado con Google».

La clave se guarda solo en ese dispositivo. Hay que ponerla en cada móvil o tablet donde se use.

Límites del plan gratuito: hay un número de usos al día. Si se acaban, la app prueba sola
con el modelo Flash-Lite, que tiene más usos gratis. Con la clave gratuita, Google puede usar
lo que se envía para mejorar sus productos.

## 5. Actualizar la app más adelante

1. En el repositorio: **Add file → Upload files** → sube el `index.html` nuevo → **Commit changes**.
2. Si cambias algo de peso, abre `sw.js` y sube el número de `numerin-v1` a `numerin-v2`
   para que los móviles descarguen la versión nueva.

El progreso de la niña no se pierde al actualizar: está guardado en su dispositivo.

## 6. Pasar el progreso a otro dispositivo

En Numerín → nombre de arriba → **Descargar copia**. En el otro dispositivo → **Cargar copia**.

## Extra: convertirla en APK (Android) o subirla a Google Play

Con la app ya publicada en GitHub Pages:

1. Abre https://www.pwabuilder.com
2. Pega la dirección `https://TU-USUARIO.github.io/numerin/` y pulsa **Start**.
3. Elige **Android → Generate Package**. Te da un APK para instalar directamente
   y el paquete para Google Play (subirla a Play requiere una cuenta de desarrollador de pago).
