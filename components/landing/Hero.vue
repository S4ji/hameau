<template>
  <main class="grid lg:grid-cols-2 place-items-center pt-16  md:pt-8">
    <div class="p-24 md:order-1 hidden md:block">
      <img
        class="rounded-full transition-transform transform hover:scale-125"
        src="~/assets/img/hero.jpg"
        alt="Starship starts the engine"
        loading="eager"
        format="avif"
        width="512"
        height="512"
      />
    </div>

    <div>
      <h1 class="text-5xl lg:text-6xl xl:text-7xl font-bold lg:tracking-tight">
        Le Hameau [FR] +18 RP/PVP/PVE
      </h1>
      <p class="text-lg mt-4 text-slate-600 max-w-xl">
        Serveur dédié 30 Slots évolutifs. Multivers. Prenez part à cette aventure entourée d'un staff à l'écoute de vos projets RP, d'une carte en constante évolution selon vos choix.



      </p>
      <div class="mt-6 flex flex-col sm:flex-row gap-3">
        <LandingLink
          href="https://github.com/Gr33nW33n/nuxtship-template"
          target="_blank"
          rel="noopener"
          >Nous Rejoindre</LandingLink
        >
        <LandingLink
          size="lg"
          styleName="outline"
          rel="noopener"
          href="https://github.com/Gr33nW33n/nuxtship-template"
          target="_blank"
          >Lire le Règlement</LandingLink
        >
      </div>
    </div>
  </main>
</template>
