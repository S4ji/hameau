<template>
    <LandingSectionhead>
        <template v-slot:title>Notre équipe</template>
        <template v-slot:desc>Une petite équipe de passionnés</template>
    </LandingSectionhead>

    <div class="grid md:grid-cols-5 gap-10 mx-auto max-w-4xl mt-12">
        <div v-for="item of team" class="group">
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

            <div class="mt-4 text-center">
                <h2 class="text-lg text-teal-100">{{ item.name }}</h2>
                <h3 class="text-sm text-teal-500">{{ item.title }}</h3>
            </div>
        </div>
    </div>
</template>

<script lang="ts" setup>
import aela from '@/assets/img/aela.jpg'
import shaylfer from '@/assets/img/Shaylfer.png'
import soryu from '@/assets/img/soryu.png'
import sutekh from '@/assets/img/sutekh.jpg'
import elyria from '@/assets/img/Elyria.png'
import alka from '@/assets/img/alka.jpeg'
import maxhos from '@/assets/img/maxhos.webp'
import katelyn from '@/assets/img/katelyn.webp'
import yuci from '@/assets/img/yuci.jpg'
import edwin from '@/assets/img/edwin.png'

const team = [
    {
        name: 'Fonda',
        title: 'Fondateur',
        description: '',
        avatar: {
            src: aela,
            width: 480,
            height: 560,
        },
    },
    {
        name: 'Shaylfer',
        title: 'Modérateur',
        description: '',
        avatar: {
            src: shaylfer,
            width: 480,
            height: 560,
        },
    },
    {
        name: 'Maxhos',
        title: 'Modérateur',
        description: '',
        avatar: {
            src: maxhos,
            width: 480,
            height: 560,
        },
    },
    {
        name: 'Alkaéna',
        title: 'Helper',
        description: '',
        avatar: {
            src: alka,
            width: 480,
            height: 560,
        },
    },
    {
        name: 'Elyria',
        title: 'Helper',
        description: '',
        avatar: {
            src: elyria,
            width: 480,
            height: 560,
        },
    },
    {
        name: 'Yuci',
        title: 'Helper',
        description: '',
        avatar: {
            src: yuci,
            width: 480,
            height: 560,
        },
    },
    {
        name: 'Sutekh',
        title: 'Animateur',
        description: '',
        avatar: {
            src: sutekh,
            width: 480,
            height: 560,
        },
    },
    {
        name: 'Kate',
        title: 'Animateur',
        description: '',
        avatar: {
            src: katelyn,
            width: 480,
            height: 560,
        },
    },
    {
        name: 'Dame Soryü',
        title: 'Animateur',
        description: '',
        avatar: {
            src: soryu,
            width: 480,
            height: 560,
        },
    },
    {
        name: 'Edwin',
        title: 'Animateur',
        description: '',
        avatar: {
            src: edwin,
            width: 480,
            height: 560,
        },
    },
]
</script>

<style></style>
