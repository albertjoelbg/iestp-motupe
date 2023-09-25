<script>
    import {Breadcrumb, BreadcrumbItem, Carousel, Gallery, Heading, P, Span} from 'flowbite-svelte';
    import {images, desfile, reinado, aniversario} from './+server.js';

    let index = 0;
    let image;

</script>
<Breadcrumb aria-label="Default breadcrumb example" class="mx-2 pt-2 px-2">
    <BreadcrumbItem href="/" home>Home</BreadcrumbItem>
    <BreadcrumbItem href="#"></BreadcrumbItem>
</Breadcrumb>

<Heading tag="h1" class="mb-4 p-3" customSize="text-2xl font-bold  md:text-5xl lg:text-5xl text-center">
    <Span gradient>Instituto de Educación Superior Tecnológico
    Público Motupe</Span>
</Heading>
<div class="overflow-hidden w-full">
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