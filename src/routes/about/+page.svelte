<script>
    import { lazy } from '@svelteuidev/composables';
    import Footer from '../../components/Footer.svelte';
    import Navbar from '../../components/Navbar.svelte';
</script>

<Navbar />

<section class="relative p-5">
    <div class="container mx-auto px-4 md:px-0 grid grid-cols-1 lg:grid-cols-2 items-center gap-x-10 mt-10">
        <div class="text-white">
            <span class="text-sm md:text-base lg:text-base uppercase text-[#627BFF]">What Is Cyber Street Race?</span>
            <h2 class="text-3xl md:text-5xl lg:text-5xl font-bold leading-none py-2">About</h2>
            <hr class="border-white border-t-2 w-24 py-1">
            <p class="text-base md:text-lg lg:text-lg text-white/70">Lorem ipsum dolor sit amet, consectetur adipiscing elit. In ac nibh finibus, dapibus urna sed, fringilla nibh. Nullam pharetra, odio at malesuada gravida, orci urna laoreet ligula, quis congue sapien magna sed odio.</p>
            <a href="/" class="text-sm font-bold text-white relative top-7 bg-gradient-to-t from-[#5C76FF]/20 to-[#3345AE]/30 border-2 border-[#627BFF] rounded-lg py-2 md:py-3 lg:py-3 px-14">
                <i class="ri-arrow-left-s-line"></i> Go Back
            </a>

            <div class="grid sm:grid-cols-2 gap-x-3 gap-y-3 mt-20">
                <img class="rounded-lg" use:lazy={{src: "https://www.upload.ee/image/16414456/WhatsApp_Go_rsel_2024-03-20_saat_23.52.27_ccf519b5.jpg"}} alt="">
                <img class="rounded-lg" use:lazy={{src: "https://www.upload.ee/image/16443981/WhatsApp_Image_2024-03-28_at_10.09.23.jpeg"}} alt="">
                <img class="rounded-lg" use:lazy={{src: "https://www.upload.ee/image/16444003/WhatsApp_Image_2024-03-28_at_10.17.31.jpeg"}} alt="">
                <img class="rounded-lg" use:lazy={{src: "https://www.upload.ee/image/16444064/cyberpunk-2077-neon-night-city-moewalls-com.gif"}} alt="">
            </div>
        </div>
    </div>
</section>

<Footer />