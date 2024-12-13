<script setup>
defineProps(['plan'])
</script>

<template>
    <div>
        <div
            class="flex flex-col w-full order-first lg:order-none border-2 border-[#489d9d25] border-opacity-50 py-5 px-6 rounded-md h-[700px]"
        >
            <div class="flex justify-center mb-4">
                <h4 class="text-lg font-medium text-teal-100 text-center">
                    {{ plan.name }}
                </h4>
            </div>

            <div class="flex justify-center mb-4">
                <img
                    class="rounded-full w-64 h-64 object-contain transition-transform transform hover:scale-125"
                    :src="plan.link"
                    alt="Image description"
                    loading="eager"
                    format="avif"
                />
            </div>

            <p
                class="mt-3 text-4xl font-bold text-teal-50 md:text-4xl text-center"
            >
                {{
                    plan.price && typeof plan.price === 'object'
                        ? plan.price.monthly
                        : plan.price
                }}
            </p>

            <ul class="mt-6 space-y-4 overflow-y-auto">
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
