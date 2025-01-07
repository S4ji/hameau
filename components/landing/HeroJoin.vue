<script setup>
const rulesUrl = '/reglement'
</script>

<template>
    <main
        class="flex flex-col items-center justify-center min-h-screen px-4 lg:px-8"
    >
        <div class="text-center max-w-3xl">
            <h1
                class="text-5xl lg:text-6xl xl:text-7xl font-bold tracking-tight"
            >
                Pour nous rejoindre
            </h1>
            <p class="text-lg mt-6 text-slate-300">
                Suivez bien les étapes suivantes :
            </p>
            <ul class="mt-8 space-y-6 text-left">
                <li>
                    - Lors de votre arrivée sur le discord, vous devrez dans un
                    premier temps lire les deux règlements, afin d'être dans les
                    normes, il sera demandé de valider votre lecture du
                    règlement rp en cliquant sur la réaction 👀. Cette action
                    déterminera le fait que le règlement est lu même si durant
                    la candidature, il est demandé de dire si vous acceptez
                    celui-ci.
                </li>
                <li>
                    - Une fois les règlements lus, il ne vous restera plus qu'à
                    déposer votre candidature dans un ticket prévu à cet effet,
                    celui parlant de création de personnage. L'intitulé de ce
                    ticket offre la totalité des informations à donner afin
                    d'avoir vos entrées sur le serveur.
                </li>
                <li>
                    - Le serveur étant multivers, le guide des races n'est là
                    que pour aider en cas d'hésitation sur la création du
                    personnage. Si vous avez déjà en tête le personnage voulu,
                    alors ce guide ne servira pas plus que cela à votre
                    candidature.
                </li>
                <li>
                    - Étant Multivers, vous pouvez alors proposer un personnage
                    de votre propre lore, d'un lore Conan classique, voir de
                    l'univers de The Age of Calamitous, Warhammer, Dark Souls,
                    etc. Tout univers ou presque est autorisé tant qu'il ne
                    s'agit pas d'un univers ultra futuriste qui serait
                    complètement étrange voire incohérent à adapter au jeu et au
                    serveur.
                </li>
                <li>
                    - Une fois ceci fait, la réponse suite à votre candidature
                    sera donnée sous peu. Vous pourrez alors disposer des
                    informations de connexion au serveur afin de débuter votre
                    aventure qui sera guidée dans un premier temps, HRP puis RP.
                    En ayant pris connaissance du lore écrit sur le Discord,
                    vous serez alors en mesure de découvrir l'univers du Hameau.
                </li>
                <li>
                    - Il est important également de prendre connaissance de la
                    carte des terres qui permet une mise au point régulière sur
                    l'avancée des joueurs dans la libération des terres. Il y
                    est aussi stipulé que vous pouvez tenter le diable et vivre
                    par-delà la brume. Si tel est le cas, vous acceptez
                    automatiquement d'avoir un personnage en grand danger, que
                    ce soit des PNJ ou même des antagonistes joueurs.
                </li>
                <li>
                    En cas de question spécifique, une catégorie d'ouverture de
                    ticket concerne les demandes de questions. N'hésitez pas à
                    en ouvrir un en parallèle de votre ticket de personnage.
                </li>
            </ul>
            <div class="mt-10 flex flex-col sm:flex-row justify-center gap-6">
                <LandingLink
                    href="https://discord.gg/fvC4sz8yZd
"
                    target="_blank"
                    rel="noopener"
                    class="py-3 px-6 text-lg font-semibold bg-indigo-600 text-white rounded-lg shadow hover:bg-indigo-500"
                >
                    Rejoindre le discord
                </LandingLink>
                <LandingLink
                    size="lg"
                    styleName="outline"
                    rel="noopener"
                    :href="rulesUrl"
                    class="py-3 px-6 text-lg font-semibold hover:bg-transparent hover:text-white"
                >
                    Lire le Règlement
                </LandingLink>
            </div>
        </div>
    </main>
</template>
