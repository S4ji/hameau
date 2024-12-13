<script setup>
definePageMeta({
    layout: 'landing',
})

import fireImg from '@/assets/img/Fire.png'
import waterImg from '@/assets/img/wa.png'
import groundImg from '@/assets/img/ground.png'
import airImg from '@/assets/img/air.png'
import arcaneImg from '@/assets/img/arcane.png'
import bloodImg from '@/assets/img/blood.png'
import divineImg from '@/assets/img/divine.png'

const pricing = [
    {
        price: 'Feu',
        popular: false,
        link: fireImg,
        features: [
            "Le métier de médecin consiste à soigner les blessés, tant personnage non-joueur que personnage joueur, il est le seul à pouvoir remettre complètement les blessés sur pieds le plus rapidement et efficacement possible. Il est le rempart face à la mort. C'est l'un des métiers les plus important pour la survie sur les terres du Hameau.",
        ],
        button: {
            text: 'Get Started',
            link: '/',
        },
    },
    {
        price: 'Eau',
        popular: false,
        link: waterImg,
        features: [
            "Le métier d'Eleveur permet la dompte de différentes créatures et bêtes afin d'en faire des alliées fidèles ou de bon gardes. l'Eleveur peut également élevé des animaux afin d'en faire des montures.",
        ],
        button: {
            text: 'Get Started',
            link: '/',
        },
    },
    {
        price: 'Terre',
        popular: false,
        link: groundImg,
        features: [
            "Les métiers qui tiennent du domaine de l'art et du divertissement consistent à rendre le moral aux autres, les divertir, offrir la joie moyennant finances. Les prouesses offrent des bonus non négligeables aux joueurs et peuvent demander une music box",
        ],
        button: {
            text: 'Get Started',
            link: '/',
        },
    },
    {
        price: 'Air',
        popular: false,
        link: airImg,
        features: [
            "Le métier d'enchanteur consiste à récupérer des gemmes ou pierres magiques afin d'en faire des enchantements divers et variés (Des enchantements hors gameplay peuvent être proposer sur votre suivi afin de possiblement devenir réel en RP !)",
        ],
        button: {
            text: 'Get Started',
            link: '/',
        },
    },
    {
        price: 'Arcanes',
        popular: false,
        link: arcaneImg,
        features: [
            'Les métiers de prêtre ou de chaman consistent à faire découvrir leurs dieux, leurs foi aux autres tout autant que bénir autrui, faire offrandes à leurs dieux, ôter ou octroyer des malédictions sous le signe de leurs dieux.',
        ],
        button: {
            text: 'Get Started',
            link: '/',
        },
    },
    {
        price: 'Sang',
        popular: false,
        link: bloodImg,
        features: [
            'Les métiers de prêtre ou de chaman consistent à faire découvrir leurs dieux, leurs foi aux autres tout autant que bénir autrui, faire offrandes à leurs dieux, ôter ou octroyer des malédictions sous le signe de leurs dieux.',
        ],
        button: {
            text: 'Get Started',
            link: '/',
        },
    },
    {
        price: 'Divin',
        popular: false,
        link: divineImg,
        features: [
            'Les métiers de prêtre ou de chaman consistent à faire découvrir leurs dieux, leurs foi aux autres tout autant que bénir autrui, faire offrandes à leurs dieux, ôter ou octroyer des malédictions sous le signe de leurs dieux.',
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
            <template v-slot:title>Magie</template>
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
