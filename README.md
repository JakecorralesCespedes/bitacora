# Bitácora / Portafolio Realidad Nacional

Portafolio digital del curso **Realidad Nacional** (UNADECA) – Mayo/Agosto 2025.

Incluye:
- Evidencias semanales (semanas 1 a 15) con descripciones y reflexiones.
- Proyecto Integrador (salud mental) con secciones estructuradas.
- Repositorio de archivos PDF y audio.
- Galería fotográfica dinámica de la gira (carga automática 1..45 + carga manual persistente en el navegador con IndexedDB).

## Archivos Clave
| Archivo | Descripción |
|---------|-------------|
| `index.html` | Página principal (copia de `portafolio.html` para servir en GitHub Pages). |
| `portafolio.html` | Versión original de trabajo. |
| `*.pdf` | Evidencias/documentos de apoyo. |
| `Entrevista Intergeneracional.m4a` | Audio evidencia semana 13. |

## Persistencia de Imágenes (Galería)
Las imágenes cargadas manualmente (botón "Seleccionar") se comprimen (JPEG ~60% calidad, máx 1600px) y se guardan automáticamente en **IndexedDB** del navegador. Esto significa:
- Permanecen después de recargar la página en el mismo navegador/dispositivo.
- No se suben a GitHub (solo viven localmente).
- Botón "Limpiar" borra las imágenes guardadas localmente.

Si quieres que las fotos estén también en el repositorio (para que otros las vean):
1. Convierte HEIC a JPEG si aplica.
2. Nómbralas `1.jpeg`, `2.jpeg`, ..., `45.jpeg` (o al menos consecutivas empezando en 1).
3. Súbelas a esta carpeta y haz commit.

## Cómo Publicar en GitHub Pages
1. Activa GitHub Pages en el repositorio (Settings > Pages).
2. Selecciona la rama `main` y carpeta `/root`.
3. Guarda – la página quedará disponible como: `https://<usuario>.github.io/bitacora/` (o similar).

## Flujo de Trabajo Sugerido
1. Editar contenido en `portafolio.html`.
2. Probar en navegador local (abrir `index.html`).
3. Commit & push.

## Comandos (Referencia)
```bash
# Inicialización (ya realizada)
git init
git add .
git commit -m "Inicial: portafolio Realidad Nacional"

git branch -M main
git remote add origin https://github.com/JakecorralesCespedes/bitacora.git
git push -u origin main
```

## Notas Técnicas
- No requiere build: HTML/CSS/JS puro.
- IndexedDB almacena base64 de imágenes manuales; no impacta el repo.
- Para resetear la galería: usar botón "Limpiar" o borrar almacenamiento del sitio en herramientas del navegador.

## Próximas Mejores (Opcional)
- Exportar/Importar galería (JSON) para mover a otro dispositivo.
- Tema oscuro.
- Compresión adaptativa según tamaño original.

---
Hecho para fines académicos. 
