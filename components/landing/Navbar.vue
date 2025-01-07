<script setup>
const menuitems = [
    {
        title: 'Accueil',
        path: '/',
    },
    {
        title: 'Règlement',
        path: '/reglement',
    },
    {
        title: 'Lore du serveur',
        path: '/background',
        icon: 'entypo:arrow-down', // Icon for lore

        children: [
            {
                title: 'Races',
                path: '/races',
            },
            {
                title: 'Métiers',
                path: '/metier',
            },
            {
                title: 'Magie',
                path: '/magie',
            },
        ],
    },
    {
        title: 'Notre équipe',
        path: '/equipe',
    },
    {
        title: 'Nous rejoindre',
        path: '/nousrejoindre',
    },
]

import logo from '@/assets/img/logohameau.png'

const open = ref(false)
</script>

<template>
    <LandingContainer>
        <header
            class="flex flex-col lg:flex-row justify-between items-center my-5"
        >
            <div class="flex w-full lg:w-auto items-center justify-between">
                <a href="/" class="text-lg">
                    <img :src="logo" alt="" width="100" height="120" />
                </a>
                <div class="block lg:hidden">
                    <button @click="open = !open" class="text-gray-800">
                        <svg
                            fill="currentColor"
                            class="w-4 h-4"
                            viewBox="0 0 20 20"
                            xmlns="http://www.w3.org/2000/svg"
                        >
                            <title>Menu</title>
                            <path
                                v-show="open"
                                fill-rule="evenodd"
                                clip-rule="evenodd"
                                d="M18.278 16.864a1 1 0 01-1.414 1.414l-4.829-4.828-4.828 4.828a1 1 0 01-1.414-1.414l4.828-4.829-4.828-4.828a1 1 0 011.414-1.414l4.829 4.828 4.828-4.828a1 1 0 111.414 1.414l-4.828 4.829 4.828 4.828z"
                            ></path>
                            <path
                                v-show="!open"
                                fill-rule="evenodd"
                                d="M4 5h16a1 1 0 010 2H4a1 1 0 110-2zm0 6h16a1 1 0 010 2H4a1 1 0 010-2zm0 6h16a1 1 0 010 2H4a1 1 0 010-2z"
                            ></path>
                        </svg>
                    </button>
                </div>
            </div>
            <nav
                class="w-full lg:w-auto mt-2 lg:flex lg:mt-0"
                :class="{ block: open, hidden: !open }"
            >
                <ul class="flex flex-col lg:flex-row lg:gap-3">
                    <li
                        v-for="item of menuitems"
                        :key="item.title"
                        class="relative group"
                    >
                        <a
                            :href="item.path"
                            class="flex items-center justify-center lg:px-3 py-2 text-teal-50 hover:text-cyan-100"
                        >
                            <span class="flex items-center">
                                {{ item.title }}
                                <Icon
                                    class="ml-2 text-white"
                                    :name="item.icon"
                                />
                            </span>
                        </a>
                        <!-- Submenu centered -->
                        <ul
                            v-if="item.children"
                            class="absolute right-4 transform -translate-x-1/2 top-full hidden group-hover:block"
                        >
                            <li
                                v-for="subItem of item.children"
                                :key="subItem.title"
                                class="bg-white text-teal-950"
                            >
                                <a
                                    :href="subItem.path"
                                    class="block text-teal-950 hover:text-teal-50 hover:bg-teal-950 p-2"
                                >
                                    {{ subItem.title }}
                                </a>
                            </li>
                        </ul>
                    </li>
                </ul>
            </nav>
        </header>
    </LandingContainer>
</template>
