<script setup>
import medImg from '@/assets/img/caducee.png'
import tameImg from '@/assets/img/ours.png'
import artistImg from '@/assets/img/luth.png'
import enchantImg from '@/assets/img/la-magie.png'
import priestImg from '@/assets/img/prier.png'
import buildImg from '@/assets/img/marteau-a-coup-mort.png'
import slaverImg from '@/assets/img/fouet.png'
import alchiImg from '@/assets/img/fiole.png'
import armorImg from '@/assets/img/armure.png'
import blacksmithImg from '@/assets/img/enclume.png'
import cookImg from '@/assets/img/tavern-sign-svgrepo-com.png'

definePageMeta({
    layout: 'landing',
})

const pricing = [
    {
        price: 'Médecin',
        popular: false,
        link: medImg,
        features: [
            "Le métier de médecin consiste à soigner les blessés, tant personnage non-joueur que personnage joueur, il est le seul à pouvoir remettre complètement les blessés sur pieds le plus rapidement et efficacement possible. Il est le rempart face à la mort. C'est l'un des métiers les plus important pour la survie sur les terres du Hameau.",
        ],
        button: {
            text: 'Get Started',
            link: '/',
        },
    },
    {
        price: 'Eleveur',
        popular: false,
        link: tameImg,
        features: [
            "Le métier d'Eleveur permet la dompte de différentes créatures et bêtes afin d'en faire des alliées fidèles ou de bon gardes. l'Eleveur peut également élevé des animaux afin d'en faire des montures.",
        ],
        button: {
            text: 'Get Started',
            link: '/',
        },
    },
    {
        price: 'Artiste',
        popular: false,
        link: artistImg,
        features: [
            "Les métiers qui tiennent du domaine de l'art et du divertissement consistent à rendre le moral aux autres, les divertir, offrir la joie moyennant finances. Les prouesses offrent des bonus non négligeables aux joueurs et peuvent demander une music box",
        ],
        button: {
            text: 'Get Started',
            link: '/',
        },
    },
    {
        price: 'Enchanteur',
        popular: false,
        link: enchantImg,
        features: [
            "Le métier d'enchanteur consiste à récupérer des gemmes ou pierres magiques afin d'en faire des enchantements divers et variés (Des enchantements hors gameplay peuvent être proposer sur votre suivi afin de possiblement devenir réel en RP !)",
        ],
        button: {
            text: 'Get Started',
            link: '/',
        },
    },
    {
        price: 'Shamane ou Prêtre',
        popular: false,
        link: priestImg,
        features: [
            'Les métiers de prêtre ou de chaman consistent à faire découvrir leurs dieux, leurs foi aux autres tout autant que bénir autrui, faire offrandes à leurs dieux, ôter ou octroyer des malédictions sous le signe de leurs dieux.',
        ],
        button: {
            text: 'Get Started',
            link: '/',
        },
    },
    {
        price: 'Bâtisseur',
        popular: false,
        link: buildImg,
        features: [
            'Le métier de bâtisseur consiste à concevoir des plans de lieux de vie et de les rendre réels. Le bâtisseur conçoit les plans et construit ces plans.',
        ],
        button: {
            text: 'Get Started',
            link: '/',
        },
    },
    {
        price: 'Esclavagiste',
        popular: false,
        link: slaverImg,
        features: [
            "Le métier d'esclavagiste consiste à fabriquer des liens de chaines ou en cordes, des accessoires divers mixant torture, soumission, plaisir sexuel. Ce métier peut également fabriquer des pièges à base de gaz paralysant ou des meubles pour faire travailler les esclaves. Son autre rôle est également de capturer et revendre des esclaves par le biais du marché des esclaves. Il est également le seul à avoir un mental assez dur pour brisé la personne capturée, en faisant un esclave docile qu'il pourra garder ou bien entendu, revendre.",
        ],
        button: {
            text: 'Get Started',
            link: '/',
        },
    },
    {
        price: 'Alchimiste',
        popular: false,
        link: alchiImg,
        features: [
            "Le métier d'alchimiste consiste à confectionner des remèdes, potions, poudres, etc à base de plantes et mineraux, les alchimistes les plus aguerris peuvent idéalement avoir la capacité de soigner autrui grace à leurs produits et de quelques bandages. Certains se font connaître pour fabriquer les meilleurs poisons, d'autres des produits aphrodisiaques. (Ce métier dispose de la possibilité de demander en suivi RP, la création d'une potion RP qui sort du gameplay)",
        ],
        button: {
            text: 'Get Started',
            link: '/',
        },
    },
    {
        price: 'Armurier',
        popular: false,
        link: armorImg,
        features: [
            "Le métier d'Armurier-couturier consiste à forger les armures du jeu ainsi que de les renforcer. Il peut réparer celles-ci ou alors dans un tout autre registre, il peut confectionner des tenues afin de les revendre, que cela aille de la simple couture à la tenue avec des renforts.",
        ],
        button: {
            text: 'Get Started',
            link: '/',
        },
    },
    {
        price: 'Forgeron',
        popular: false,
        link: blacksmithImg,
        features: [
            "Le métier de forgeron consiste à forger toutes les armes et confectionner les arcs ainsi que leurs kit d'amélioration, il peut aussi réparer les armes.",
        ],
        button: {
            text: 'Get Started',
            link: '/',
        },
    },
    {
        price: 'Cuisinier Brasseur',
        popular: false,
        link: cookImg,
        features: [
            'Le métier de cuisinier-brasseur consiste à confectionner tous les plats et boissons du jeu. ',
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
            <template v-slot:title>Métiers</template>
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
