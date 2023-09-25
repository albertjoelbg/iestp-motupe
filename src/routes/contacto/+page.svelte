<script>
    import {Card, Button, Breadcrumb, BreadcrumbItem} from 'flowbite-svelte';
    import {PhoneSolid, MessagesSolid, MapLocationOutline, FacebookSolid} from 'flowbite-svelte-icons';
</script>
<Breadcrumb aria-label="Default breadcrumb example" class="m-2 p-2">
    <BreadcrumbItem href="/" home>Home</BreadcrumbItem>
    <BreadcrumbItem href="#">Contacto</BreadcrumbItem>
    <BreadcrumbItem href="#"></BreadcrumbItem>
</Breadcrumb>
<h1 class="text-3xl text-center p-4 m-4 font-bold text-gray-600">Contacto</h1>

<main class="flex justify-center items-center flex-wrap m-4 p-4">
    <Card class="m-4 flex justify-center items-center flex-auto">
        <h5 class="mb-2 text-2xl tracking-tight text-gray-900 dark:text-white">Whatsapp</h5>
        <Button class="w-fit bg-green-500 hover:bg-gray-600">
            <PhoneSolid class="w-3.5 h-3.5 ml-2 text-white mr-2"/>
            <a href="https://api.whatsapp.com/send?phone=910920997" target="_blank" rel="noopener noreferrer">(+51)
                910920997</a>
        </Button>
    </Card>
    <Card class="m-4 flex justify-center items-center flex-auto">
        <h5 class="mb-2 text-2xl tracking-tight text-gray-900 dark:text-white">Correo</h5>
        <Button class="w-fit bg-red-600 hover:bg-gray-600">
            <MessagesSolid class="w-3.5 h-3.5 ml-2 text-white mr-2"/>
            <a href="mailto:informes@iestpmotupe.edu.pe">informes@iestpmotupe.edu.pe</a>
        </Button>
    </Card>
    <Card class="m-4 flex justify-center items-center flex-auto">
        <h5 class="mb-2 text-2xl tracking-tight text-gray-900 dark:text-white">Dirección</h5>
        <Button class="w-fit bg-yellow-300 hover:bg-gray-600">
            <MapLocationOutline class="w-3.5 h-3.5 ml-2 text-white mr-2"/>
            <a href="https://maps.app.goo.gl/t2PVenFqbNa821PT6" target="_blank">Ir a mapa</a>
        </Button>
    </Card>
    <Card class="m-4 flex justify-center items-center flex-auto">
        <h5 class="mb-2 text-2xl tracking-tight text-gray-900 dark:text-white">Facebook</h5>
        <Button class="w-fit bg-blue-800 hover:bg-gray-600">
            <FacebookSolid class="w-3.5 h-3.5 ml-2 text-white mr-2"/>
            <a href="https://www.facebook.com/tecnologicomotupe">IESTP Motupe</a>
        </Button>
    </Card>
</main>

