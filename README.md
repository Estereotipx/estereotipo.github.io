\# Crea tu sitio web Refracta a partir de una colección de Zotero en 10 sencillos pasos

1\. **Comprueba que cumples los requisitos**

- Una [cuenta de Zotero](https://www.zotero.org/user/register/?utm_source=chatgpt.com)
- Una [cuenta de GitHub](https://github.com/signup?utm_source=chatgpt.com)

2\. **Prepara los campos de Zotero** para un sitio web Refracta. Los elementos de Refracta se añaden del mismo modo que cualquier otro elemento en una [biblioteca de Zotero](https://www.zotero.org/support/adding_items_to_zotero). Solo ten en cuenta:

- **El campo URL:** corresponde a la dirección donde está alojado el archivo en máxima resolución (Wikimedia Commons, Archive.org, u otro repositorio).
- **Imagen visible en la página:** es un archivo JPG de baja o mediana resolución que se añade como `attachment` al elemento de Zotero (consulta la [documentación](https://www.zotero.org/support/attaching_files?utm_source=chatgpt.com) sobre los archivos adjuntos de Zotero).

3\. **[Haz un fork](https://github.com/morelrep/morel-no-code-generator/fork?utm_source=chatgpt.com) de este repositorio**, es decir, [crea una copia](https://github.com/morelrep/morel-no-code-generator/fork?utm_source=chatgpt.com) en tu cuenta de [GitHub](https://github.com?utm_source=chatgpt.com).

4\. **Ve a la pestaña&#x20;**`actions` y habilita los flujos de trabajo (*workflows*).

5\. **Abre el archivo&#x20;**`_config.yml` y modifica los siguientes campos:

- El `title` con el título de tu sitio.
- El `tagline` con el lema de tu sitio.
- El `email` y/o las cuentas de redes sociales con los de tu sitio.
- El enlace `jotform` (crea una cuenta gratuita en [https://www.jotform.com/](https://www.jotform.com/?utm_source=chatgpt.com)).

> La cuenta de Jotform sirve para recibir contribuciones de los usuarios.

6\. **Espera a que se genere el sitio.** Ve a la pestaña `actions` y espera a que el icono de ejecución del flujo de trabajo se ponga en verde. A veces GitHub funciona con lentitud. Si la generación tarda demasiado o falla, espera un par de horas y vuelve a editar el archivo `_config.yml` para activar el proceso.

7\. **Reemplaza o añade en&#x20;**`assets/img/tema` las imágenes que prefieras:

- `logo.png`
- `avatar.png`

8\. **Ve a la pestaña&#x20;**`settings`, abre la sección `pages` y selecciona `GitHub Actions` como la "fuente" (_source_) desde la que se generará el sitio.

9\. **Abre el archivo&#x20;**`_abouts/site-description.md` y escribe una descripción de tu sitio. La línea `<!-- more -->` separa el contenido que aparece en el pie de página de todas las páginas de la descripción más extensa que aparece únicamente en la página `about`.

10\. **Genera el contenido a partir de Zotero** [exportando una colección](https://forums.zotero.org/discussion/5286/can-one-export-a-collection-and-not-the-entire-library?utm_source=chatgpt.com), subcolección o biblioteca como un archivo `csv`.

10.1. Añade una imagen de portada al elemento correspondiente de tu biblioteca de Zotero arrastrándola como archivo adjunto.
10.2. Clona el repositorio en una carpeta local.
10.3. Crea un entorno de Python desde la raíz de la carpeta mediante el comando `python3 -m venv assets/env`.
10.4. Ejecuta `source assets/env/bin/activate`.
10.5. Ejecuta `pip install r requirements.txt`.
10.6. Exporta tu biblioteca o colección de Zotero como un archivo `.csv` y guárdalo como `assets/data/books_zotero.csv`. Recuerda marcar la opción «add notes» para incluir los fragmentos.
10.7. Ejecuta `python3 assets/env/src/morel-generate.py`.
10.8. Confirma tus cambios (**añadiendo&#x20;**`[skip ci]`**&#x20;al mensaje del commit**).
10.9. Sube tus cambios a GitHub (*push*).

\# Añadir imágenes de portada sin escribir código

Si quieres utilizar un generador Refracta sin código que incluya imágenes de portada obtenidas de una biblioteca de Zotero, puedes:

- Solicitar una prespuesto para contratar un servicio personalizado en refractaservicio@gmail.com.
- [Promover este proyecto](https://www.addtoany.com/share?utm_source=chatgpt.com#url=http%3A%2F%2F127.0.0.1%3A4000%2Fmorel-no-code-generator%2F\&title=%7C%20MOREL%20no-code%20website%20generator) para encontrar colaboradores que contribuyan al desarrollo de esta funcionalidad.