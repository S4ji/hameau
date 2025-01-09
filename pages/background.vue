<script setup>
definePageMeta({
    layout: 'landing',
})

import plaine1 from '@/assets/img/plaine1.png'
import plaine2 from '@/assets/img/plaine2.png'
import plaine3 from '@/assets/img/plaine3.png'
import night1 from '@/assets/img/night1.png'
import night2 from '@/assets/img/night3.png'
import night3 from '@/assets/img/night4.png'
import civ1 from '@/assets/img/villagedruidesse.png'
import civ2 from '@/assets/img/murun2.png'
import civ3 from '@/assets/img/hameau.png'

const band1 = [
    {
        avatar: {
            src: plaine1,
            width: 480,
            height: 560,
        },
    },
    {
        avatar: {
            src: plaine2,
            width: 480,
            height: 560,
        },
    },
    {
        avatar: {
            src: plaine3,
            width: 480,
            height: 560,
        },
    },
]
const band2 = [
    {
        avatar: {
            src: night1,
            width: 480,
            height: 560,
        },
    },
    {
        avatar: {
            src: night2,
            width: 480,
            height: 560,
        },
    },
    {
        avatar: {
            src: night3,
            width: 480,
            height: 560,
        },
    },
]
const band3 = [
    {
        avatar: {
            src: civ1,
            width: 480,
            height: 560,
        },
    },
    {
        avatar: {
            src: civ2,
            width: 480,
            height: 560,
        },
    },
    {
        avatar: {
            src: civ3,
            width: 480,
            height: 560,
        },
    },
]
</script>

<template>
    <LandingContainer>
        <LandingSectionhead>
            <template v-slot:title>Lore du serveur </template>
            <template v-slot:desc>
                <p class="pb-4">
                    C'est dans ce décor sombre et énigmatique que se déroule le
                    destin des nouveaux venus, cherchant à s'adapter, à percer
                    les secrets des terres sauvages et, peut-être, à retrouver
                    un jour leur foyer.
                </p>
                <div class="grid md:grid-cols-3 gap-10 mx-auto max-w-4xl mt-12">
                    <div v-for="item of band1" class="group">
                        <div class="w-full aspect-square">
                            <img
                                :src="item.avatar.src"
                                :width="item.avatar.width"
                                :height="item.avatar.height"
                                format="avif"
                                alt="Team"
                                class="w-full h-full object-cover rounded transition group-hover:-translate-y-1 group-hover:shadow-xl"
                            />
                        </div>
                    </div>
                </div>
                <p class="text-teal-100 text-justify pb-4">
                    Dans les profondeurs des terres sauvages, là où les horizons
                    s'étirent à perte de vue et où la brume épaisse enveloppe
                    tout comme un voile mystérieux, une force ancienne et
                    insondable réside. C'est un royaume où la nature est à la
                    fois majestueuse et cruelle, où les échos du passé résonnent
                    dans chaque souffle de vent et chaque frémissement des
                    feuilles.
                </p>

                <p class="text-teal-100 text-justify pb-4">
                    Des légendes parlent de ce lieu comme d'une terre autrefois
                    prospère, où les hommes et les bêtes coexistaient en
                    harmonie, mais quelque chose a changé. Un mal indicible
                    s'est éveillé, se répandant lentement mais inexorablement à
                    travers les terres sauvages, corrompant tout sur son
                    passage. Des créatures autrefois paisibles sont devenues des
                    prédateurs féroces, tandis que des abominations monstrueuses
                    errent dans l'obscurité.
                </p>

                <div class="grid md:grid-cols-3 gap-10 mx-auto max-w-4xl mt-12">
                    <div v-for="item of band2" class="group">
                        <div class="w-full aspect-square">
                            <img
                                :src="item.avatar.src"
                                :width="item.avatar.width"
                                :height="item.avatar.height"
                                format="avif"
                                alt="Team"
                                class="w-full h-full object-cover rounded transition group-hover:-translate-y-1 group-hover:shadow-xl"
                            />
                        </div>
                    </div>
                </div>

                <p class="text-teal-100 text-justify pb-4">
                    Les nouveaux arrivants, arrachés à leur monde par un portail
                    mystérieux leurs prenant tous leurs pouvoirs et précipités
                    dans cet univers inhospitalier, se retrouvent désormais
                    confrontés à un destin incertain. Le portail, une fois
                    franchi, se referme irrémédiablement, condamnant les
                    voyageurs à demeurer dans les terres sauvages sans espoir de
                    retour.
                </p>

                <p class="text-teal-100 text-justify pb-4">
                    Par chance, un hameau isolé se dresse au cœur de ce chaos,
                    offrant un refuge temporaire pour ceux qui osent s'aventurer
                    dans ces contrées dangereuses. Dernière barrière fragile
                    contre les menaces qui rôdent au-dehors. Mais même là, la
                    sécurité est précaire, car les forces du mal ne sont jamais
                    loin, guettant le moment propice pour frapper.
                </p>

                <div class="grid md:grid-cols-3 gap-10 mx-auto max-w-4xl mt-12">
                    <div v-for="item of band3" class="group">
                        <div class="w-full aspect-square">
                            <img
                                :src="item.avatar.src"
                                :width="item.avatar.width"
                                :height="item.avatar.height"
                                format="avif"
                                alt="Team"
                                class="w-full h-full object-cover rounded transition group-hover:-translate-y-1 group-hover:shadow-xl"
                            />
                        </div>
                    </div>
                </div>

                <p class="text-teal-100 text-justify pb-4">
                    Les habitants du hameau vivent dans la crainte constante,
                    sachant que chaque jour pourrait être leur dernier.
                    Pourtant, ils se battent pour survivre, s'accrochant à
                    l'espoir que peut-être, un jour, ils trouveront un moyen de
                    lever la malédiction qui les retient captifs dans les terres
                    sauvages.
                </p>

                <p class="text-teal-100 text-justify pb-4">
                    C'est dans ce décor sombre et mystérieux que se joue le
                    destin des nouveaux arrivants, alors qu'ils luttent pour
                    s'adapter à leur nouvel environnement, découvrir les secrets
                    cachés des terres sauvages et peut-être, un jour, trouver un
                    moyen de rentrer chez eux.
                </p>
            </template>
        </LandingSectionhead>
    </LandingContainer>
</template>
