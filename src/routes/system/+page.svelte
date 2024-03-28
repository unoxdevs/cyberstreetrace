<script>
    import { onMount } from 'svelte';
    import Footer from '../../components/Footer.svelte';
    import Navbar from '../../components/Navbar.svelte';

    let osOptions = [
        {
            title: 'Windows',
            value: 'windows',
            requiments: {
                memory: '8 GB',
                disk: '45 GB',
                os: 'Windows 10 or higher',
                cpu: 'Intel Core i5 or higher'
            },
            isOpen: false
        },
        {
            title: 'MacOS',
            value: 'macos',
            requiments: {
                memory: '8 GB',
                disk: '45 GB',
                os: 'MacOS',
                cpu: 'Intel Core i5 or higher'
            },
            isOpen: false
        }
    ];

    /**
   * @param {number} index
   */
    function toggleAccordion(index) {
        osOptions = osOptions.map((option, i) => {
            if (i === index) {
                option.isOpen = !option.isOpen;
            } else {
                option.isOpen = false;
            }
            return option;
        });
    }

    onMount(() => {
        osOptions = osOptions.map(option => {
            option.isOpen = false;
            return option;
        });
    });
</script>

<Navbar />

<section class="relative p-5">
    <div class="container mx-auto px-4 md:px-0 grid grid-cols-1 lg:grid-cols-2 items-center gap-x-10 mt-10">
        <div class="text-white">
            <span class="text-sm md:text-base lg:text-base uppercase text-[#627BFF]">What is Needed?</span>
            <h2 class="text-3xl md:text-5xl lg:text-5xl font-bold leading-none py-2">System Requirements</h2>
            <hr class="border-white border-t-2 w-24 py-1">
            <p class="text-base md:text-lg lg:text-lg text-white/70">Lorem ipsum dolor sit amet, consectetur adipiscing elit. In ac nibh finibus, dapibus urna sed, fringilla nibh. Nullam pharetra, odio at malesuada gravida, orci urna laoreet ligula, quis congue sapien magna sed odio.</p>
            <a href="/" class="text-sm font-bold text-white relative top-7 bg-gradient-to-t from-[#5C76FF]/20 to-[#3345AE]/30 border-2 border-[#627BFF] rounded-lg py-2 md:py-3 lg:py-3 px-14">
                <i class="ri-arrow-left-s-line"></i> Go Back
            </a>
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-5 py-10 mt-10">
                {#each osOptions as option, index}
                    <div class="flex flex-col items-start gap-3">
                        <button class="text-xl font-bold focus:outline-none" on:click={() => toggleAccordion(index)}>
                            {option.title}
                            {#if option.isOpen}
                                <i class="ri-arrow-up-s-line"></i>
                            {:else}
                                <i class="ri-arrow-down-s-line"></i>
                            {/if}
                        </button>
                        {#if option.isOpen}
                            <div class="text-lg text-white/70">
                                <p><i class="ri-ram-2-fill"></i> Memory: {option.requiments.memory}</p>
                                <p><i class="ri-hard-drive-3-fill"></i> Disk: {option.requiments.disk}</p>
                                <p><i class="ri-computer-fill"></i> OS: {option.requiments.os}</p>
                                <p><i class="ri-cpu-line"></i> CPU: {option.requiments.cpu}</p>
                            </div>
                        {/if}
                    </div>
                {/each}
            </div>
        </div>
    </div>
</section>

<Footer />
