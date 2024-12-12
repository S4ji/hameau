<script setup>
definePageMeta({
  layout: "landing",
});

const pricing = [
  {
    price: "Humains",
    popular: false,
    link:'testurl',
    features: [
      "La race la plus commune sur les terres du Hameau, leur capacité à repousser l'échéance est telle qu'ils peuvent se sortir des situations les plus dangereuses, ils possèdent un 'second souffle' qui leur permet de régénérer une partie de leur santé, de devenir plus résistants à la douleur et de se déplacer plus vite et plus longtemps lorsque la situation est critique",
    ],
    button: {
      text: "Get Started",
      link: "/",
    },
  },
  {
    price: "Elfes",
    popular: false,
    link:'testurl',
    features: [
      "La race la plus commune sur les terres du Hameau, leur capacité à repousser l'échéance est telle qu'ils peuvent se sortir des situations les plus dangereuses, ils possèdent un 'second souffle' qui leur permet de régénérer une partie de leur santé, de devenir plus résistants à la douleur et de se déplacer plus vite et plus longtemps lorsque la situation est critique",
    ],
    button: {
      text: "Get Started",
      link: "/",
    },
  },
  {
    price: "Orcs",
    popular: false,
    link:'testurl',
    features: [
      "La race la plus commune sur les terres du Hameau, leur capacité à repousser l'échéance est telle qu'ils peuvent se sortir des situations les plus dangereuses, ils possèdent un 'second souffle' qui leur permet de régénérer une partie de leur santé, de devenir plus résistants à la douleur et de se déplacer plus vite et plus longtemps lorsque la situation est critique",
    ],
    button: {
      text: "Get Started",
      link: "/",
    },
  },
  {
    price: "Nains",
    popular: false,
    link:'testurl',
    features: [
      "La race la plus commune sur les terres du Hameau, leur capacité à repousser l'échéance est telle qu'ils peuvent se sortir des situations les plus dangereuses, ils possèdent un 'second souffle' qui leur permet de régénérer une partie de leur santé, de devenir plus résistants à la douleur et de se déplacer plus vite et plus longtemps lorsque la situation est critique",
    ],
    button: {
      text: "Get Started",
      link: "/",
    },
  },
  {
    price: "Anges",
    popular: false,
    link:'testurl',
    features: [
      "La race la plus commune sur les terres du Hameau, leur capacité à repousser l'échéance est telle qu'ils peuvent se sortir des situations les plus dangereuses, ils possèdent un 'second souffle' qui leur permet de régénérer une partie de leur santé, de devenir plus résistants à la douleur et de se déplacer plus vite et plus longtemps lorsque la situation est critique",
    ],
    button: {
      text: "Get Started",
      link: "/",
    },
  },
  {
    price: "Démons",
    popular: false,
    link:'testurl',
    features: [
      "La race la plus commune sur les terres du Hameau, leur capacité à repousser l'échéance est telle qu'ils peuvent se sortir des situations les plus dangereuses, ils possèdent un 'second souffle' qui leur permet de régénérer une partie de leur santé, de devenir plus résistants à la douleur et de se déplacer plus vite et plus longtemps lorsque la situation est critique",
    ],
    button: {
      text: "Get Started",
      link: "/",
    },
  },
  {
    price: "Vampires",
    popular: false,
    link:'testurl',
    features: [
      "La race la plus commune sur les terres du Hameau, leur capacité à repousser l'échéance est telle qu'ils peuvent se sortir des situations les plus dangereuses, ils possèdent un 'second souffle' qui leur permet de régénérer une partie de leur santé, de devenir plus résistants à la douleur et de se déplacer plus vite et plus longtemps lorsque la situation est critique",
    ],
    button: {
      text: "Get Started",
      link: "/",
    },
  },
  {
    price: "Lycans",
    popular: false,
    link:'testurl',
    features: [
      "La race la plus commune sur les terres du Hameau, leur capacité à repousser l'échéance est telle qu'ils peuvent se sortir des situations les plus dangereuses, ils possèdent un 'second souffle' qui leur permet de régénérer une partie de leur santé, de devenir plus résistants à la douleur et de se déplacer plus vite et plus longtemps lorsque la situation est critique",
    ],
    button: {
      text: "Get Started",
      link: "/",
    },
  },
  {
    price: "Créatures des abysses",
    popular: false,
    link:'testurl',
    features: [
      "La race la plus commune sur les terres du Hameau, leur capacité à repousser l'échéance est telle qu'ils peuvent se sortir des situations les plus dangereuses, ils possèdent un 'second souffle' qui leur permet de régénérer une partie de leur santé, de devenir plus résistants à la douleur et de se déplacer plus vite et plus longtemps lorsque la situation est critique",
    ],
    button: {
      text: "Get Started",
      link: "/",
    },
  },
  {
    price: "Gobelins",
    popular: false,
    link:'testurl',
    features: [
      "La race la plus commune sur les terres du Hameau, leur capacité à repousser l'échéance est telle qu'ils peuvent se sortir des situations les plus dangereuses, ils possèdent un 'second souffle' qui leur permet de régénérer une partie de leur santé, de devenir plus résistants à la douleur et de se déplacer plus vite et plus longtemps lorsque la situation est critique",
    ],
    button: {
      text: "Get Started",
      link: "/",
    },
  },
  {
    price: "Changeformes",
    popular: false,
    link:'testurl',
    features: [
      "La race la plus commune sur les terres du Hameau, leur capacité à repousser l'échéance est telle qu'ils peuvent se sortir des situations les plus dangereuses, ils possèdent un 'second souffle' qui leur permet de régénérer une partie de leur santé, de devenir plus résistants à la douleur et de se déplacer plus vite et plus longtemps lorsque la situation est critique",
    ],
    button: {
      text: "Get Started",
      link: "/",
    },
  },
  {
    price: "Dragonoïdes",
    popular: false,
    link:'testurl',
    features: [
      "La race la plus commune sur les terres du Hameau, leur capacité à repousser l'échéance est telle qu'ils peuvent se sortir des situations les plus dangereuses, ils possèdent un 'second souffle' qui leur permet de régénérer une partie de leur santé, de devenir plus résistants à la douleur et de se déplacer plus vite et plus longtemps lorsque la situation est critique",
    ],
    button: {
      text: "Get Started",
      link: "/",
    },
  },
  {
    price: "Créatures Spirituelles",
    popular: false,
    link:'testurl',
    features: [
      "La race la plus commune sur les terres du Hameau, leur capacité à repousser l'échéance est telle qu'ils peuvent se sortir des situations les plus dangereuses, ils possèdent un 'second souffle' qui leur permet de régénérer une partie de leur santé, de devenir plus résistants à la douleur et de se déplacer plus vite et plus longtemps lorsque la situation est critique",
    ],
    button: {
      text: "Get Started",
      link: "/",
    },
  },
];
</script>

<template>
  <LandingContainer>
    <LandingSectionhead>
      <template v-slot:title>Races</template>
      <template v-slot:desc
        >Grâce à Indrid, de nombreuses races sont accessibles, avec leur bonus au niveau du gameplay.</template
      >
    </LandingSectionhead>

    <div class="grid md:grid-cols-3 gap-16 mx-auto max-w-screen-lg mt-12">
      <LandingCard v-for="item of pricing" :plan="item" />
    </div>
  </LandingContainer>
</template>
