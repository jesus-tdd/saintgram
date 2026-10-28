# Perfil tipo red social para catequesis

Web estática (HTML + CSS + JS, sin dependencias). Los datos reales van en `data.json` y `datos/<id>.json`.

## Estructura
```
index.html
perfiles.json      <- lista de perfiles de la página de inicio
data.json          <- solo se usa si no existe perfiles.json
datos/
  ejemplo.json
  perfil-uno.json
  perfil-dos.json
img/
  ejemplo/
    perfil.svg
    1.svg
    2.svg
```
Para cada perfil nuevo: crea `datos/<id>.json` (id en minúsculas, números y guiones) y una carpeta `img/<id>/`.
Se abre con `https://TU-USUARIO.github.io/TU-REPO/?santo=<id>`.

## Nombre de usuario (opcional)
Cada perfil puede llevar `"usuario": "san_ejemplo"` (con o sin @). Se muestra como `@san_ejemplo`
en la cabecera, en cada publicación y en la lista. Si no se pone, se usa el nombre.

## Página de inicio
Al entrar sin `?santo=` se muestra la lista de `perfiles.json`:
`{ "titulo": "Perfiles", "perfiles": ["ejemplo", "perfil-uno"] }`
Cada id debe tener su `datos/<id>.json`. Para añadir un perfil, súmalo a esa lista.

## Probar en local
Dentro de la carpeta, en una terminal: `python3 -m http.server 8000` (en Windows: `py -m http.server 8000`)
y abre http://localhost:8000/ o http://localhost:8000/?santo=ejemplo
