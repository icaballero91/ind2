# Actualizar el sitio

El sitio entero vive en `index.html`. Para publicar una versión nueva basta con reemplazar ese archivo.

## Pasos

1. Reciba el nuevo `index.html` cifrado. El equipo que mantiene el sistema lo genera a partir del código fuente, que **no** se guarda en este repositorio.
2. En GitHub, abra `index.html` y pulse el ícono de lápiz → **…** → **Upload files**. También puede arrastrar el archivo nuevo a la página del repositorio.
3. Escriba un mensaje que diga qué cambió, por ejemplo `v10: metas de I.5 contra la banda natural`, y pulse **Commit changes**.
4. Si usa GitHub Actions, la publicación se hace sola en uno o dos minutos. Si usa la rama, también.
5. Abra el sitio y recargue sin caché (Ctrl + Shift + R, o Cmd + Shift + R en Mac).

## Cambiar la contraseña

La contraseña está dentro del cifrado de `index.html`, así que no se puede cambiar desde GitHub: hay que generar un `index.html` nuevo con la clave nueva y subirlo. La clave anterior deja de servir apenas se publica el archivo nuevo.

## Registro de versiones

Anote cada versión en el historial de commits. El registro detallado de cambios y verificaciones se lleva en el documento «Anexos · Registro de versiones y cambios del Sistema de Indicadores PFP Bolivia».

## Lo que no hay que hacer

- No subir el archivo sin cifrar, ni el código fuente o los datos, a un repositorio público.
- No escribir el usuario ni la contraseña en el README, en los commits ni en los *issues*.
