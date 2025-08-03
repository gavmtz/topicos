# static-export-template

Este es un repositorio de demostración que contiene dos cuadernos de trabajo [Pluto](https://github.com/fonsp/Pluto.jl) que se **convierten automáticamente a HTML** por medio de _github action_ y publicados con _github pages_. 🌝

Consulta el despliegue de este repositorio a través de _github pages_ :
https://juliapluto.github.io/static-export-template/

# ¿Cómo usar la plantilla?

### 👉 Paso 1

Crea una cuenta en GitHub, haz click en ["Use this template"](https://github.com/JuliaPluto/static-export-template/generate). ¡Elíge un nuevo nombre!

<img width="400" alt="screenshot of clicking the Use-this-template button" src="https://user-images.githubusercontent.com/6933510/103711531-f7cdc800-4fb7-11eb-98b7-6ebd070a337b.png">

Ahora cuentas con tu propio repositorio (dale un vistazo al URL), que contiene una copia de los archivos de la plantilla, incluye este archivo que estás leyendo (`README.md`).

### 👉 Paso 2

Haz click en **Add files** (o **+**), seguido de **Upload files**. En la siguiente página, carga los archivos `.jl`.

<img width="400" alt="screenshot of clicking the Upload-files button" src="https://user-images.githubusercontent.com/6933510/103710071-67da4f00-4fb4-11eb-9943-b66f26119d36.png">

Los cuadernos de trabajo se ejecutarán en github cada que actualices los archivos en el repositorio. Para consultar el progreso, dirígete a [la página "Actions"](./actions) de tu repositorio, ahí encontrarás el _workflow_ del último commit.

<img width="400" alt="screenshot of the actions page, showing a currently running workflow" src="https://user-images.githubusercontent.com/6933510/103711844-978b5600-4fb8-11eb-8b1b-1e5bdacc1c85.png">

Espera a que la *acción* realice la ejecución del cuaderno de trabajo.

### 👉 Paso 3

Ve hacia [la página "Settings"](./settings) del repositorio y a la [sección "Pages"](./settings/pages). For the "Source", choose `gh-pages`. Wait a minute for everything to initialize, and the URL to your web page will be shown! 

<img width="400" alt="screenshot of the Pages settings, displaying the URL after the web page is ready" src="https://user-images.githubusercontent.com/6933510/103711695-43807180-4fb8-11eb-9ba8-a96a70612177.png">

Don't worry if it doesn't work immediately! It can take a while for the web page to be ready, even after your settings page says it's done. (Github pages says 20 minutes, but it can take even longer.)

## Actualizar los cuadernos de trabajo (nb.jl)

To update an existing notebook file, simply repeat Step 2 above! (You can also use **Add files** `>` **Upload files** to _update_ upload a file that already exists on the repository.)

Are you working on this website and planning to make many changes? Then it might be nice to use [GitHub Desktop](https://github.com/apps/desktop), a program on your computer that lets you synchronise your local files with github.com more easily, without having to upload to the website each time. If you are familiar with using the terminal, then you can also use the `git` command to publish changes.

# Alternative setup: agrega sitios web a un repositorio existente

If you already have a github repository with some pluto notebooks in it, you may want to add a web view like the one for this repository. In that case, the steps are slightly different. In this case, I assume that you are familiar with adding files to a repository. If not, follow the steps above.

### 👉 Paso 1

From this repository, download [ExportPluto.yaml](./.github/workflows/ExportPluto.yaml). 

Save the file in your own repository, in the same location: make a folder `.github` in the main directory, within that a folder `workflows`, and add the file there, with the name `ExportPluto.yaml`. Commit the new file to your repository. 

*Note: The yaml file states that github should use the github notebooks in the `main` branch or `master` branch of your repository. If you changed the name of your default branch, or you want to use a different branch, change `main` in [line 5](https://github.com/JuliaPluto/static-export-template/blob/main/.github/workflows/ExportPluto.yaml#L5) in the yaml file to the name of your favourite branch.*

Your notebooks will run on github every time that you update the files in this repository. To check the progress, click on ["Actions"](./actions), you will find the _workflow_ for the last commit.

<img width="400" alt="Schermafbeelding 2021-01-06 om 00 45 25" src="https://user-images.githubusercontent.com/6933510/103711844-978b5600-4fb8-11eb-8b1b-1e5bdacc1c85.png">

### 👉 Paso 2

Go to the ["Settings" page](./settings) of your repository, and go to [the "Pages" section](./settings/pages). For the "Source", choose `gh-pages`. Wait a minute for everything to initialize, and the URL to your web page will be shown! 

<img width="400" alt="Schermafbeelding 2021-01-06 om 00 43 00" src="https://user-images.githubusercontent.com/6933510/103711695-43807180-4fb8-11eb-9ba8-a96a70612177.png">

Don't worry if it doesn't work immediately! It can take a while for the web page to be ready, even after your settings page says it's done. (Github pages says 20 minutes, but it can take even longer.)


# 💡Tips

### Paquetes de Julia

Because Pluto has a [built-in package manager](https://github.com/fonsp/Pluto.jl/wiki/%F0%9F%8E%81-Package-management), packages will automatically work on the website!

### Archivos por defecto

This files `README.md` and `My cool notebook.jl` are example files, and you can safely edit or delete them! After you have set up your repository, you can remove these setup instructions from the `README.md` file, and write a description of your project.

### ¿Sigue sin funcionar?

If your website is not automatically updating, then go to the **"Actions"** page of your repository, and take a look at the latest logs. If they show a ❌ symbol, then something went wrong. Click on it, and carefully read the error message. If you get stuck, be sure to ask for help: open an issue at https://github.com/JuliaPluto/static-export-template/issues/new and send us a link to your repository.

### Página de inicio

If you go to the (GitHub Pages) URL of repository, you will see a small index of the notebooks in this repository. You can customize this page, two options are:

-   Create your own `index.html` or `index.md` file, it will be used as the homepage.
-   Rename one of your notebooks to `index.jl`, and it will be the default notebook!

# Licencia

This *template* repository is [Unlicensed](https://unlicense.org), which means that you can do anything you want with it! When you use this template, you are also free to remove this license message.

<details>
<summary>View license text</summary>
(This license applies to the template https://github.com/JuliaPluto/static-export-template, not necessarily to the user of the template.)

```
This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or
distribute this software, either in source code form or as a compiled
binary, for any purpose, commercial or non-commercial, and by any
means.

In jurisdictions that recognize copyright laws, the author or authors
of this software dedicate any and all copyright interest in the
software to the public domain. We make this dedication for the benefit
of the public at large and to the detriment of our heirs and
successors. We intend this dedication to be an overt act of
relinquishment in perpetuity of all present and future rights to this
software under copyright law.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR
OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.

For more information, please refer to <https://unlicense.org>
```
</details>
