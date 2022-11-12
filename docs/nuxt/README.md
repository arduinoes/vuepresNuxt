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
npm i --dev sass
```
3. Create **assets/styles/main.scss**

```
@import "bootstrap/scss/bootstrap";
```
4. Añade al archivo **nuxt.config.ts**

```
css: ['~/assets/styles/main.scss'],
```

## Pages opción 1

1. Crea una carpeta con el nombre **pages**

2. Crea un archivo con el nombre **index.vue**

```
pages/index.vue
```

3. Pon una etiqueta con un texto de prueba "Hola index"

4. Crea otra llamada **about.vue**

5. Pon una etiqueta con el texto de prueba "Sobre nosotros"

## Pages opción 2

1. Vete a nuxt.config.ts y añade:

```
 srcDir: 'src/'
```
2. Crea una carpeta con el nombre **src**

3. Crea otra dentro con el nombre **pages**

4. Añade un archivo con el nombre **index.vue**

```
src/pages/index.vue
```

5. Vete a el archivo **app.vue** y cambia  por **NuxtWelcome** por **NuxtPage**

## Components

1. A la misma altura que **pages** crea la carpeta **components**

2. Crea el componente **Navbar.vue**

3. Cópialo de Boostrap

## Routering

1. Copia una barra de navegación de Boostrap

2. Modifica la etiqueta **a** por **NuxtLink** y con el atriburo **to="/about"**

3. Vete al archivo **app.vue** y escribe la etiqueta **Navbar**


