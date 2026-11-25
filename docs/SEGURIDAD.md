# Seguridad del sitio

## Qué protege

- **El contenido viaja cifrado.** `index.html` contiene el sistema comprimido y cifrado con AES-GCM de 256 bits. La clave del contenido está envuelta con una clave derivada de la contraseña mediante PBKDF2-SHA-256 con 600.000 iteraciones y sal aleatoria.
- **Nada legible en el repositorio.** Sin la contraseña, el archivo solo muestra la pantalla de ingreso; ni las cifras ni los textos de los indicadores se pueden leer en el código.
- **Descifrado local.** El descifrado ocurre en el navegador de quien ingresa. No se envía la contraseña a ningún servidor.
- **Sin indexación.** `robots.txt` y la etiqueta `noindex` piden a los buscadores no indexar el sitio.

## Qué no protege

- **Quien conoce la contraseña puede ver y copiar todo.** Compártala solo con el equipo autorizado y cámbiela si alguien deja el equipo (ver `ACTUALIZAR.md`).
- **Una contraseña corta se puede adivinar** con suficiente tiempo de cálculo. Las 600.000 iteraciones vuelven lento cada intento, pero conviene usar una contraseña larga.
- **La pantalla de ingreso es pública.** Su texto de presentación (título, número de áreas e indicadores, horizonte del Plan) se ve sin clave.
- **La sesión se recuerda en la pestaña** si se marca «Mantener la sesión en esta pestaña». En equipos compartidos, cierre la pestaña al terminar.

## Recomendaciones

1. Repositorio **privado** si el plan de GitHub lo permite.
2. Contraseña de al menos 12 caracteres, entregada por un canal distinto al enlace.
3. Cambio de contraseña al cierre de cada fase del programa o cuando cambie el equipo.
