<script lang="ts">
    import hero from "$lib/images/hero.svg";

    let referenceElement: HTMLElement;
    
    
</script>

<section class="min-h-screen mt-12 flex flex-col md:flex-row justify-center items-center p-8">
    <div class="md:w-1/2 text-left ">
        <h1 class="text-3xl md:text-6xl font-bold text-gray-800 mb-6 leading-tight text-left">
            Explore the gospel in the context of the Judgement.
        </h1>
        <h1 class=" w-full md:w-2/3 text-xl text-black mb-4 leading-snug text-left">
            We will be going through the book of Daniel and the book of Revelation,the background of the cosmic conflict and the implications of harmful doctrines.
        </h1>
        <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
            Explre
        </button>
        
    </div>
    <div class="md:w-1/2 flex justify-center items-center ">
        <div class="relative">
            <h1 class=" text-gray-700 mb-4 leading-snug">
                <span class="welcome inline-block ">
                    <picture>
                        <img
                            bind:this={referenceElement}
                            src={hero}
                            alt="gospel illustration"
                            class="w-[30em] h-[12em] floating-hero  object-contain"
                        />
                    </picture>
                </span>
                <br />This gospel of the kingdom will be <br /> preached in the whole world
            </h1>
            <h2 class=" text-gray-600 mt-4 text-center ">
                <strong>Matthew 24:14</strong>
            </h2>
        </div>
    </div>
</section>
<section class="py-8 md:py-20">
     <h1 class="text-2xl text-black md:text-3xl font-bold tracking-tighter sm:text-5xl mt-6">
        See why the theam of the book of Daniel and  the book of <br/> Revelation is Judgement betewwn two kingdoms.
    </h1>
    <h3 class=" text-black  text-center">
        The kingdom of heaven is made up of the poeple in it, and the kingdom of <br/>  the beast is made up of the governments of this world.
    </h3>
    <div class="w-full md:w-[80rem] mx-auto rounded-xl">
        <div class="flex justify-between">
            <div class="rounded-xl w-[30rem]">
                <img
                    src="/06b53174fc4c8998642b532779f9b665.jpg"
                    alt=""
                    class="w-full h-full object-cover"
                />
            </div>
            <div class="w-[30rem] flex self-center flex-col">
                <picture class="flex justify-center">
                    <img src="/Remove-bg.ai_1732478868234.png" alt="" class="w-48 h-48" />
                </picture>
            </div>
            <div class="flex justify-between">
                <div class="rounded-xl w-[30rem]">
                    <img
                        src="/8c2e4034ff4ffb27b3992d54428b4edc.jpg"
                        alt=""
                        class="w-full h-full object-cover"
                    />
                </div>
            </div>
        </div>
    </div>
</section>
<section class="py-8 md:py-20">
     <h1 class="text-2xl text-black md:text-3xl font-bold tracking-tighter sm:text-5xl mt-6">
        Thoughts on the Mart of the Beast
    </h1>
    
    
</section>


<style>
    .floating-hero {
        animation: float 3s ease-in-out infinite;
    }

    @keyframes float {
        0% {
            transform: translateY(0px);
        }
        50% {
            transform: translateY(-20px);
        }
        100% {
            transform: translateY(0px);
        }
    }
</style>


