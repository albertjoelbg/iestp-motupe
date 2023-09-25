<script>
    import {Card, Button, Breadcrumb, BreadcrumbItem, GradientButton} from 'flowbite-svelte';
    import {
        PhoneOutline,
        MessagesOutline,
        MapLocationOutline,
        FacebookSolid,
        MapPinAltSolid
    } from 'flowbite-svelte-icons';
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
        <GradientButton shadow color="green" class="w-fit">
            <PhoneOutline class="w-3.5 h-3.5 ml-2 text-white mr-2"/>
            <a href="https://api.whatsapp.com/send?phone=975381234" target="_blank"
               rel="noopener noreferrer">975381234</a>
        </GradientButton>
    </Card>
    <Card class="m-4 flex justify-center items-center flex-auto">
        <h5 class="mb-2 text-2xl tracking-tight text-gray-900 dark:text-white">Facebook</h5>
        <GradientButton shadow color="blue" class="w-fit">
            <FacebookSolid class="w-3.5 h-3.5 ml-2 text-white mr-2"/>
            <a href="https://www.facebook.com/tecnologicomotupe" target="_blank">IESTP Motupe</a>
        </GradientButton>
    </Card>
    <Card class="m-4 flex justify-center items-center flex-auto">
        <h5 class="mb-2 text-2xl tracking-tight text-gray-900 dark:text-white">Ubicación</h5>
        <GradientButton shadow color="cyan" class="w-fit">
            <MapLocationOutline class="w-3.5 h-3.5 ml-2 text-white mr-2"/>
            <a href="https://maps.app.goo.gl/t2PVenFqbNa821PT6" target="_blank">Ir a mapa</a>
        </GradientButton>
    </Card>
    <Card class="m-4 flex justify-center items-center flex-auto">
        <h5 class="mb-2 text-2xl tracking-tight text-gray-900 dark:text-white">Correo</h5>
        <GradientButton shadow color="red" class="w-fit">
            <MessagesOutline class="w-3.5 h-3.5 ml-2 text-white mr-2"/>
            <a href="mailto:informes@iestpmotupe.edu.pe" target="_blank">informes@iestpmotupe.edu.pe</a>
        </GradientButton>
    </Card>


</main>

