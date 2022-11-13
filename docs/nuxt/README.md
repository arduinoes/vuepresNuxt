---
sidebar: auto
---


# Vue 3 Vite

## Instalación

Nuxt 3 [install](https://v3.nuxtjs.org/)

1. Crea una carpeta y arrastrala a Visual Studio

2. Abre el terminal y escribe:

Si utilizas el modo pnpm y no lo tienes instalado:

```
npx nuxi init nuxt-app
```  

3. Dentro de la carpeta encontraremos el proyecto. Arrastralo a Visual Studio Code.

4. Abre el terminal y escribe:
```
npm install
```
para instalar los módulos de Node.js

5. Lanza el proyecto en modo desarrollo y comprueba que todo funciona
```
npm run dev
```

## Boostrap

1. Instala Boostrap:
```
npm i bootstrap
```
```
npm i @popperjs/core 
```
2. Instala **sass** alguna versión superior me ha dado problemas, con esta funciona **versión 1.54.8** bien.

```
npm i --dev sass@1.54.8 sass-loader
```
3. Create **assets/styles/main.scss**

```
@import "bootstrap/scss/bootstrap";
```
4. Añade al archivo **nuxt.config.ts**

```
css: ['~/assets/styles/main.scss'],
```

5. Crea **pluging/bootstrap.client.ts**

Para que funcione el menú de la barra de navegación

```js
import { Modal } from "bootstrap";

export default defineNuxtPlugin(() => ({
  provide: {
    bootstrap: {
      Modal,
    },
  },
}));
```

## Components

1. A la misma altura que **app.vue** crea la carpeta **components**

2. Crea el componente **Navbar.vue**

```
components/Navbar.vue
```

3. Cópialo de Boostrap [Navbar](https://getbootstrap.com/docs/5.2/components/navbar/)

4. Modifica la etiqueta **a** por **NuxtLink** y con el atributo **to="/about"**

```vue
<NuxtLink to="/about"   > </NuxtLink>
```

5. Elimina desde **ul** hasta **Home**

6. Vete al archivo **app.vue** y escribe la etiqueta **Navbar**

## Pages opción 1

1. Crea una carpeta con el nombre **pages**

2. Crea un archivo con el nombre **index.vue**

3. Crea un archivo con el nombre **about.vue**

```
pages/index.vue
```

4. Pon una etiqueta con un texto de prueba "Hola index"

5. Pon una etiqueta con el texto de prueba "About"

6. Vete a el archivo **app.vue** y cambia  por **NuxtWelcome** por **NuxtPage**

## Pages opción 2

1. Vete a nuxt.config.ts y añade:

```
 srcDir: 'src/'
```
2. Crea una carpeta con el nombre **src**

Dentro de esta carpeta incluye las de **assets, components, public...**

3. Crea otra dentro con el nombre **pages**

4. Añade un archivo con el nombre **index.vue**

```
src/pages/index.vue
```

5. Vete a el archivo **app.vue** y cambia  por **NuxtWelcome** por **NuxtPage**




