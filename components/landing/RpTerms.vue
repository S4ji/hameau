<template>
    <ul
        class="space-y-4 text-gray-500 list-disc list-inside dark:text-gray-400"
    >
        <li v-for="(rule, term) in rules" :key="term">
            <strong>{{ term }}</strong> : {{ rule.definition }}
            <!-- Check if there are sub-rules (nested items) -->
            <ul
                v-if="rule.subRules"
                class="ps-5 mt-2 space-y-1 list-disc list-inside"
            >
                <li
                    v-for="(subRule, subIndex) in rule.subRules"
                    :key="subIndex"
                >
                    {{ subRule }}
                </li>
            </ul>
        </li>
    </ul>
</template>

<script setup>
// Define props for the component
defineProps({
    rules: {
        type: Object,
        required: true,
    },
})
</script>

<style scoped>
/* Additional styling, if necessary */
</style>
