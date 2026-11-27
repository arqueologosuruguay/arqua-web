# Sitio web de Arqua

Sitio de la Asociación de Arqueología del Uruguay (Arqua). Está hecho con Jekyll y se publica gratis con GitHub Pages.

## Cómo cargar una novedad (sin saber programar)

1. Entrá a [app.pagescms.org](https://app.pagescms.org) y tocá **Sign in with GitHub**. Usá tu cuenta de GitHub (cada persona que edite necesita una cuenta gratis y que la cuenta de Arqua la invite como colaboradora del repositorio).
2. Elegí el repositorio **arqua-web**.
3. En el menú de la izquierda elegí **Novedades** y tocá **Add an entry**.
4. Completá título, fecha, tipo, imagen, resumen y texto, y tocá **Save**.
5. En uno o dos minutos la novedad aparece en el sitio.

Lo mismo sirve para **Declaraciones**, **Autoridades** y las **Páginas** de texto.

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

El sitio usa el dominio **arqua.com.uy** (archivo `CNAME` en la raíz del repositorio; en `_config.yml`, `url: "https://arqua.com.uy"` y `baseurl: ""`).

El DNS del dominio se administra en Cloudflare (el dominio está registrado en nic.uy):

- Cuatro registros **A** para `arqua.com.uy`: 185.199.108.153, 185.199.109.153, 185.199.110.153 y 185.199.111.153 (con la nube gris, «Solo DNS»).
- Un registro **CNAME** `www` → `arqueologosuruguay.github.io` (también «Solo DNS»).

En Settings → Pages tiene que figurar `arqua.com.uy` como Custom domain y estar marcado **Enforce HTTPS**.

## Probar en una computadora

```
gem install jekyll
jekyll serve
```
