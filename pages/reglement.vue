<script setup>
definePageMeta({
    layout: 'landing',
})
</script>

<template>
    <LandingContainer>
        <LandingSectionhead>
            <template v-slot:title>Règlement du serveur Le Hameau </template>
            <template v-slot:desc>
                <p class="text-teal-100">
                    La lecture de ces règles est obligatoire avant de commencer
                    à jouer.
                </p>
            </template>
        </LandingSectionhead>

        <iframe
            src="https://docs.google.com/document/d/11oCemzMF9vvEOavxyLA7NqeZMeEaKDFGnHpLTSNz5XM/preview"
            width="100%"
            height="800"
            style="border: none"
        >
        </iframe>
        <!-- <LandingRpTerms :rules="clanWarPvpRules" /> -->
    </LandingContainer>
</template>
