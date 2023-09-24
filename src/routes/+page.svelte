<script>
    import {Carousel} from 'flowbite-svelte';
    import {images} from './+server.js';

    let index = 0;
    let image;
</script>
<h1 class="text-2xl text-center p-3 m-3">Instituto de Educación Superior Tecnológico Público Motupe</h1>
<div>
    <Carousel {images} let:Indicators on:change={({ detail }) => (image = detail)} duration="3000">
        <Indicators/>
    </Carousel>

    <div class="rounded h-10 bg-gray-300 dark:bg-gray-700 dark:text-white p-2 my-2 text-center">
        {image?.alt}
    </div>
</div>