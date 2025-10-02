# Hello Vue.js

Este es un ejemplo sencillo de cómo usar **Vue 3** con la sintaxis de Composition API directamente en un archivo HTML, sin necesidad de build tools como Vite o Webpack.

## Tecnologías utilizadas

- **Vue 3** (via CDN)
- **HTML5**
- **JavaScript moderno (ES6+)**

## Descripción

Este ejemplo muestra cómo:

1. **Mostrar datos reactivos**:  
   El mensaje dentro de `<h1>` se actualiza automáticamente cuando se escribe en el input gracias a `v-model`.

2. **Usar eventos**:  
   Se incrementa un contador cada vez que se hace clic en el botón usando `@click`.

3. **Composition API**:  
   Se utilizan `ref` para crear variables reactivas y funciones dentro de `setup()`.

## Uso

1. Clona o descarga este archivo.
2. Abre el archivo `index.html` en tu navegador.
3. Escribe en el input y observa cómo el texto cambia en tiempo real.
4. Haz clic en el botón para incrementar el contador.

## Código principal

```javascript
const { createApp, ref } = Vue

createApp({
    setup() {
        const message = ref("Hello Vue.js, this is my first practice.")
        const counter = ref(0)

        function count() {
            counter.value++
        }

        return { message, counter, count }
    }
}).mount("#app")
