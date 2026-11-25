# Sistema de indicadores · PFP Bolivia

Sitio web del **Sistema de indicadores de impacto** del Plan de Conservación y de Desarrollo Comunitario para las Áreas Protegidas Nacionales (Programa de Financiamiento para la Permanencia, PFP Bolivia).

El sitio reúne los 12 indicadores de impacto del Plan en 5 ejes, con su línea base, metas a los años 6, 10 y 15 (2033, 2037 y 2042), gráficos por área protegida, riesgos, tareas pendientes y la ruta de actividades.

> **Acceso restringido.** Todo el contenido está cifrado dentro de `index.html`. Para verlo se necesita usuario y contraseña, que se entregan por un canal separado y **no deben escribirse en este repositorio**.

---

## Contenido del repositorio

| Archivo | Para qué sirve |
|---|---|
| `index.html` | El sitio completo en un solo archivo, cifrado (AES-GCM 256 + PBKDF2 de 600.000 iteraciones). Muestra la pantalla de ingreso y, con la clave correcta, abre el sistema. |
| `.nojekyll` | Indica a GitHub Pages que publique los archivos tal cual, sin procesarlos. |
| `robots.txt` | Pide a los buscadores que no indexen el sitio. |
| `.github/workflows/pages.yml` | Publica el sitio en GitHub Pages cada vez que se sube un cambio a la rama `main` (opcional). |
| `docs/PUBLICAR.md` | Paso a paso para subir y publicar el sitio. |
| `docs/ACTUALIZAR.md` | Cómo reemplazar el sitio por una versión nueva. |
| `docs/SEGURIDAD.md` | Qué protege el cifrado y qué no. |
| `docs/USO.md` | Guía rápida para navegar el sitio. |

## Publicación rápida

1. Cree un repositorio en GitHub (por ejemplo, `pfp-sistema-indicadores`).
2. Suba todos los archivos de esta carpeta, **incluidos** `.nojekyll` y la carpeta `.github`.
3. En el repositorio, vaya a **Settings → Pages**, elija **Source: GitHub Actions** y espere a que termine la acción «Publicar en GitHub Pages».
4. El sitio quedará en `https://<usuario-u-organización>.github.io/pfp-sistema-indicadores/`.

El detalle, con la alternativa sin acciones, está en [`docs/PUBLICAR.md`](docs/PUBLICAR.md).

## Qué contiene el sitio

- **Portada**: los 5 ejes, el estado del punto de partida de los 12 indicadores y cifras de contexto.
- **Una página por indicador**, con su nombre oficial según la ficha del Plan y 11 secciones que se pueden mostrar u ocultar:
  1. ¿Qué mide y por qué?
  2. ¿Cómo se calcula? (fórmula escrita en palabras, con cada término explicado)
  3. ¿Cómo se mide?
  4. ¿Desde dónde partimos? (mapa y gráficos cruzados por área)
  5. ¿A dónde vamos y cómo?
  6. ¿Cuándo y quién mide?
  7. ¿Qué puede fallar?
  8. Lo que falta y cómo mejorar
  9. Análisis resumen
  10. Aportes del equipo
  11. Decisión
- **Conclusiones**: preparación de cada indicador para congelar la línea base.
- **Ruta y calendario**: diagrama de Gantt por cadena de resultados (eje → indicador → resultado → actividad).
- **Lo que necesitamos**: tareas pendientes agrupadas por indicador.
- **Fuentes y créditos**.

Tiene tema claro y oscuro, y funciona en computadora y celular.

## Decisiones por indicador

La sección «Decisión» de cada indicador guarda lo que se escribe:

- **En claude.ai**, donde se publicó originalmente, se guarda en una base compartida por todo el equipo.
- **En GitHub Pages**, no hay base compartida: se guarda solo en el navegador de cada persona. El botón «Copiar» permite pasar el texto a un correo o documento.

## Requisitos

Ninguno del lado del servidor: es un archivo estático. Necesita un navegador actualizado (Chrome, Edge, Firefox o Safari recientes) y conexión a internet para cargar las tipografías de Google Fonts. Sin conexión se ve con las tipografías del sistema.

## Fuentes de datos

Las cifras provienen de fuentes oficiales y publicadas: SIMB–DGGyDF, SERNAP, MapBiomas Bolivia, INE (Censo 2024), APMT, NDC de Bolivia, Free-Flowing Rivers, UICN y otras. La lista completa, con año de cada fuente, está dentro del sitio, en «Fuentes y créditos».

## Licencia y uso

Material de trabajo del PFP Bolivia. El repositorio no declara una licencia abierta: su reutilización requiere autorización del programa. Las fotografías de especies conservan su licencia original (CC0, CC BY o CC BY-NC), indicada en el sitio.
