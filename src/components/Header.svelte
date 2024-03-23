<script>
    import { useOs } from '@svelteuidev/composables';
	const os = useOs();
</script>

<header class="relative mt-[23rem]">
    <div class="absolute inset-0 flex justify-center items-center">
        <div class="container mx-auto px-4 md:px-0 flex flex-col justify-center items-center h-full">
            <div>
                <h1 class="text-5xl md:text-5xl lg:text-5xl xl:text-8xl font-bold leading-none text-center text-white">
                    Cyber Street Race
                </h1>
                <p class="text-base md:text-lg lg:text-lg xl:text-lg font-light text-white/70 text-center px-4">
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit. In ac nibh finibus, dapibus urna sed, fringilla nibh.
                </p>
            </div>
            {#if os == "android"}
            <button disabled class="text-xs md:text-lg lg:text-lg xl:text-lg font-bold text-white mt-5 bg-gradient-to-t from-[#5C76FF]/20 to-[#3345AE]/30 border-2 border-[#627BFF] rounded-lg py-3 px-10 md:px-14">
                <i class="ri-install-line"></i> Disabled For Android
            </button>
            {:else if os == "ios"}
            <button disabled class="text-xs md:text-lg lg:text-lg xl:text-lg font-bold text-white mt-5 bg-gradient-to-t from-[#5C76FF]/20 to-[#3345AE]/30 border-2 border-[#627BFF] rounded-lg py-3 px-10 md:px-14">
                <i class="ri-install-line"></i> Disabled For Android
            </button>
            {:else}
            <button disabled class="text-xs md:text-lg lg:text-lg xl:text-lg font-bold text-white mt-5 bg-gradient-to-t from-[#5C76FF]/20 to-[#3345AE]/30 border-2 border-[#627BFF] rounded-lg py-3 px-10 md:px-14">
                <i class="ri-install-line"></i> Install | {os}
            </button>
            {/if}
        </div>
    </div>
</header>