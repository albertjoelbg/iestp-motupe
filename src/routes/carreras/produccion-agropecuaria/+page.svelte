<script>
    import {Carousel} from 'flowbite-svelte';
    import {images} from './+server.js';
    let index = 0;
    let image;
</script>
<h1 class="text-3xl text-center p-4 m-4 font-bold text-gray-600">Producción Agropecuaria</h1>

<div>
    <Carousel {images} let:Indicators let:Controls on:change={({ detail }) => (image = detail)}>
        <Controls/>
        <Indicators/>
    </Carousel>

    <div class="rounded p-3 bg-gray-300 dark:bg-gray-700 dark:text-white my-2 text-center">
        <span class="text-lg" href={image?.url}>{image?.alt}</span>
    </div>
</div>

