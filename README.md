# The Big Bang Theory · Serie recomendada

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
- Sass (SCSS) con variables, anidado, funciones propias, parciales y `@use`
- Metodología BEM
- Stylelint con una regla propia que obliga a usar BEM
- Configuración de Stylelint en `.stylelintrc.json` (reglas estándar para SCSS más la regla BEM `selector-class-pattern`)

## Estructura de estilos SCSS

- `src/assets/styles/components/`: componentes BEM (`_button`, `_card`, `_facts`, `_footer`, `_header`, `_hero`, `_nav`, `_opinion`, `_section`).
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