# Cómo publicar un sitio web estático en GitHub

Pasos para publicar un sitio web estático con GitHub Pages y vincularlo a un proveedor de DNS.

### 1. Crear un respositorio

El primer paso es crear un repositorio para el sitio web que queremos publicar.

### 2. Subir el código

El fichero HTML con nombre `index.html` se publicará como la página de inicio (o página por defecto). Si no existe el fichero `index.html`, buscará el fichero `README.md` y se renderizará y publicará el fichero Markdown como página de inicio.

### 3. Publicar el repositorio mediante GitHub Pages

Pulsar en la pestaña `Settings`, bajar hasta la sección `GitHub Pages` y seleccionar `master branch`.

### 4. Ir al sitio web

Unos 15 ó 20 segundos después podremos acceder al sitio web publicado.

El sitio se publicará en la dirección [https://<github.username>.github.io/<repo.name>](https://<github.username>.github.io/<repo.name>), donde `github.username` será nuestro usuario de GitHub y `repo.name` el nombre del repositorio (en mi caso es [https://fvarrui.github.io/website-demo/](https://fvarrui.github.io/website-demo/)).

> Enlace a la plantilla HTML utilizada como ejemplo: [Ziggy](https://www.free-css.com/free-css-templates/page244/ziggy).

### 5. Añadir el fichero CNAME el repositorio de GitHub

Para poder vincular nuestro nuevo sitio web con nuestro nombre de dominio (por ejemplo: `fvarrui.es`) tendremos que crear en el repositorio el fichero `CNAME` (sin extensión) y añadirle una línea con el nombre de dominio.

En mi caso, el fichero `CNAME` tendrá el siguiente contenido:

```
fvarrui.es
```

### 6. Añadir los registros A mediante nuestro proveedor de DNS

Este paso (añadir registros A) se hará en el lado del proveedor de DNS.

Tendremos que crear un registro `ALIAS` o `ANAME`, o simplemente, un registro `A` que apunte a la dirección IP (o dominio) del servidor de GitHub Pages.

Todo lo que necesitamos es encontrar una sección en el sitio web de nuestro proveedor de nombre de dominio donde añadir los registros `A`, y a continuación añadimos las siguientes direcciones IP:

```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

Para más información consulta el siguiente [enlace](https://help.github.com/articles/setting-up-an-apex-domain/#configuring-a-records-with-your-dns-provider).
