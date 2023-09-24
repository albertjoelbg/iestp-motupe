<script>
    import {Carousel} from 'flowbite-svelte';
    import {images} from './+server.js';

    let index = 0;
    let image;
</script>
<h1 class="text-2xl text-center m-3 p-3">Agropecuaria</h1>

<div class="">
    <Carousel {images} let:Indicators let:Controls on:change={({ detail }) => (image = detail)}>
        <Controls/>
        <Indicators/>
    </Carousel>

    <div class="rounded h-10 bg-gray-300 dark:bg-gray-700 dark:text-white p-2 my-2 text-center">
        {image?.alt}
    </div>
</div>

