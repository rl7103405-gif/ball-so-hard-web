# Pasos para publicar y presentar

El proyecto ya tiene su commit hecho en local. Falta el repositorio en GitHub,
que sí o sí lo tienes que crear tú (no hay `gh` instalado en esta máquina y yo no
puedo entrar a tu cuenta).

## 1. Crear el repositorio (2 minutos)

1. Entra a <https://github.com/new>
2. **Repository name:** `ball-so-hard-web`
3. Déjalo **Public** — GitHub Pages gratis solo funciona con repos públicos.
4. **NO** marques "Add a README file" (ya hay uno).
5. Clic en **Create repository**.

## 2. Subirlo

Copia y pega esto en la terminal, dentro de `Desktop\ball-so-hard`
(cambia `TU-USUARIO` por tu usuario de GitHub, que en el otro proyecto es
`rl7103405-gif`):

```bash
git remote add origin https://github.com/TU-USUARIO/ball-so-hard-web.git
git branch -M main
git push -u origin main
```

## 3. Encender la página

1. En el repo: **Settings → Pages**
2. **Source:** Deploy from a branch
3. **Branch:** `main` · carpeta `/ (root)` → **Save**
4. En uno o dos minutos queda en:
   `https://TU-USUARIO.github.io/ball-so-hard-web/`

Si el despliegue se queda encolado mucho rato y te llega un correo de "some jobs
were not successful", no es tu código: haz cualquier commit nuevo y se destraba.

## 4. Cómo presentarla

Mándale el link por WhatsApp a Yannick y que la abra en el celular. Eso es la
presentación — no hace falta un PowerPoint.

Tres cosas que conviene decir al enseñarla:

- **Es una muestra, no está publicada como su sitio oficial.** Por eso la banda
  amarilla de arriba y por eso Google no la indexa todavía.
- **Los textos salen de sus propias notas de prensa y de su Instagram.** Si algo
  está mal, se corrige.
- **Falta su material:** logo, fotos, horarios y costos. Con eso el sitio queda
  terminado.

## 5. Cuando digan que sí

Se quitan dos cosas del `index.html`:

1. El `<div class="banda-muestra">` y sus reglas CSS (están marcadas con un
   comentario que dice qué borrar).
2. La línea `<meta name="robots" content="noindex, nofollow">`, para que Google
   empiece a indexarlo.

Y de ahí siguen las fases del `GUIA-REPLICAR.md` de Jaguares: portal privado,
editor de contenido y Firebase.
