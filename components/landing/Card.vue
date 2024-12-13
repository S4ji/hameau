<script setup>
defineProps(['plan'])
</script>

<template>
    <div>
        <div
            class="flex flex-col w-full order-first lg:order-none border-2 border-[#489d9d25] border-opacity-50 py-5 px-6 rounded-md h-[700px]"
        >
            <div class="flex flex-col items-center justify-between flex-grow">
                <h4 class="text-lg font-medium text-teal-100 mb-4 text-center">
                    {{ plan.name }}
                </h4>

                <div class="flex justify-center mb-4">
                    <img
                        class="rounded-full w-48 h-48 object-contain transition-transform transform hover:scale-125"
                        :src="plan.link"
                        alt="Starship starts the engine"
                        loading="eager"
                        format="avif"
                    />
                </div>

                <p class="mt-3 text-4xl font-bold text-teal-50 md:text-4xl">
                    {{
                        plan.price && typeof plan.price === 'object'
                            ? plan.price.monthly
                            : plan.price
                    }}
                </p>
            </div>

            <!-- Features List -->
            <ul class="mt-8 space-y-4 flex-grow overflow-y-auto">
                <li
                    v-for="item of plan.features"
                    class="flex items-start gap-3 text-teal-100"
                >
                    <LandingTick class="w-6 h-6" />
                    <span>{{ item }}</span>
                </li>
            </ul>
        </div>
    </div>
</template>
