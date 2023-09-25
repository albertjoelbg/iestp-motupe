<script>
    import {Breadcrumb, BreadcrumbItem, Carousel} from 'flowbite-svelte';
    import {images} from './+server.js';

    let index = 0;
    let image;
</script>
<Breadcrumb aria-label="Default breadcrumb example" class="m-2 p-2">
    <BreadcrumbItem href="/" home>Home</BreadcrumbItem>
    <BreadcrumbItem href="#">Carreras</BreadcrumbItem>
    <BreadcrumbItem href="/carreras/apsti">Arquitectura de Plataformas y Servicios TI</BreadcrumbItem>
    <BreadcrumbItem href="#"></BreadcrumbItem>
</Breadcrumb>
<h1 class="text-3xl text-center p-4 m-4 font-bold text-gray-600">Arquitectura de Plataformas y Servicios de Tecnología
    de Información</h1>

<div class="overflow-hidden w-full">
    <Carousel {images} let:Indicators let:Controls on:change={({ detail }) => (image = detail)}>
        <Controls/>
        <Indicators/>
    </Carousel>

    <div class="rounded p-3 bg-gray-300 dark:bg-gray-700 dark:text-white my-2 text-center">
        <span class="text-lg" href={image?.url}>{image?.alt}</span>
    </div>
</div>

