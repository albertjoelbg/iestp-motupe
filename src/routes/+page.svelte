<script>
    import {Carousel, Gallery} from 'flowbite-svelte';
    import {images, desfile, reinado, aniversario} from './+server.js';

    let index = 0;
    let image;

</script>
<h1 id="titulo" class="text-3xl text-center p-4 m-4 font-bold text-gray-600">Instituto de Educación Superior Tecnológico
    Público Motupe</h1>
<div>
    <Carousel {images} let:Indicators on:change={({ detail }) => (image = detail)} duration="4000">
        <Indicators/>
    </Carousel>

    <div class="rounded p-3 bg-gray-300 dark:bg-gray-700 dark:text-white my-2 text-center">
        <a class="text-lg hover:underline hover:text-blue-600" href={image?.url}>{image?.alt}</a>
    </div>
</div>

<h2 class="text-2xl text-center p-4 m-4 font-bold text-gray-600">Recuerdos</h2>

<Gallery class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-3 gap-4">
    <Gallery items={desfile}/>
    <Gallery items={reinado}/>
    <Gallery items={aniversario}/>
</Gallery>