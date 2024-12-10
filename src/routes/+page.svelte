<script lang="ts">
    import hero from "$lib/images/hero.svg";

    let referenceElement: HTMLElement;
</script>

<section class="min-h-screen   flex flex-col md:flex-row justify-between items-center px-8 py-12 bg-gradient-to-br from-blue-50 to-blue-100">
    <div class="md:w-1/2">
        <h1 class="text-4xl md:text-6xl font-extrabold text-transparent bg-clip-text bg-gradient-to-r from-blue-600 to-teal-400 mb-6 leading-tight">
            Explore the Gospel in the Context of Judgement
        </h1>
        <p class="text-lg md:text-xl text-gray-700 mb-8 leading-relaxed">
            Dive into the book of Daniel and Revelation, uncovering the cosmic conflict and exploring the implications of harmful doctrines.
        </p>
        <button class="bg-blue-600 hover:bg-blue-700 text-white font-semibold py-3 px-6 rounded-lg shadow-md transition-transform transform hover:scale-105">
            <a href="/Explore">
            Explore
            </a>
        </button>
    </div>
    <div class="md:w-1/2 flex justify-center items-center">
        <div class="relative">
            <picture>
                <img
                    bind:this={referenceElement}
                    src={hero}
                    alt="gospel illustration"
                    class="w-[30em] md:w-[40em] h-auto floating-hero object-contain drop-shadow-xl"
                />
            </picture>
            <h2 class="text-gray-600 text-center mt-6 text-lg md:text-xl">
                <strong>Matthew 24:14</strong>: "This gospel of the kingdom will be preached in the whole world."
            </h2>
        </div>
    </div>
</section>

<section class="py-16 bg-gradient-to-br from-blue-50 to-blue-100">
    <h1 class="text-3xl md:text-5xl font-extrabold text-center text-gray-800 leading-tight mb-6">
        The Judgement Between Two Kingdoms
    </h1>
    <p class="text-lg text-gray-600 text-center mb-12">
        The kingdom of heaven consists of its people, while the kingdom of the beast represents the governments of this world.
    </p>
    <div class="max-w-6xl mx-auto grid grid-cols-1 md:grid-cols-3 gap-8">
        <div class="rounded-xl overflow-hidden shadow-lg transition-transform transform hover:scale-105">
            <img src="/06b53174fc4c8998642b532779f9b665.jpg" alt="Kingdom of Heaven" class="w-full h-48 object-cover" />
        </div>
        <div class="flex flex-col items-center justify-center">
            <picture>
                <img src="/Remove-bg.ai_1732478868234.png" alt="Judgement Symbol" class="w-48 h-48 rounded-full shadow-lg" />
            </picture>
        </div>
        <div class="rounded-xl overflow-hidden shadow-lg transition-transform transform hover:scale-105">
            <img src="/8c2e4034ff4ffb27b3992d54428b4edc.jpg" alt="Kingdom of the Beast" class="w-full h-48 object-cover" />
        </div>
    </div>
</section>

<section class="py-16 bg-gradient-to-br from-gray-100 to-gray-200">
    <h1 class="text-3xl md:text-5xl font-extrabold text-center text-gray-800 mb-6">
        Thoughts on the Mark of the Beast
    </h1>
    <p class="text-lg text-gray-600 text-center">
        Explore the implications of the mark of the beast and its relevance to our spiritual journey and choices.
    </p>
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
