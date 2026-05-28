# Guía: Cómo configurar Google Search Console y SEO

Esta guía es un recordatorio paso a paso de lo que hicimos para conectar la página a Google. Úsala cuando tengas que hacer el proyecto oficial con su dominio real.

## Paso 1: Preparar el Código

Antes de ir a Google, la página debe tener la información lista para que los robots la lean.

1. **Etiquetas SEO (Meta Tags):** 
   En tu archivo `index.html`, dentro de la etiqueta `<head>`, debes tener las descripciones de la página:
   ```html
   <meta name="description" content="Descripción corta de tu negocio">
   <meta name="keywords" content="palabra1, palabra2, palabra3">
   ```
2. **Archivo robots.txt:**
   Debes crear un archivo llamado `robots.txt` en la misma carpeta que tu `index.html` con este texto para darle permiso a Google de leer todo:
   ```txt
   User-agent: *
   Allow: /
   ```
3. Sube todos estos cambios a Vercel usando `git push`.

## Paso 2: Registrarse en Google Search Console

1. Entra a [Google Search Console](https://search.google.com/search-console/about) con una cuenta de Gmail.
2. Si es la primera vez, verás una pantalla para "Añadir propiedad".
3. Busca el cuadro de la derecha que dice **"Prefijo de la URL"**.
4. Pega la URL exacta de tu página (ejemplo: `https://www.midominio.com/`) y dale a "Continuar".

## Paso 3: Verificar la Propiedad (La Etiqueta HTML)

Google necesita comprobar que la página es tuya.

1. Te saldrá una ventana con métodos de verificación. Ve hacia abajo y haz clic en **"Etiqueta HTML"**.
2. Copia el código que te da (se parece a esto: `<meta name="google-site-verification" content="..." />`).
3. Ve a tu código local y pega esa etiqueta dentro del `<head>` de tu `index.html`.
4. Guarda y vuelve a subir los cambios a Vercel (`git add .`, `git commit...`, `git push`).
5. Vuelve a Google y haz clic en el botón **"Verificar"**. Debería salirte un mensaje verde de éxito.

## Paso 4: Solicitar Indexación (Forzar a Google)

Una vez verificado, entraste al panel de control de tu página en Google.

1. En la parte superior hay una barra buscadora que dice *"Inspeccionar las URL de..."*.
2. Escribe ahí la URL de tu página y presiona Enter.
3. Te dirá *"La URL no está en Google"*.
4. Haz clic en el botón gris **"SOLICITAR INDEXACIÓN"**.
5. ¡Y listo! Si te sale el error de "Cuota Superada", no pasa nada, ya estás verificado y Google pasará a leerte por su cuenta en los próximos días.
