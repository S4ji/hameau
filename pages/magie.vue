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
            'Comme une étoile naissant dans la nuit, le mage invoque les flammes, les faisant onduler, se tordre et brûler sous son commandement. Chaque étincelle obéit à son souffle, et il sculpte le feu dans des formes infinies, modulant sa chaleur, sa lumière, sa danse dévorante ou délicate à sa volonté.',
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
            "L’eau s'écoule et se transforme, suivant les pensées du mage. Il la guide, la modèle, la fait surgir en torrents ou l'apprivoise en gouttes légères. D’un simple mouvement, il peut faire naître des vagues, des geysers ou des cristaux gelés, chaque éclat de liquide répondant à son appel.",
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
            'La terre et les plantes répondent à l’appel du mage, leurs racines s’étendant sous ses pieds. Il façonne le sol et les roches, modelant des montagnes ou faisant surgir des forêts entières. En touchant la terre, il fait croître des plantes, les tord et les élève, sculptant la nature elle-même, reliant chaque élément à sa volonté.',
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
            'L’air se courbe et se plie à la volonté du mage, léger comme un murmure ou puissant comme un cyclone. Il manipule les vents, modifiant leur direction, leur pression, leur vitesse, créant des tourments ou des silences apaisants. L’atmosphère devient une toile, sur laquelle il peint avec l’invisible.',
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
            'permettant d’influencer la vaste majorité de ce qui touche à l’Esprit. Rares sont ceux pratiquant cette forme de Magie, car elle demande bien plus de temps d’étude et de pratique pour en développer les capacités. Cette forme de Magie, que certains nomment “Arcanes” ou “Magie de l’Esprit”, est néanmoins l’une des plus vastes qui existe et beaucoup de ses secrets sont encore à découvrir.',
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
            'capable d’énormément de choses en faisant usage de l’énergie vitale. Certains nomment cela “Magie du Sang”, d’autres poussent leurs expériences vers la Nécromancie.',
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
            'ce que beaucoup peuvent nommer “Magie Divine”. Lumière et Ténèbres réunies en un tout complexe et sensible.',
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
                    En arrivant, vous predez tous vos pouvoirs.. Pourtant, vous
                    pouvez ressentir quelque chose, d'étrange, propre à
                    l'endroit ou vous êtes arrivés..
                </p></template
            >
        </LandingSectionhead>

        <div class="grid md:grid-cols-2 gap-4 mx-auto max-w-screen-lg mt-4">
            <LandingCard v-for="item of pricing" :plan="item" />
        </div>
    </LandingContainer>
</template>
