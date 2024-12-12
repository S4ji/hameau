<template>
  <main class="grid lg:grid-cols-2 place-items-center pt-16  md:pt-8">
  

    <div>
      <h1 class="text-5xl lg:text-6xl xl:text-7xl font-bold lg:tracking-tight">
        Pour nous rejoindre 
      </h1>
      <p class="text-lg mt-4 text-slate-600 max-w-xl">
Suivez bien les étapes suivantes : <ul>
  <li>- Rejoingez notre discord</li>
  <li>- Lisez le règlement</li>
  <li>- Créer votre ticket avec votre fiche personnage et les informations demandées.</li>
</ul> </p>
      <div class="mt-6 flex flex-col sm:flex-row gap-3">
        <LandingLink
          href="https://github.com/Gr33nW33n/nuxtship-template"
          target="_blank"
          rel="noopener"
          >Rejoindre le discord</LandingLink
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
