<script>
    import Icon from "../../public/icon.svelte";

    let isToggled = false;

    function handleToggle() {
        isToggled = !isToggled;
    }

</script>

<nav class="relative px-6 mb-3 flex justify-between items-center pt-6 pb-6 font-medium md:px-16 lg:px-16 shadow-lg bg-white z-40">
    
    <!-- TITLE -->

    <div class="basis-1/6">
        <Icon />
    </div>

    <h1 class="text-lg font-light basis-4/6 text-center underline underline-offset-8">
        <a href="/">Yolo Community Band</a>
    </h1>
    
    <div class="hidden xl:block basis-1/6">
        <div class="flex gap-12 justify-end items-end">
            <a href="#">Home</a>
            <a href="#">Services</a>
            <a href="#">Contact</a>
        </div>
    </div>

    <div class="basis-1/6 flex flex-col justify-end items-end xl:hidden">
        <button on:click="{handleToggle}" class="space-y-1 cursor-pointer z-50 items-end">
            <span class="block h-0.5 w-8 bg-black"></span>
            <span class="block h-0.5 w-6 bg-black"></span>
            <span class="block h-0.5 w-4 bg-black"></span>
        </button>
    </div>

    {#if isToggled}
        <div class="fixed flex bg-white bottom-0 left-0 w-full h-screen items-center justify-center xl:hidden z-40">
            <div class="flex flex-col gap-24 text-lg">
                <a href="#">Home</a>
                <a href="#">Services</a>
                <a href="#">Contact</a>
            </div>
        </div>
    {/if}
    
</nav>