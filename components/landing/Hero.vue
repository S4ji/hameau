<script setup>
const rulesUrl = '/reglement'
</script>

<template>
    <main class="grid lg:grid-cols-2 place-items-center pt-16 md:pt-8">
        <div class="p-24 md:order-1 hidden md:block">
            <img
                class="rounded-full transition-transform transform hover:scale-125"
                src="~/assets/img/Hameau.jpg"
                alt="Starship starts the engine"
                loading="eager"
                format="avif"
                width="512"
                height="512"
            />
        </div>

        <div>
            <h1
                class="text-5xl lg:text-6xl xl:text-7xl font-bold lg:tracking-tight"
            >
                Le Hameau [FR] +18 RP/PVP/PVE
            </h1>
            <p class="text-lg mt-4 text-slate-300 max-w-xl">
                Serveur dédié Conan Exiles 35 Slots évolutifs. Prenez part à
                cette aventure, entourés d'un staff à l'écoute de vos projets
                RP, d'une carte en constante évolution selon vos choix.
            </p>
            <div class="mt-6 flex flex-col sm:flex-row gap-3">
                <LandingLink
                    target="_blank"
                    rel="noopener"
                    href="https://discord.gg/fvC4sz8yZd"
                    >Nous Rejoindre</LandingLink
                >
                <LandingLink
                    size="lg"
                    styleName="outline"
                    rel="noopener"
                    :href="rulesUrl"
                    >Lire le Règlement</LandingLink
                >
            </div>
        </div>
    </main>
</template>
