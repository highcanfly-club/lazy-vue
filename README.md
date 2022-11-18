# Lazy utilities for Vue3
This utility is developped for internal use.  
Feel free to use it but there is strictly no support.  
It uses TailwindCss classes.

## LazyObserver
it loads a component while the user scrolls on it
```html
<template>
    <lazy-observer :id="index" @on-change="onlazyMeteo">
        <some-custom-vue-sfc />
    </lazy-observer>
</template>
<script setup lang="ts">
import {LazyObserver} from "@sctg/lazy-vue";
</script>
```
## LazyImg
it loads a component while the user scrolls on it
```html
<template>
    <lazy-img class="mx-auto w-8 h-8" src="https://someurl/img.jpg"
                alt="Alt text" />
</template>
<script setup lang="ts">
import {LazyImg} from "@sctg/lazy-vue";
</script>
```

## CssLightbox
this is a no script pure css lightbox
it needs to create zIndex: 999 in tailwindConfig
```html
<template>
    <css-lightbox class="absolute block left-0 top-O w-full h-full"
            src="https://someurl/img.jpg"
            full-screen-src="https://someurl/img-full-res.jpg"
            :lazy="true"
            />
</template>
<script setup lang="ts">
import {CssLightbox} from "@sctg/lazy-vue";
import '@sctg/lazy-vue/dist/index.css'
</script>

```