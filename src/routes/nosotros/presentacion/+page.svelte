<script>
    import {Breadcrumb, BreadcrumbItem, List, Li, Heading} from "flowbite-svelte";
    import {CheckCircleSolid} from 'flowbite-svelte-icons';
</script>

<Breadcrumb aria-label="Default breadcrumb example" class="m-2 p-2">
    <BreadcrumbItem href="/" home>Home</BreadcrumbItem>
    <BreadcrumbItem href="#">Nosotros</BreadcrumbItem>
    <BreadcrumbItem href="/nosotros/presentacion">Presentación</BreadcrumbItem>
    <BreadcrumbItem href="#"></BreadcrumbItem>
</Breadcrumb>
<h1 class="text-3xl text-center p-4 m-4 font-bold text-gray-600">Presentación</h1>

<main class="max-w-3xl mx-auto px-10 lg:px-0 text-justify">
    <p class="my-4">Saludo a la comunidad en representación del Instituto de Educación Superior Tecnológico Público
        “Motupe”;
        institución creada hace 36 años; el 14 de septiembre de 1984 para ofertar servicio educativo a los jóvenes y
        adultos interesados en capacitarse para el empleo y autoempleo; generando la mejora de las economías de las
        familias del distrito de Motupe y lugares aledaños; poniendo énfasis en el cuidado del medio ambiente practica
        de valores que permitan el desarrollo sostenible como personas y ciudadanos en pos de una comunidad exitosa.</p>
    <p class="my-4">En sus tres décadas de trabajo nuestra Institución busca interrelaciones de manera fluida y dinámica
        con las
        instituciones públicas y privadas; empresas agroindustriales y de servicios establecidos en el valle
        Motupe-Olmos; y con los pequeños y medianos productores del valle para que asuman su rol de emprendedores
        asociándose para enfrentar los retos del mercado complejo y exigente tanto en demanda como oferta de productos y
        servicios.</p>
    <p class="my-4">En el desarrollo de nuestras actividades Institucionales aspiramos a la mejora continua con la
        participación
        decidida y el compromiso de todos los estamentos que conforman la Institución para obtener como producto
        profesionales técnicos competentes que solucionen problemas en el área de producción y servicios a través de
        nuestros 04 programas de estudios:</p>
    <Heading tag="h2" customSize="text-lg font-semibold"
             class="mb-2 text-lg font-semibold text-gray-900 dark:text-white">Programas de Estudio:
    </Heading>
    <List tag="ul" class="space-y-1 text-gray-800 dark:text-gray-400" list="none">
        <Li icon>
            <CheckCircleSolid class="w-3.5 h-3.5 mr-2 text-green-500 dark:text-green-400"/>
            Arquitectura de Plataformas de Tecnología de Información
        </Li>
        <Li icon>
            <CheckCircleSolid class="w-3.5 h-3.5 mr-2 text-green-500 dark:text-green-400"/>
            Enfermería Técnica
        </Li>
        <Li icon>
            <CheckCircleSolid class="w-3.5 h-3.5 mr-2 text-green-500 dark:text-green-400"/>
            Gestión Administrativa
        </Li>
        <Li icon>
            <CheckCircleSolid class="w-3.5 h-3.5 mr-2 text-green-500 dark:text-green-400"/>
            Producción Agropecuaria
        </Li>

    </List>
</main>