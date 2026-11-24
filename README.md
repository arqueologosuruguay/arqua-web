# Sitio web de Arqua

Sitio de la Asociación de Arqueología del Uruguay (Arqua). Está hecho con Jekyll y se publica gratis con GitHub Pages.

## Cómo cargar una novedad (sin saber programar)

1. Entrá a [app.pagescms.org](https://app.pagescms.org) y tocá **Sign in with GitHub**. Usá tu cuenta de GitHub (cada persona que edite necesita una cuenta gratis y que la cuenta de Arqua la invite como colaboradora del repositorio).
2. Elegí el repositorio **arqua-web**.
3. En el menú de la izquierda elegí **Novedades** y tocá **Add an entry**.
4. Completá título, fecha, tipo, imagen, resumen y texto, y tocá **Save**.
5. En uno o dos minutos la novedad aparece en el sitio.

Lo mismo sirve para **Declaraciones**, **Autoridades** y las **Páginas** de texto.

Para que una novedad deje de aparecer en el inicio y pase al archivo, marcá **Pasar al archivo**.

## Dónde está cada cosa

| Qué | Dónde |
|---|---|
| Novedades | `_novedades/` |
| Declaraciones | `_declaraciones/` |
| Autoridades | `_data/autoridades.yml` |
| Inicio | `index.html` |
| Páginas de texto | `asociate.md`, `contacto.md`, `institucional/` |
| Fotos y PDF | `assets/img/` y `assets/pdf/` |
| Colores y estilos | `assets/css/main.css` |
| Datos generales (correos, redes) | `_config.yml` |

## Publicación

GitHub Pages arma el sitio solo a partir de la rama `main` (Settings → Pages → Deploy from a branch → `main` / root).

Para usar el dominio **arqua.com.uy**:

1. En `_config.yml`, cambiar `baseurl` a `""` y `url` a `"https://arqua.com.uy"`.
2. En Settings → Pages → Custom domain, escribir `arqua.com.uy`.
3. En el proveedor del dominio, crear los registros DNS que indica GitHub (registros A a las IP de GitHub Pages y un CNAME `www` a `arqueologosuruguay.github.io`).

## Probar en una computadora

```
gem install jekyll
jekyll serve
```
