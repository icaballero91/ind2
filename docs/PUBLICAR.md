# Publicar el sitio en GitHub Pages

Hay dos caminos. Ambos dejan el sitio en `https://<usuario-u-organización>.github.io/<repositorio>/`.

## 1. Crear el repositorio

1. Entre a GitHub y pulse **New repository**.
2. Nombre sugerido: `pfp-sistema-indicadores`.
3. Visibilidad:
   - **Privado**: solo quienes usted invite ven el repositorio. Para publicar un sitio desde un repositorio privado, GitHub exige un plan de pago (Pro, Team o Enterprise).
   - **Público**: cualquiera ve los archivos, pero el contenido sigue cifrado dentro de `index.html`.
4. No marque «Add a README»: el README ya viene en esta carpeta.

## 2. Subir los archivos

**Desde el navegador**

1. En el repositorio vacío, pulse **uploading an existing file**.
2. Arrastre **todo el contenido** de la carpeta `pfp-sistema-indicadores`.
3. Verifique que estén `.nojekyll` y la carpeta `.github`. Algunos sistemas ocultan los archivos que empiezan con punto: active «mostrar archivos ocultos» antes de arrastrarlos.
4. Pulse **Commit changes**.

**Con git**

```bash
cd pfp-sistema-indicadores
git init -b main
git add .
git commit -m "Sistema de indicadores PFP Bolivia"
git remote add origin https://github.com/<usuario-u-organización>/pfp-sistema-indicadores.git
git push -u origin main
```

## 3. Activar GitHub Pages

### Opción A: con GitHub Actions (recomendada)

1. En el repositorio, vaya a **Settings → Pages**.
2. En **Build and deployment → Source**, elija **GitHub Actions**.
3. Vaya a la pestaña **Actions**. La acción «Publicar en GitHub Pages» corre sola con cada cambio en `main`. Si no arrancó, ábrala y pulse **Run workflow**.
4. Cuando termine (marca verde), el enlace aparece en **Settings → Pages**.

### Opción B: desde la rama, sin acciones

1. En **Settings → Pages → Source**, elija **Deploy from a branch**.
2. Rama `main`, carpeta `/ (root)`. Pulse **Save**.
3. En uno o dos minutos aparece el enlace.

Si usa la opción B, puede borrar la carpeta `.github`.

## 4. Comprobar

1. Abra el enlace: debe aparecer la pantalla «Iniciar sesión».
2. Ingrese con el usuario y la contraseña entregados por el programa.
3. Revise la portada, un indicador y la página «Ruta y calendario».

## Dominio propio (opcional)

En **Settings → Pages → Custom domain**, escriba el dominio (por ejemplo, `indicadores.ejemplo.org`). Luego, en el proveedor del dominio, cree un registro `CNAME` que apunte a `<usuario-u-organización>.github.io`. Active **Enforce HTTPS** cuando GitHub lo permita.

## Problemas frecuentes

| Síntoma | Causa probable | Solución |
|---|---|---|
| Error 404 al abrir el enlace | Pages no está activado o aún no termina | Revise **Settings → Pages** y la pestaña **Actions** |
| La acción falla con «Pages not enabled» | Falta elegir **GitHub Actions** como fuente | Paso 3, opción A |
| La pantalla de ingreso no acepta la clave | Usuario o contraseña mal escritos | Escríbalos sin espacios; mayúsculas y minúsculas dan igual |
| El sitio se ve sin estilos | El archivo se subió dañado o incompleto | Vuelva a subir `index.html` (debe pesar unos 650 KB) |
