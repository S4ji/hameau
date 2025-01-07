<script setup>
const features = [
    {
        title: 'Devenez un des survivants, à la conquête du continent !',
        description:
            "Une dynamique d'exploration originale, le but est de débloquer la carte au fur et à mesure des intrigues qui se dessinnent",
        icon: 'bx:bxs-file-find',
    },
    {
        title: 'Map Savage Wilds',
        description:
            'Venez découvrir la célèbre map moddée, revisitée par nos soins avec Murun comme centre urbain !',
        icon: 'bx:bxs-briefcase',
    },
    {
        title: 'Multivers',
        description:
            "Son multivers vous permet l'introduction de votre propre lore ou d'un lore déjà connu.",
        icon: 'bx:bxs-window-alt',
    },
    {
        title: 'Mise en valeurs de vos projets',
        description:
            'Nous écoutons vos projets RP dans ce serveur où seules vos actions feront évoluer les terres. Notre système de projet RP vous permet de proposer vos idées et à nous de les suivres !',
        icon: 'bx:bxs-data',
    },
    {
        title: 'Trouvez votre place !',
        description:
            " Devenez mage, guerrier ou voleur, tout le monde trouve sa place, même les grands méchants pourront s'amuser !",
        icon: 'bx:bxs-bot',
    },
    {
        title: 'Slots évolutifs',
        description:
            "Serveur dédié 35 slots avec possibilité de passer à 40 à n'importe quel instant.",
        icon: 'bx:bxs-briefcase',
    },
]
</script>

<template>
    <div>
        <div class="mt-16 md:mt-0">
            <h2 class="text-4xl lg:text-5xl font-bold lg:tracking-tight">
                Serveur RP écrit
            </h2>
            <p class="text-lg mt-4 text-slate-300">
                Dans un paysage sauvage et mystique, où la nature oscille entre
                majesté et cruauté, une force ancienne et insaisissable réside.
                Jadis prospère, ce royaume est maintenant corrompu par un mal
                indicible qui transforme des créatures pacifiques en prédateurs
                féroces et engendre des monstres terrifiants. Des étrangers,
                dépouillés de leurs pouvoirs et transportés dans cet univers
                hostile par un portail mystérieux, se retrouvent piégés sans
                espoir de retour.
            </p>
        </div>
        <div class="grid sm:grid-cols-2 md:grid-cols-3 mt-16 gap-16">
            <div v-for="item of features" class="flex gap-4 items-start">
                <div class="mt-1 bg-black rounded-full p-2 w-8 h-8 shrink-0">
                    <Icon class="text-white" :name="item.icon" />
                </div>
                <div>
                    <h3 class="font-semibold text-lg">{{ item.title }}</h3>
                    <p class="text-slate-300 mt-2 leading-relaxed">
                        {{ item.description }}
                    </p>
                </div>
            </div>
        </div>
    </div>
</template>
