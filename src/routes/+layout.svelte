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
        Banner,
        ImagePlaceholder
    } from 'flowbite-svelte';

    import {
        ChevronDownOutline,
        FacebookSolid,
        GithubSolid,
        DiscordSolid,
        TwitterSolid,
        BullhornSolid,
        FaceGrinSolid
    } from 'flowbite-svelte-icons';
    import {page} from '$app/stores';

    $: activeUrl = $page.url.pathname;
</script>
<Navbar let:hidden let:toggle class="bg-slate-200">
    <Banner id="default-banner" position="relative">
        <p class="flex items-center text-sm font-normal text-gray-500 dark:text-gray-400">
    <span class="inline-flex p-1 mr-3 bg-white-200 rounded-full dark:bg-gray-600">
      <BullhornSolid class="w-3 h-3 text-yellow-300 dark:text-gray-400"/>
      <span class="sr-only">Light bulb</span>
    </span>
            <span>New Landing Page!</span>
        </p>
    </Banner>
    <NavBrand href="/">
        <img alt="Logo IESTP Motupe" src="https://www.iestpmotupe.edu.pe/wp-content/uploads/2022/08/Logo-150x150.jpg"
             class="mr-3 h-6 sm:h-9"/>
        <span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">IESTP Motupe</span>
    </NavBrand>
    <div class="flex md:order-2">
        <Button size="sm" color="blue">Campus Virtual</Button>
        <NavHamburger on:click={toggle}/>
    </div>
    <NavUl {hidden} {activeUrl} class="order-1">
        <NavLi href="/nosotros">Nosotros</NavLi>
        <NavLi class="cursor-pointer">
            Carreras
            <ChevronDownOutline class="w-3 h-3 ml-2 text-primary-800 dark:text-white inline"/>
        </NavLi>
        <Dropdown class="w-44 z-20">
            <DropdownItem href="/carreras/apsti">Arquitectura de Plataformas de TI</DropdownItem>
            <DropdownDivider/>
            <DropdownItem href="/carreras/enfermeria-tecnica">Enfermería Técnica</DropdownItem>
            <DropdownDivider/>
            <DropdownItem href="/carreras/gestion-administrativa">Gestión Administrativa</DropdownItem>
            <DropdownDivider/>
            <DropdownItem href="/carreras/produccion-agropecuaria">Producción Agropecuaria</DropdownItem> <DropdownDivider/>
        </Dropdown>

        <NavLi class="cursor-pointer">
            Entornos Virtuales
            <ChevronDownOutline class="w-3 h-3 ml-2 text-primary-800 dark:text-white inline"/>
        </NavLi>
        <Dropdown class="w-44 z-20">
            <DropdownItem href="/">Biblioteca Virtual</DropdownItem>
            <DropdownDivider/>
            <DropdownItem href="/">Campus Virtual</DropdownItem>
        </Dropdown>
        <NavLi class="cursor-pointer">
            Gestión Institucional
            <ChevronDownOutline class="w-3 h-3 ml-2 text-primary-800 dark:text-white inline"/>
        </NavLi>
        <Dropdown class="w-44 z-20">
            <DropdownItem href="/">Formación Continua</DropdownItem>
            <DropdownDivider/>
            <DropdownItem href="/">Unidad Académica</DropdownItem>
            <DropdownDivider/>
            <DropdownItem href="/">Bienestar y Empleabilidad</DropdownItem>
        </Dropdown>
        <NavLi href="/contacto">Contacto</NavLi>
    </NavUl>
</Navbar>

<slot/>

<ImagePlaceholder class="m-5"/>
<ImagePlaceholder class="m-5"/>
<ImagePlaceholder class="m-5"/>
<ImagePlaceholder class="m-5"/>

<Footer footerType="socialmedia" class="bg-slate-200">
    <div class="md:flex md:justify-between">
        <div class="mb-6 md:mb-0">
            <FooterBrand href="/" alt="Logo IESTP Motupe"
                         src="https://www.iestpmotupe.edu.pe/wp-content/uploads/2022/08/Logo-150x150.jpg"
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
