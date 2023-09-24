<script>
    import {Card, Button} from 'flowbite-svelte';
    import {PhoneSolid, MessagesSolid, MapLocationOutline, FacebookSolid} from 'flowbite-svelte-icons';
</script>

<h1 class="text-3xl text-center p-4 m-4 font-bold text-gray-600">Contacto</h1>

<main class="flex justify-center items-center flex-wrap">
    <Card class="m-4 flex justify-center items-center flex-auto">
        <h5 class="mb-2 text-2xl tracking-tight text-gray-900 dark:text-white">Whatsapp</h5>
        <Button class="w-fit bg-green-500 hover:bg-gray-600">
            <PhoneSolid class="w-3.5 h-3.5 ml-2 text-white mr-2"/>
            <span>(+51) 910920997</span>
        </Button>
    </Card>
    <Card class="m-4 flex justify-center items-center flex-auto">
        <h5 class="mb-2 text-2xl tracking-tight text-gray-900 dark:text-white">Correo</h5>
        <Button class="w-fit bg-red-600 hover:bg-gray-600">
            <MessagesSolid class="w-3.5 h-3.5 ml-2 text-white mr-2"/>
            <span>informes@iestpmotupe.edu.pe</span>
        </Button>
    </Card>
    <Card class="m-4 flex justify-center items-center flex-auto">
        <h5 class="mb-2 text-2xl tracking-tight text-gray-900 dark:text-white">Dirección</h5>
        <Button class="w-fit bg-yellow-300 hover:bg-gray-600">
            <MapLocationOutline class="w-3.5 h-3.5 ml-2 text-white mr-2"/>
            <span>Ir a mapa</span>
        </Button>
    </Card>
    <Card class="m-4 flex justify-center items-center flex-auto">
        <h5 class="mb-2 text-2xl tracking-tight text-gray-900 dark:text-white">Facebook</h5>
        <Button class="w-fit bg-blue-800 hover:bg-gray-600">
            <FacebookSolid class="w-3.5 h-3.5 ml-2 text-white mr-2"/>
            <span>IESTP Motupe</span>
        </Button>
    </Card>
</main>

