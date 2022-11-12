---
sidebar: auto
---

## Pinia 

1. Instalar **Pinia**

Lo instalo con **yarn** ya que con **npm** me dá problemas.
Posiblemente tengas que instalar **yarn** búsca cómo instalarlo en tu sistema operatiro.

```
yarn install @pinia/nuxt
```
No me acuerdo si es necesario instalar también pinia
```
yarn install pinia
```

2. Vete a nuxt.config.ts y añade:

```
modules: [
      '@pinia/nuxt',
    ],
```

### Store Archivo.js
```js
import { defineStore } from 'pinia'

export const almacen = defineStore('main', {
  state: () => {
    return {
      obras: [
        { author: "01", title: "Gamora", photo: "./imagenes/Gamora.jpeg", descripcion: "Gamora es la hija adoptiva de Thanos, y la última de su especie. Sus poderes incluyen fuerza y agilidad sobrehumanas y un factor de curación acelerada"},
        { author: "02", title: "Groot", photo: "./imagenes/Groot.jpeg", descripcion: "Groot es un coloso Flora del Planeta X, la capital de los mundos secundarios"},
        { author: "03", title: "Rocket", photo: "./imagenes/Rocket.jpeg", descripcion: "Rocket, es un individuo genéticamente modificado parecido a un mapache que se convirtió en un criminal al igual que su amigo Groot"},
        { author: "04", title: "StarLord", photo: "./imagenes/StarLord.jpeg", descripcion: "Es el hijo mestizo del emperador J'Son del planeta Spartax y la humana Meredith Quill"},
      ]
    }
  },
})
```
### Vista AboutView.vue

#### script
```js
<script setup>
import BaseCard from '../components/BaseCard.vue'
import { almacen } from '../stores/archivo.js'

const datos = almacen()

</script>
```
#### template
```html
<template>
  <div class="row justify-content-center">
    <BaseCard
      class="col-4 m-2"
      v-for="obra in datos.obras"
      :key="obra.author"
      :obra="obra"
    />
  </div>
</template>
```
### Componente

#### script
```js
<script setup>
defineProps({
  obra: {
    type: Object,
    required: true
  }
})
</script>
```
#### template
```html
<template>
  <div class="card" style="width: 18rem">
    <img :src="obra.photo" class="card-img-top" alt="" />
    <div class="card-body">
      <h5 class="card-title">{{ obra.author }}</h5>
      <p class="card-text">
        {{ obra.title }}
      </p>
      <a href="#" class="btn btn-primary">Leer más</a>
    </div>
  </div>
</template>
```

