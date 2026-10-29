# Inventario de tienda (PWA) - archivos sin carpetas

Todos los archivos de este zip van sueltos en la raiz del repositorio (nada de carpetas):
index.html, manifest.webmanifest, sw.js, icon-192.png, icon-512.png, icon-maskable-512.png, _config.yml
(assetlinks-plantilla.json es solo un ejemplo, no hace falta subirlo).

## 1. Subir a GitHub
1. Repositorio publico llamado exactamente `TU-USUARIO.github.io`.
2. Add file > Upload files: arrastra los archivos del zip (descomprimido) y haz Commit.
3. Settings > Pages > Deploy from a branch > main / (root) > Save.

## 2. Crear assetlinks.json (esto es lo que quita la barra del navegador)
Debe estar en `.well-known/assetlinks.json`. Esa carpeta se crea escribiendo, no subiendo:
1. En el repositorio: Add file > Create new file.
2. En el cuadro del nombre escribe `.well-known/assetlinks.json` (al escribir la "/" GitHub crea la carpeta solo).
3. Pega dentro el contenido del `assetlinks.json` que te da PWABuilder (viene en el zip del APK). Si no, usa la plantilla cambiando `package_name` y la huella SHA-256 por las de tu APK.
4. Commit changes.
5. Comprueba que abre en el navegador: https://TU-USUARIO.github.io/.well-known/assetlinks.json
6. Desinstala la app, instala el APK de nuevo y abrela.

El archivo `_config.yml` hace que GitHub publique la carpeta `.well-known` (por defecto la ignora).

## Notas
- Si cambias index.html, cambia `inventario-v5` por `inventario-v13` en sw.js.
- Importar desde WhatsApp: Compartir el Excel > elegir "Inventario".
