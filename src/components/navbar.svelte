<script>
    import Icon from "../../public/icon.svelte";

    let isToggled = false;

    function handleToggle() {
        isToggled = !isToggled;
    }

</script>

<nav class="relative mx-6 mb-24 flex justify-between items-center pt-12 pb-6 font-medium md:mx-16 lg:mx-16">
    <svg class="absolute bottom-0 left-1/2 -translate-x-1/2" 
        width='250' height='4' 
        viewBox='0 0 250 4' 
        fill='none' 
        xmlns="https://www.w3.org/200/svg"
    >
        <path d="m2 2L428 2" stroke="#282828" stroke-width="2" stroke-linecap="round" />
    </svg>
    
    <!-- TITLE -->

    <div class="basis-1/6">
        <Icon />
    </div>

    <h1 class="text-lg font-bold basis-4/6 text-center">
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
        <div class="fixed flex bg-white bottom-0 left-0 w-full h-screen items-center justify-center xl:hidden">
            <div class="flex flex-col gap-24 text-lg">
                <a href="#">Home</a>
                <a href="#">Services</a>
                <a href="#">Contact</a>
            </div>
        </div>
    {/if}
    
</nav>