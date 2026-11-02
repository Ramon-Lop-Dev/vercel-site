# Despliegue de SOLUNEXO en Vercel

Esta carpeta contiene una copia lista para desplegar del sitio estático: `index.html`, `assets/`, `robots.txt` y `sitemap.xml`. No requiere instalación de dependencias ni comando de compilación.

## Publicar desde GitHub

1. Sube el repositorio a GitHub, incluyendo esta carpeta `vercel-site/`.
2. En Vercel, importa ese repositorio y configura **Root Directory** como `vercel-site`.
3. Selecciona **Other** como framework. Deja vacíos el comando de compilación y el directorio de salida; no se necesita build.
4. Después del despliegue, prueba la página y verifica que carguen `/robots.txt`, `/sitemap.xml` y los recursos de `/assets/`.
5. En Vercel, agrega el dominio definitivo del negocio y completa los registros DNS indicados por Vercel.
6. Cuando el dominio esté activo, verifica en Google Search Console la propiedad del dominio y envía `https://solunexo.com/sitemap.xml` (actualiza esa dirección si el dominio definitivo es otro).

## Revisión obligatoria antes de publicar

El HTML y los archivos SEO actuales usan `https://solunexo.com/` como dominio canónico. Confirma que ese sea el dominio real y que esté conectado a Vercel. Si usarás otro dominio, cambia el dominio en `index.html` (canonical, Open Graph, Twitter y JSON-LD), `robots.txt` y `sitemap.xml` antes de enviar el sitio a Google. No dejes ambos dominios indexables como versiones independientes.

Confirma también que teléfono, horarios, precios, ubicación y demás datos comerciales del HTML sean actuales. El SEO técnico facilita el rastreo, pero no garantiza posiciones ni inclusión inmediata en Google.

## Actualizar el sitio

Haz los cambios de contenido en el `index.html` de esta carpeta y actualiza `sitemap.xml` cuando cambie la página, incluyendo la fecha real de modificación en `lastmod`. Mantén `assets/`, `robots.txt` y `sitemap.xml` dentro de esta carpeta: Vercel desplegará `vercel-site/` como raíz pública.
