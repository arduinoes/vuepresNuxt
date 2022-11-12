---
sidebar: auto
---

# Básicos

## Carpetas

### Pages 

Esta carpeta **pages** contiene las páginas o subpáginas de desarrollo.

- En el archivo **app.vue** cambia la etiqueta **Welcome**

```vue
 <NuxtPage />
```
- Redirecciona a **pages/index.vue** y **pages/about.vue**

```vue
<NuxtLink to="/">Inicio</NuxtLink>
<NuxtLink to="/about">About</NuxtLink>
```

```js
<button @click="navegarA"> Navegar </button>

function navegarA () {
  navigateTo("about")
}
```

- Rutas dinámicas 

El nombre del archivo será **nombreArchivo-[nombre].vue**

```vue
<p> Ruta dinámica {{ $route.params.nombre}} </p>
```

- SEO título de la página 

```js
useHead({
  title: 'My App',
  meta: [
    { name: 'description', content: 'My amazing site.' }
  ]
})
```

- nuxt.config.ts

```js
app: {
  head: {
    charset: 'utf-16',
    viewport: 'width=500, initial-scale=1', 
    title: 'My App',
    meta: [
      { name: 'description', content: 'My amazing site.' }
    ],
  }
}
```


- Etiquetas

```vue
<div>
  <Head> 
    <Title> Título de la página </Title>
    <Meta> Para añadir metas</Meta>
  </Head>
</div>
```


### Components 

Esta carpeta **components** contiene partes/componentes de las páginas.

- Components/Navbar.vue

```vue
<Navbar />
```

- Conponents/Nav/Bar.vue

```vue
<NavBar /> // Camel-case
```
```vue
<nav-bar /> // Kebab-case
```

### Layouts

Esta carpeta **layouts** contiene estilos de página.

- Crea el archivo **default.vue**


### Assets 

Esta carpeta **assets** contiene utilidades como archivos **css**.


### Public 

Esta carpeta **public** contiene archivos como **png/jpeg**

### Composables

Esta carpeta **composables** contiene funciones reutilizables.

## Etiquetas

- Redirecciona a la carpeta **pages**

```vue
 <NuxtPage />
```
- Redirecciona a **pages/index.vue**

```vue
<NuxtLink to="/">Inicio</NuxtLink>
```
