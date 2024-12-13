<script setup>
definePageMeta({
    layout: 'landing',
})

const pricing = [
    {
        price: 'Humains',
        popular: false,
        link: 'testurl',
        features: [
            "La race la plus commune sur les terres du Hameau, leur capacité à repousser l'échéance est telle qu'ils peuvent se sortir des situations les plus dangereuses, ils possèdent un 'second souffle' qui leur permet de régénérer une partie de leur santé, de devenir plus résistants à la douleur et de se déplacer plus vite et plus longtemps lorsque la situation est critique",
        ],
        button: {
            text: 'Get Started',
            link: '/',
        },
    },
    {
        price: 'Elfes',
        popular: false,
        link: 'testurl',
        features: [
            "Une race ayant une affinité pour la magie, ils sont capables de voir dans l'obscurité, sont un peu plus endurants et sont capables de lancer des sortilèges de manière plus efficace que les autres race (Bonus stamina max et bonus dégâts de sorts Indrid)",
        ],
        button: {
            text: 'Get Started',
            link: '/',
        },
    },
    {
        price: 'Orcs',
        popular: false,
        link: 'testurl',
        features: [
            'Une race de guerrier brutaux et sanguinaires, ils possèdent une résistance naturelle plus élevée que les autres races, ce qui leur permet de combattre plus longtemps.',
        ],
        button: {
            text: 'Get Started',
            link: '/',
        },
    },
    {
        price: 'Nains',
        popular: false,
        link: 'testurl',
        features: [
            "Une race de travailleurs forcenés, adorant les mines et les montagnes, ils sont naturellement plus résistant que d'autre races et peuvent voir dans l'obscurité",
        ],
        button: {
            text: 'Get Started',
            link: '/',
        },
    },
    {
        price: 'Anges',
        popular: false,
        link: 'testurl',
        features: [
            "Des êtres célestes de lumière pure, ils ne peuvent être corrompus, ont la capacité de voler, et sont capable de voir dans l'obscurité",
        ],
        button: {
            text: 'Get Started',
            link: '/',
        },
    },
    {
        price: 'Démons',
        popular: false,
        link: 'testurl',
        features: [
            "Des êtres venus des profondeurs des enfers, ils adorent tourmenter les mortels et ont ces derniers comme mets favoris, ils peuvent dévorer n'importe quel cadavre pour devenir plus résistants, sont capables de voler, de voir dans l'obscurité, et sont invulnérables aux chaleurs extrêmes.",
        ],
        button: {
            text: 'Get Started',
            link: '/',
        },
    },
    {
        price: 'Vampires',
        popular: false,
        link: 'testurl',
        features: [
            "Des êtres considérés comme immortels (mais intemporels dans les faits), ils n'ont besoin de se nourrir que de sang, ils en ont besoin pour survivre, ils ont la capacité de se transformer en une immonde créature, certains ont la capacité de vol, ils peuvent se soigner via les blessures qu'ils infligent, sont capable de voir dans la nuit et ne peuvent être noyés de par le fait qu'ils ne respirent pas.",
        ],
        button: {
            text: 'Get Started',
            link: '/',
        },
    },
    {
        price: 'Lycans',
        popular: false,
        link: 'testurl',
        features: [
            "Les ennemis mortels des vampires, ces derniers peuvent se transformer en d'immondes créature mi-homme, mi-loup, leurs griffes acérés peuvent se montrer redoutables, ils sont capable de se nourrir sur n'importe quelle créature, ils ont des jambes leur permettant des sauts d'une hauteur inégalée, et possèdent des réflexes identiques à leur vitesse.",
        ],
        button: {
            text: 'Get Started',
            link: '/',
        },
    },
    {
        price: 'Créatures des abysses',
        popular: false,
        link: 'testurl',
        features: [
            "Toute créature vivant dans les profondeurs des mers les plus hostiles, ils sont naturellement amphibiens, sont capable de voir dans l'obscurité totale des profondeurs, et sont immunisés aux climats les plus froids.",
        ],
        button: {
            text: 'Get Started',
            link: '/',
        },
    },
    {
        price: 'Gobelins',
        popular: false,
        link: 'testurl',
        features: [
            ' Une race de petites créatures sauvages et agile, ayant un appétit vorace. Ils peuvent aussi voir dans la nuit, et sont infatigables',
        ],
        button: {
            text: 'Get Started',
            link: '/',
        },
    },
    {
        price: 'Changeformes',
        popular: false,
        link: 'testurl',
        features: [
            "Tout ceux ayant la capacité de se transformer en divers animaux se regroupent ici. Ils sont de nature plutôt pacifiste, mais sont capable, dans les situations délicate, de s'enfuir ou de combattre de manière plus véloce. En fonction de l'animal qu'ils prennent comme forme, ils peuvent voir dans l'obscurité.",
        ],
        button: {
            text: 'Get Started',
            link: '/',
        },
    },
    {
        price: 'Dragonoïdes',
        popular: false,
        link: 'testurl',
        features: [
            "Une race de créatures puissantes, nobles, naturellement plus résistantes que les autres races, ayant la capacité de vol, d'alterner entre leur forme humaine et draconnique, ils peuvent se renforcer selon leur état de satiété, et sont capable de s'adapter à tout climat.",
        ],
        button: {
            text: 'Get Started',
            link: '/',
        },
    },
    {
        price: 'Créatures Spirituelles',
        popular: false,
        link: 'testurl',
        features: [
            "Divers esprits peuplent cette catégorie, il peuvent se transformer, voir dans le noir, et s'adapter à tout type de climat",
        ],
        button: {
            text: 'Get Started',
            link: '/',
        },
    },
]
</script>

<template>
    <LandingContainer>
        <LandingSectionhead>
            <template v-slot:title>Races</template>
            <template v-slot:desc
                ><p class="text-teal-100">
                    Grâce à Indrid, de nombreuses races sont accessibles, avec
                    leur bonus au niveau du gameplay.
                </p></template
            >
        </LandingSectionhead>

        <div class="grid md:grid-cols-3 gap-4 mx-auto max-w-screen-lg mt-4">
            <LandingCard v-for="item of pricing" :plan="item" />
        </div>
    </LandingContainer>
</template>
