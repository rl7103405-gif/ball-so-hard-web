# 🏀 Ball So Hard — página web (borrador para presentar)

Sitio de una sola página para **Ball So Hard**, equipo profesional de baloncesto 3x3
de Puebla y su academia **Ball So Hard Development** (6 a 17 años).

> ⚠️ **Esto es un borrador hecho sin material del cliente.** Los textos salen de
> prensa pública, del perfil `@ballsohard_dev` y del sitio de la FIBA. Antes de
> enseñarlo hay que sustituir las fotos y confirmar los datos marcados en amarillo
> dentro de la página (`POR CONFIRMAR`).

## Estado

Marcado como **muestra no oficial**: banda amarilla arriba y `noindex` para que
Google no lo liste. Ver `PASOS.md` para publicarlo y para quitar ambas cosas
cuando el cliente autorice.

## Cómo verlo

Abre `index.html` con doble clic. No hay que instalar nada — es HTML, CSS y JS puros,
sin frameworks ni dependencias.

## Lo que falta (pedirlo al cliente)

| Qué | Dónde va |
|---|---|
| Logo en PNG con fondo transparente | `assets/logo-ballsohard.png` y `assets/logo-icono.png` |
| Foto de portada (equipo en cancha, horizontal) | `assets/hero.jpg` |
| Foto para la sección "Quiénes somos" | `assets/equipo.jpg` |
| 10–20 fotos buenas para la galería | `assets/galeria/` + agregarlas a la lista `FOTOS` al final de `index.html` |
| **Horarios y costos** de la academia | Sección Academia (hoy dice `POR CONFIRMAR`) |
| Correo de contacto | Sección Contacto |
| Resultado del nacional de Oaxtepec (mayo 2026) | Sección Palmarés |
| Retratos de Yannick, Daniel y la coach Zury | Sección Equipo (hoy son iniciales) |

**Importante:** las fotos deben ser del cliente o con su permiso. Las que están en
Instagram y en las notas de prensa no se pueden usar sin autorización.

## Datos que ya están puestos y de dónde salieron

- **Fundación 2021**, por Yannick Espinosa y Daniel Montiel — entrevista en Grada (2023).
- **Palmarés** — Grada, El Sol de Puebla, El Heraldo de Puebla y la bio de `@ballsohard_dev`.
- **FIBA Open Puebla 2026**: 231 equipos, final 9-7 sobre Dame Dolla, cuatro títulos.
- **Sede de la academia**: Polideportivo Flor del Bosque, Gral. Juan N. Méndez #142,
  San Bernardino Tlaxcalancingo, Puebla.
- **WhatsApp 222 116 8221** — aparece en el flyer público del Hoop It Up.
  Confirmar que es el número al que quieren recibir mensajes del sitio.

## Cómo cambiar la identidad visual

Todo el color y la tipografía viven en las variables `:root` al inicio de `index.html`.
Cambiar esas diez líneas cambia el sitio completo:

```css
--verde: #A3FF12;      /* el verde neón del logo */
--negro: #08090A;      /* fondo */
--fuente-display: 'Archivo Black', Impact, sans-serif;
--fuente-cuerpo: 'Barlow', 'Helvetica Neue', Arial, sans-serif;
```

## Cómo agregar fotos a la galería

1. Copia los archivos a `assets/galeria/`.
2. Agrega el nombre de cada uno a la lista `FOTOS`, al final de `index.html`.
3. Nómbralos con palabras separadas por guiones (`campeon-fiba-open-2026.jpg`):
   ese nombre se usa como descripción de la foto.

## Fases siguientes (si el cliente compra)

1. **Publicar** en GitHub Pages (gratis, con HTTPS).
2. **Portal privado** para el equipo — avisos, entrenamientos, asistencia.
3. **Editor de contenido** para que la academia cambie textos y fotos sin tocar código.
4. **Firebase** cuando haya usuarios y datos reales.

El plano completo de esas fases está en `GUIA-REPLICAR.md` del proyecto de
Jaguares NZ, que es de donde sale la estructura de este sitio.

## Verificado

Probado con Playwright en 1280 px y 390 px: sin errores de JavaScript en consola,
sin scroll horizontal, las 35 animaciones de aparición funcionan, el mapa carga y el
formulario arma el mensaje de WhatsApp. Los únicos errores de consola son los 404 de
las imágenes que todavía no existen — desaparecen al subir los archivos.
