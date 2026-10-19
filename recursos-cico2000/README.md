# Recursos interactivos · CICO2000

Recursos interactivos (simulaciones, visualizadores, laboratorios guiados) de la asignatura **Análisis de Datos y Visualización (CICO2000)** – Ingeniería en Redes y Analítica de Datos, UTPL.

## Estructura

```
/
├── index.html                      ← catálogo de recursos (página de inicio)
├── README.md
└── recursos/
    ├── s4-consumo-apis/
    │   └── index.html              ← Misión API (Semana 4, apartado 2.2)
    └── sNN-nombre-del-recurso/     ← cada recurso nuevo en su propia carpeta
        └── index.html
```

Reglas para cada recurso:

- Un recurso = una carpeta con un `index.html` **autocontenido** (CSS, JS e imágenes incluidos o en la misma carpeta). No depende de servidores ni de bases de datos.
- Nombre de carpeta: `s<semana>-<tema-en-minusculas>` (p. ej., `s9-valores-nulos`).
- Al publicar un recurso nuevo, añadir su tarjeta en `index.html` (hay un comentario que indica dónde).

## Publicación con GitHub Pages (gratuito)

1. Cree un repositorio **público** en GitHub, por ejemplo `recursos-cico2000`.
2. Suba el contenido de esta carpeta (botón **Add file → Upload files**, o con Git).
3. En el repositorio: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, rama `main`, carpeta `/ (root)` → **Save**.
4. En 1–2 minutos el sitio queda en:
   - Catálogo: `https://<usuario>.github.io/recursos-cico2000/`
   - Recurso: `https://<usuario>.github.io/recursos-cico2000/recursos/s4-consumo-apis/`

> Alternativa equivalente: **GitLab Pages** (requiere un archivo `.gitlab-ci.yml` que copie el contenido a la carpeta `public`).

## Insertar el recurso en Canvas (EVA)

En una página, tarea o módulo de Canvas, abra el editor de contenido → **HTML** (`</>`) y pegue:

```html
<iframe src="https://<usuario>.github.io/recursos-cico2000/recursos/s4-consumo-apis/"
        title="Misión API – Consumo de datos mediante APIs"
        width="100%" height="760" style="border:0" allowfullscreen></iframe>
<p><a href="https://<usuario>.github.io/recursos-cico2000/recursos/s4-consumo-apis/" target="_blank">Abrir el recurso en una pestaña nueva</a></p>
```

También puede agregarlo como **URL externa** en un módulo (opción «Cargar en una nueva pestaña»).

## Actualizar un recurso

Reemplace el `index.html` de la carpeta del recurso y confirme el cambio (commit). La URL no cambia; los estudiantes ven la versión nueva al recargar.

## Configuración de «Misión API»

En `recursos/s4-consumo-apis/index.html`, busque la línea:

```js
const PRACTICA_URL = "#";
```

y reemplace `#` por el enlace al notebook práctico de la semana (Canvas, Colab, etc.). Es el destino del botón **Ir a la práctica**.
