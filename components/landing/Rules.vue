<template>
    <ol
        class="space-y-4 text-gray-500 list-decimal list-inside dark:text-gray-400"
    >
        <li v-for="(rule, index) in rules" :key="index">
            <strong>{{ rule.term }}</strong> : {{ rule.definition }}
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
    </ol>
</template>

<script setup>
// Define props for the component
defineProps({
    rules: {
        type: Array,
        required: true,
    },
})
</script>

<style scoped></style>
