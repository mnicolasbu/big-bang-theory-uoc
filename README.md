# Proyecto web: The Big Bang Theory

Web responsive de una sola página sobre *The Big Bang Theory*, hecha para la PEC 1 de Herramientas HTML y CSS II (M4.258) de la UOC.

- **Web publicada:** https://big-bang-theory-uoc.netlify.app/
- **Repositorio:** https://github.com/mnicolasbu/big-bang-theory-uoc

## Autor

- **Nombre:** Manuel Nicolás Budesca
- **GitHub:** [mnicolasbu](https://github.com/mnicolasbu)
- **Asignatura:** Herramientas HTML y CSS II (M4.258), UOC
- **Entrega:** PEC 1

## Tecnologías
- UOC Boilerplate v3.14.0 y Parcel
- Sass (SCSS) con variables, anidado, funciones propias, mixins, parciales y `@use`
- Metodología BEM
- Stylelint con una regla propia que obliga a usar BEM
- Configuración de Stylelint en `.stylelintrc.json` (reglas estándar para SCSS más la regla BEM `selector-class-pattern`)
- Diseño responsive con enfoque mobile first
- Font Awesome para los iconos
- Carrusel de imágenes hecho solo con CSS (`@keyframes`), con soporte para `prefers-reduced-motion`
- Tráiler incrustado con `iframe`, carga diferida (`loading="lazy"`) y proporción fija con `aspect-ratio`
- Imagen de fondo en el hero con degradado oscuro para mantener el texto legible

## Estructura de estilos SCSS

- `src/assets/styles/components/`: componentes BEM (`_button`, `_card`, `_facts`, `_footer`, `_gallery`, `_header`, `_hero`, `_nav`, `_opinion`, `_section`, `_video`).
- `src/assets/styles/layouts/`: estilos globales de la página (`_home.scss`).
- `src/assets/styles/_dependencies.scss`: importa las dependencias de npm (Font Awesome).
- `src/assets/styles/_functions.scss`: funciones propias (`rem`, `tint`, `shade`, `space`).
- `src/assets/styles/_mixins.scss`: mixin `up` para media queries mobile first.
- `src/assets/styles/_variables.scss`: colores, tipografías, anchos y breakpoints.
- `src/assets/styles/main.scss`: fichero principal, solo importa los parciales con `@use`.

## Cómo ejecutarlo

| Comando         | Descripción                                                                                                                                                                                                                                                                                                                                                         |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `npm install`   | Instala las dependencias del proyecto. Hay que ejecutarlo una sola vez, después de clonar el repositorio.                                                                                                                     |
| `npm run dev`   | Revisa los estilos con Stylelint y arranca un servidor local de desarrollo en `http://localhost:8123`. Compila estilos y scripts automáticamente cuando cambia un fichero de `src/`. Es lo que se ejecuta mientras se desarrolla.                                                                                                                     |
| `npm run lint`   | Revisa los ficheros `.scss` con Stylelint y avisa si algo no cumple las reglas de estilo o la nomenclatura BEM.                                                                                                                     |
| `npm run build` | Ejecuta `lint`, borra `dist/` y las cachés, y compila y optimiza los ficheros. El resultado queda en la carpeta `dist/`. Es el comando que usa Netlify para publicar la web. |
| `npm run clean` | Elimina la carpeta `/dist` y las carpetas de caché.                                                                                                                                                                                                                                                                                                               |
| `npm run test`  | Muestra un mensaje de éxito si todo funciona como se espera.                                                                                                                                                                                                                                                                                                    |

## Créditos de las imágenes

Las imágenes de la galería y del fondo del hero proceden de Wikimedia Commons y se usan según sus licencias.

| Imagen      | Título                                                              | Autor                    | Licencia                            |
| ------ | ------ | ----- | -------- |
| 1 | [The Big Bang Theory (Burbank)](https://commons.wikimedia.org/wiki/File:The_Big_Bang_Theory_(Burbank)_July_2022_(4).JPG) | Benoît Prieur | [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/) |
| 2 | [The Big Bang Theory, Comic Book Store "The Comic Center of Pasadena"](https://commons.wikimedia.org/wiki/File:The_Big_Bang_Theory,_Comic_Book_Store_%22The_Comic_Center_of_Pasadena%22_(6196384919).jpg) | Chester | [CC BY 2.0](https://creativecommons.org/licenses/by/2.0/) |
| 3 | [Cast of The Big Bang Theory](https://commons.wikimedia.org/wiki/File:Cast_of_The_Big_Bang_Theory_05.jpg) | therainstopped | [CC BY 2.0](https://creativecommons.org/licenses/by/2.0/) |
| 4 | [The Big Bang Theory (Burbank)](https://commons.wikimedia.org/wiki/File:The_Big_Bang_Theory_(Burbank)_July_2022_(2).JPG) | Benoît Prieur | [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/) |

El icono de la pestaña del navegador (logo_icono.png) y el tráiler de YouTube pertenecen a sus respectivos propietarios y se usan solo con fines académicos.