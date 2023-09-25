<script>
    import "../app.postcss";
    import {
        Navbar,
        NavBrand,
        NavLi,
        NavUl,
        NavHamburger,
        Button,
        Dropdown,
        DropdownItem,
        DropdownDivider,
        Footer,
        FooterCopyright,
        FooterLinkGroup,
        FooterLink,
        FooterBrand,
        FooterIcon,
        ImagePlaceholder
    } from 'flowbite-svelte';

    import {
        ChevronDownOutline,
        FacebookSolid,
        GithubSolid,
        DiscordSolid,
        TwitterSolid
    } from 'flowbite-svelte-icons';
    import {page} from '$app/stores';
    import logo from '$lib/assets/util/logo-iestp-motupe.png';

    $: activeUrl = $page.url.pathname;
</script>

<svelte:head>
    <title>IEST Motupe</title>
</svelte:head>

<Navbar let:hidden let:toggle class="bg-slate-200 fixed z-10 top-0">
    <NavBrand href="/">
        <img alt="Logo IESTP Motupe" src={logo}
             class="mr-3 h-6 sm:h-9" on:click={hidden?hidden:toggle}/>
        <span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white"
              on:click={hidden?hidden:toggle}>IESTP Motupe</span>
    </NavBrand>
    <div class="flex lg:order-2">
        <Button size="sm" color="blue" href="https://campus.iestpmotupe.edu.pe/">Campus Virtual</Button>
        <NavHamburger on:click={toggle}/>
    </div>
    <NavUl {hidden} {activeUrl} class="order-1">
        <NavLi class="cursor-pointer">
            Nosotros
            <ChevronDownOutline class="w-3 h-3 ml-2 text-primary-800 dark:text-white inline"/>
        </NavLi>
        <Dropdown class="w-44 z-20">
            <DropdownItem href="/nosotros/presentacion" on:click={hidden?hidden:toggle}>Presentación</DropdownItem>
            <DropdownDivider/>
            <DropdownItem href="/nosotros/historia" on:click={hidden?hidden:toggle}>Historia</DropdownItem>
            <DropdownDivider/>
            <DropdownItem href="/nosotros/mision-vision" on:click={hidden?hidden:toggle}>Misión y Visión</DropdownItem>
        </Dropdown>
        <NavLi class="cursor-pointer">
            Carreras
            <ChevronDownOutline class="w-3 h-3 ml-2 text-primary-800 dark:text-white inline"/>
        </NavLi>
        <Dropdown class="w-44 z-20">
            <DropdownItem href="/carreras/apsti" on:click={hidden?hidden:toggle}>Arquitectura de Plataformas y Servicios
                TI
            </DropdownItem>
            <DropdownDivider/>
            <DropdownItem href="/carreras/enfermeria-tecnica" on:click={hidden?hidden:toggle}>Enfermería Técnica
            </DropdownItem>
            <DropdownDivider/>
            <DropdownItem href="/carreras/gestion-administrativa" on:click={hidden?hidden:toggle}>Gestión Administrativa
            </DropdownItem>
            <DropdownDivider/>
            <DropdownItem href="/carreras/produccion-agropecuaria" on:click={hidden?hidden:toggle}>Producción
                Agropecuaria
            </DropdownItem>
            <DropdownDivider/>
        </Dropdown>

        <NavLi class="cursor-pointer">
            Entornos Virtuales
            <ChevronDownOutline class="w-3 h-3 ml-2 text-primary-800 dark:text-white inline"/>
        </NavLi>
        <Dropdown class="w-44 z-20">
            <DropdownItem href="/" on:click={hidden?hidden:toggle}>Biblioteca Virtual</DropdownItem>
            <DropdownDivider/>
            <DropdownItem href="/" on:click={hidden?hidden:toggle}>Campus Virtual</DropdownItem>
        </Dropdown>
        <NavLi class="cursor-pointer">
            Gestión Institucional
            <ChevronDownOutline class="w-3 h-3 ml-2 text-primary-800 dark:text-white inline"/>
        </NavLi>
        <Dropdown class="w-44 z-20">
            <DropdownItem href="/" on:click={hidden?hidden:toggle}>Formación Continua</DropdownItem>
            <DropdownDivider/>
            <DropdownItem href="/" on:click={hidden?hidden:toggle}>Unidad Académica</DropdownItem>
            <DropdownDivider/>
            <DropdownItem href="/" on:click={hidden?hidden:toggle}>Bienestar y Empleabilidad</DropdownItem>
        </Dropdown>
        <NavLi href="/contacto" on:click={hidden?hidden:toggle}>Contacto</NavLi>
    </NavUl>
</Navbar>
<div class="mt-20 sm:mt-30 md:mt-40 lg:mt-20 md:pt-0">
    <slot/>
</div>


<ImagePlaceholder class="m-5"/>
<ImagePlaceholder class="m-5"/>
<Footer footerType="socialmedia" class="bg-slate-200">
    <div class="md:flex md:justify-between">
        <div class="mb-6 md:mb-0">
            <FooterBrand href="/" alt="Logo IESTP Motupe"
                         src={logo}
                         name="IESTP Motupe"/>
        </div>
        <div class="grid grid-cols-2 gap-8 sm:gap-6 sm:grid-cols-3">
            <div>
                <h2 class="mb-6 text-sm font-semibold text-gray-900 uppercase dark:text-white">Resources</h2>
                <FooterLinkGroup>
                    <FooterLink liClass="mb-4" href="/">Flowbite</FooterLink>
                    <FooterLink liClass="mb-4" href="/">Tailwind CSS</FooterLink>
                </FooterLinkGroup>
            </div>
            <div>
                <h2 class="mb-6 text-sm font-semibold uppercase text-gray-900 dark:text-white">Follow us</h2>
                <FooterLinkGroup>
                    <FooterLink liClass="mb-4" href="/">GitHub</FooterLink>
                    <FooterLink liClass="mb-4" href="/">Discord</FooterLink>
                </FooterLinkGroup>
            </div>
            <div>
                <h2 class="mb-6 text-sm font-semibold uppercase text-gray-900 dark:text-white">Legal</h2>
                <FooterLinkGroup>
                    <FooterLink liClass="mb-4" href="/">Privacy Policy</FooterLink>
                    <FooterLink liClass="mb-4" href="/">Terms & Conditions</FooterLink>
                </FooterLinkGroup>
            </div>
        </div>
    </div>
    <hr class="my-6 border-gray-200 sm:mx-auto dark:border-gray-700 lg:my-8"/>
    <div class="sm:flex sm:items-center sm:justify-between">
        <FooterCopyright href="/" by="Instituto de Educación Superior Tecnológico Público Motupe"/>
        <div class="flex mt-4 space-x-6 sm:justify-center sm:mt-0">
            <FooterIcon href="/">
                <FacebookSolid
                        class="w-4 h-4 text-gray-500 dark:text-gray-500 hover:text-gray-900 dark:hover:text-white"/>
            </FooterIcon>
            <FooterIcon href="/">
                <DiscordSolid
                        class="w-4 h-4 text-gray-500 dark:text-gray-500 hover:text-gray-900 dark:hover:text-white"/>
            </FooterIcon>
            <FooterIcon href="/">
                <TwitterSolid
                        class="w-4 h-4 text-gray-500 dark:text-gray-500 hover:text-gray-900 dark:hover:text-white"/>
            </FooterIcon>
            <FooterIcon href="/">
                <GithubSolid
                        class="w-4 h-4 text-gray-500 dark:text-gray-500 hover:text-gray-900 dark:hover:text-white"/>
            </FooterIcon>
        </div>
    </div>
</Footer>