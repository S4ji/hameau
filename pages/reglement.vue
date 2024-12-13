<script setup>
definePageMeta({
    layout: 'landing',
})

const rpTerms = {
    Metagaming: {
        definition:
            'Le meta est interdit et désigne le fait d’utiliser des informations hors roleplay dans le cadre roleplay afin de modifier le roleplay qui en découle.',
    },
    Powerplaying: {
        definition:
            'Le powerplay désigne des méthodes afin de rendre son personnage surpuissant afin de gagner en toute circonstances. C’est également une pratique interdite.',
    },
    Ellipse: {
        definition:
            'Les ellipses sont faites afin d’écourter des scènes lorsque le temps ou le consentement à jouer une scène trop rude à nos yeux est de rigueur.',
    },
    'Le Void': {
        definition:
            "Le Void est une pratique utilisée quand le besoin d’annuler une scène est nécessaire. Seul le staff se voit accorder l'autorisation de Void (Annuler) une scène.",
    },
    'Le Fear RP': {
        definition:
            'Le Fear RP est la définition même de jouer la peur de la mort, des blessures, du danger.',
    },
    'Le No Fear RP': {
        definition:
            'Le No Fear RP est le terme pour désigner le fait de ne pas faire de Fear RP.',
    },
    'Le Force RP': {
        definition:
            "C'est le fait de forcer un RP et la volonté qui va avec, à autrui.",
    },
    'Le Mass RP': {
        definition:
            'Le Mass RP, c’est le fait de prendre en compte que vous n’êtes pas seuls, vous les joueurs.',
    },
}

const serverRules = {
    'Avoir 18 ans ou plus': {
        definition:
            'Vous devez avoir 18 ans ou plus pour jouer sur le serveur.',
    },
    'Restez toujours en RP': {
        definition:
            'Le HRP doit être une chose exceptionnelle et ne doit pas être une chose commune.',
    },
    'Ne faites pas de Méta': {
        definition:
            'Le métagaming est interdit. Il désigne le fait d’utiliser des informations hors roleplay dans le cadre roleplay afin de modifier le roleplay.',
    },
    'Ne faites pas de Powerplay': {
        definition:
            'Le powerplay désigne des méthodes afin de rendre son personnage surpuissant pour gagner en toute circonstance.',
    },
    'Ne faites pas de Force RP': {
        definition:
            'Le Force RP consiste à forcer un RP et à imposer sa volonté à autrui. Cette pratique est interdite.',
    },
    'Ne faites pas de No Fear RP': {
        definition:
            'Le No Fear RP désigne le fait de ne pas faire preuve de peur dans des situations menaçant la vie de votre personnage.',
    },
    'Respectez le Mass RP': {
        definition:
            'Agissez comme si un monde entier et bien vivant existait autour de vous. Ne pas respecter cette règle peut entraîner des sanctions sévères.',
    },
    'Pas de PvP à vue sans raison cohérente': {
        definition:
            'Le PvP à vue est interdit sans une raison RP claire et cohérente.',
    },
    'N’exploitez pas les bugs du jeu': {
        definition:
            'Exploiter les bugs du jeu est strictement interdit et peut entraîner des sanctions.',
    },
    'Ne courez pas de façon HRP': {
        definition:
            'Ne courez pas de manière HRP. Laissez du temps aux autres pour initier des scènes RP. Si vous ne pouvez pas, expliquez-le en RP.',
    },
    'Ne jouez pas de personnage enfantin': {
        definition: 'Les personnages enfantins ne sont pas autorisés.',
    },
    'Maximum 20 accessoires ToT!Custom': {
        definition:
            "Vous ne pouvez porter que 20 accessoires dans la catégorie 'Accessories' du Shift B. Les accessoires gameplay ne comptent pas dans ce maximum.",
    },
    'L’ellipse doit être validée': {
        definition:
            'Les ellipses doivent être validées par les personnes engagées dans la scène RP. En cas de désaccord, faites un ticket auprès du staff.',
    },
    'Pas de changement de sexe ou de race sans accords du staff': {
        definition:
            'Tout changement de sexe ou de race de votre personnage doit être validé par le staff.',
    },
    'Pas d’ailes ou accessoires/potions permettant le vol': {
        definition:
            'Les ailes ou accessoires/potions permettant de voler en PvE ou PvP sont interdits.',
    },
    'Vols sous surveillance du staff': {
        definition:
            'Les vols de maisons/clans doivent être effectués sous la surveillance du staff. Si un vol est commis sans la présence du staff, des sanctions seront appliquées.',
    },
    'Consentez à subir les animations': {
        definition:
            'Vous consentez à participer aux animations. La participation est volontaire, mais vous pouvez prendre part de manière passive, comme aider les blessés.',
    },
    'Demander consentement avant scènes dérangeantes': {
        definition:
            "Demandez toujours le consentement HRP avant d'impliquer quelqu'un dans une scène violente ou dérangeante, comme l’abus sexuel ou la violence extrême.",
    },
    'Cacher son identité avec /acts': {
        definition:
            'Les /acts pour cacher votre identité (nom et visage) ne doivent pas être validés sur le suivi RP.',
    },
    'Respect du ERP': {
        definition:
            "Le ERP nécessite du respect. Il est interdit de forcer une personne à participer à une scène d'érotique RP qui la met mal à l’aise.",
    },
    'Le temps passe différemment sur les terres': {
        definition:
            "Le temps dans le jeu s'écoule plus rapidement pour torturer l'esprit des joueurs, mais un jour réel équivaut à plusieurs jours en jeu.",
    },
    'Portail et langage commun': {
        definition:
            'Lorsque vous passez par le portail, vous acquérez la capacité de comprendre et de parler le langage des autres.',
    },
    'Les terres sont en proie au chaos': {
        definition:
            "Les terres sont en proie au chaos et seul le hameau résiste. Vous pouvez aider à reconquérir le territoire ou choisir de partir dans l'inconnu.",
    },
}
const actRules = {
    'Un /act est un personnage éphémère': {
        definition:
            'Un /act est un personnage temporaire, créé lorsque le personnage principal est indisponible. Il ne doit pas changer significativement le RP.',
    },
    "N'en posséder qu'un": {
        definition: "Un joueur ne peut posséder qu'un seul /act à la fois.",
    },
    'Ne doit pas agir sur des RP importants': {
        definition:
            'Le /act ne doit pas interférer dans des RP importants ou majeurs.',
    },
    'Ne doit pas utiliser les rolls du personnage principal': {
        definition:
            'Le /act ne doit pas utiliser les dés du personnage principal. Il doit utiliser uniquement le /roll 1d20.',
    },
    'Ne possède pas de métier': {
        definition:
            'Le /act ne doit pas avoir de métier, il ne participe pas aux activités professionnelles du serveur.',
    },
    'Ne possède pas de porte de sortie en cas de mort RP': {
        definition:
            "Le /act n'a pas de porte de sortie en cas de mort en RP. Il suit les règles de RP sans exception.",
    },
    'Ne peut pas devenir parent': {
        definition: 'Le /act ne peut pas devenir parent dans le cadre du RP.',
    },
    'Ne possède pas de magie ni de pouvoir raciaux': {
        definition:
            'Le /act ne possède pas de magie ni de pouvoirs raciaux. Il doit être limité à des actions simples.',
    },
    'Peut être esclave sous réserve d’exprimer au possesseur que cela ne sera pas un RP temps plein':
        {
            definition:
                'Le /act peut être esclave, mais il faut que le possesseur accepte que cela ne soit pas un RP à plein temps.',
        },
    'Jouer son enfant du personnage principal ne doit pas inclure de meta parent/enfant':
        {
            definition:
                'Lorsque vous jouez l’enfant de votre personnage principal, cela ne doit pas inclure de méta RP parent/enfant.',
        },
    'Ne peut pas former de couple': {
        definition:
            'Le /act ne peut pas former de couple, car cela est considéré comme un RP important.',
    },
    "Qu'il ne soit pas un ancien PJ principal": {
        definition:
            'Le /act ne peut pas être un ancien personnage principal. Il doit être un personnage totalement distinct.',
    },
    'Le /act doit être validé par le staff': {
        definition:
            "Avant d'utiliser un /act, il doit être validé par le staff. La demande se fait via le suivi RP.",
    },
}

const suiviRpRules = {
    'Le Suivi RP est obligatoire': {
        definition:
            'Le Suivi RP est obligatoire. Vous devez le remplir au moins une fois tous les 15 jours sous peine de suppression du suivi et du personnage.',
    },
    'Décrire vos scènes RP et votre quotidien': {
        definition:
            'Dans le Suivi RP, vous pouvez décrire vos scènes RP, vos échanges, et le quotidien de votre personnage, y compris son état de santé mental et physique.',
    },
    'Signaler vos absences': {
        definition:
            'Vous devez signaler vos absences dans le Suivi RP pour éviter que votre personnage ne soit supprimé par erreur.',
    },
}

const mortRpRerollRules = {
    'Mort RP et Reroll': {
        definition:
            'En cas de mort RP de votre personnage, vous devez supprimer votre personnage via le menu échappement et créer une nouvelle candidature sur Discord pour être validé à nouveau.',
    },
    'Reroll et validation': {
        definition:
            'En cas de reroll, vous devrez également supprimer votre personnage via le menu échappement et créer une nouvelle candidature sur Discord afin de recevoir une nouvelle validation.',
    },
    'Suivi RP pour la mort RP': {
        definition:
            "Si vous proposez une mort RP, vous devez être irréprochable dans votre suivi RP. Les motifs avant la tentative et les captures d'écran de la scène doivent être inclus dans votre suivi RP. Le staff surveillera pour éviter les abus.",
    },
    'Non-validation par le staff pour la mort RP': {
        definition:
            "La mort RP ne nécessite pas de validation préalable du staff, mais il est obligatoire de l'informer afin qu'il puisse surveiller toute scène où la mort RP pourrait être infligée.",
    },
    'Portes de sortie recommandées': {
        definition:
            "Les portes de sortie ne sont pas obligatoires, mais fortement recommandées dans un cadre de Fair-play. La mort facile n'est jamais amusante ni appréciée.",
    },
    'Droit du staff sur la mort RP en animation': {
        definition:
            "Lors d'une animation, le staff se réserve le droit d'infliger une mort RP, surtout en cas d'actions grotesques ou de Powerplay, ou en l'absence de Fear RP face aux dangers.",
    },
    'Préparation à la mort RP': {
        definition:
            'Lorsque vous préparez à infliger une mort RP, considérez que la situation pourrait se retourner contre vous.',
    },
}

const absencesRules = {
    "Informer en cas d'absence": {
        definition:
            "Lorsque vous vous absentez, que ce soit par démotivation ou préoccupations liées à la vie réelle, il est de votre devoir d'en faire part dans le suivi RP ainsi que le canal d'absence.",
    },
    'Absences non justifiées': {
        definition:
            'Les absences non justifiées peuvent entraîner des mesures prises par le Staff.',
    },
    "Rappel à l'ordre après 15 jours": {
        definition:
            "Si vous êtes inactif pendant 15 jours sans nouvelles, un rappel à l'ordre sera effectué.",
    },
    'Destruction des constructions après 25 jours': {
        definition:
            'Après 25 jours sans nouvelles, vos constructions seront détruites.',
    },
    'Suppression du personnage après 30 jours': {
        definition:
            'Après 30 jours sans nouvelles, votre personnage sera supprimé.',
    },
    'Suivi RP est essentiel': {
        definition:
            "Le suivi RP est l'essence même de votre aventure et votre contact avec le staff. Ne le négligez pas. Utilisez le journal dans le Shift+R comme pense-bête pour vous souvenir des événements importants.",
    },
    'Renouveler les absences justifiées tous les 30 jours': {
        definition:
            'Les absences justifiées doivent être renouvelées tous les 30 jours maximum pour éviter des mesures.',
    },
    'Prévenir les personnes en cours de projets RP': {
        definition:
            "Pensez à prévenir les personnes avec qui des projets RP sont en cours, afin d'éviter de les bloquer suite à votre disparition soudaine.",
    },
}

const constructionAndClanRules = {
    'Ne construisez pas à vue du hameau': {
        definition: 'Ne construisez pas à vue du hameau.',
    },
    'Ne construisez pas sans avoir de clan': {
        definition: 'Ne construisez pas sans avoir de clan.',
    },
    'Ne construisez pas à vue d’un autre clan': {
        definition: 'Ne construisez pas à vue d’un autre clan.',
    },
    'Limite de niveau de construction (T2)': {
        definition:
            'Ne construisez pas au-dessus du T2 si vous n’êtes pas bâtisseur de métier. (T3=Bois renforcé, pierre renforcée, la majeure partie des DLC vanilla, la plupart des mods)',
    },
    'Ne construisez pas près d’un portail de téléportation': {
        definition: 'Ne construisez pas collé à un portail de téléportation.',
    },
    "Éviter les constructions avec pertes d'images": {
        definition:
            'Ne faites pas de constructions qui pourraient causer des pertes d’images aux joueurs possédant une petite configuration. (Si vous n’êtes pas sûr, demandez!)',
    },
    'Limite de BP par joueur': {
        definition:
            'Chaque joueur a le droit de poser 400 BP, incluant construction et décorations. Faites toujours un /heatmap afin de voir si vous dépassez les 400 BP.',
    },
    'Limite de BP par clan': {
        definition:
            'Un clan se constitue de 7 personnes maximum, ce qui signifie qu’un clan ne pourra posséder que 2800 BP maximum.',
    },
    'Favorisez les végétations non animées': {
        definition:
            'Favorisez les végétations qui n’ont pas d’animation afin d’éviter de trop grosses pertes d’images.',
    },
    'Les Lamplighters et montures ne comptent pas pour les thralls': {
        definition:
            "Les Lamplighters ou 'Lampistes' et les montures ne sont pas comptabilisés dans le maximum de thralls possible. Si vous souhaitez les renommer, précisez leur rôle dans le nom pour faciliter les vérifications du staff.",
    },
    'Limite de Thralls/Pets de combat par joueur': {
        definition:
            'Le maximum de Thrall/pet de combat par joueur est de 3, dans une limite de 15 par clan.',
    },
    'Limite de montures par joueur': {
        definition:
            'Une monture terrestre et une monture volante par personne maximum.',
    },
    'Nommez vos montures': {
        definition:
            'Nommez au moins vos montures avec votre nom afin que le propriétaire soit connu en cas de monture perdue en milieu sauvage.',
    },
    'Limite de coffres pour ressources par clan': {
        definition:
            "Trois coffres autorisés pour les ressources (minerais, bois, or, argent, cristaux, armes, armures, etc.) par clan. Le serveur ayant le mod Unlock+, ce mod recherche sans fin les conteneurs autour de l'atelier en cours d'utilisation.",
    },
    'Relations de clan et alliances': {
        definition:
            'Chaque clan peut avoir des alliés et des ennemis. Les alliances de circonstances peuvent avoir lieu, mais elles doivent être temporaires et notifiées dans le suivi RP, validées par le staff.',
    },
    "Construction proche de votre lieu d'installation": {
        definition:
            'Un clan/joueur ne peut construire qu’à proximité immédiate du lieu où il s’installe. Vous ne pouvez pas construire des bâtisses éloignées de votre lieu de résidence.',
    },
}

const slaveryRules = {
    'Seuls les esclavagistes peuvent dresser et revendre des esclaves': {
        definition:
            'Seuls les esclavagistes peuvent dresser et revendre au marché, des esclaves.',
    },
    'N’importe qui peut posséder un esclave': {
        definition: 'N’importe qui peut posséder un esclave.',
    },
    'Affranchissement après 3 mois': {
        definition:
            'Les esclaves peuvent être affranchis après une période de 3 mois. A noter qu’une fois affranchi, l’esclave devra le préciser dans son suivi RP.',
    },
    "Les esclaves ne sont pas là que pour l'ERP": {
        definition: 'Les esclaves ne sont pas là que pour la pratique du ERP.',
    },
    'Demande de vente via ticket': {
        definition:
            "Un esclave à l’arrivée sur le serveur peut demander à se faire vendre via un ticket. Il peut aussi être un esclave en fuite et pourra donc afficher le statut dans le shift+R 'Esclave en fuite' si personne ne semble comprendre qu’il en est un.",
    },
    'Les esclaves peuvent s’échapper': {
        definition:
            'Les esclaves qui le deviennent par la suite de scènes RP pourront s’échapper et ne sont pas soumis à la règle des 3 mois avant d’être affranchis, trouvez une solution afin de ne pas gâcher le RP de l’un des partis.',
    },
    "Tentative de fuite si sans RP pendant plus d'une heure": {
        definition:
            'Un esclave ne recevant pas de RP pendant plus d’une heure (alors que des personnes sont disponibles en jeu) peut faire une tentative de fuite. Si personne n’est disponible en jeu, il sera bon ton de trouver un accord avec les détenteurs de l’esclave.',
    },
    'Esclave sans garde PNJ peut être enlevé': {
        definition:
            'Si votre esclave n’est pas surveillé par un garde PnJ lors de ses balades sans ses maîtres, vous acceptez alors que celui-ci vous soit enlevé.',
    },
    'Armer un esclave à vos risques et périls': {
        definition:
            'Vous pouvez armer votre esclave, à vos risques et périls. Rien n’empêche celui-ci de se rebeller.',
    },
    'Respect du consentement HRP': {
        definition:
            'Veuillez toujours respecter le consentement HRP de la personne qui joue l’esclave, nous sommes ici pour nous amuser, pas nous dégoûter.',
    },
}

const professionRules = {
    'Nombre de métiers limité': {
        definition:
            'Vous ne pouvez posséder que deux métiers, afin de les connaître et de les comprendre dans les grandes lignes, allez ici https://discord.com/channels/1231460610122846251/1232356125198782464',
    },
    'Changer de métier': {
        definition:
            'Pour changer de métier, il vous faut trouver quelqu’un pratiquant le futur métier de vos rêves et lui demander des cours, Cinq ou six cours suffiront, avec minimum 2 à 3 jours d’espacement entre deux.',
    },
    'Craft et construction sans métier': {
        definition:
            'Si vous ne possédez pas le métier pour un craft ou une construction, vous ne pouvez que créer du T1 et T2, jusqu’à l’acier durcit.',
    },
}

const pvpRules = {
    'Pas de PVP à vue': {
        definition:
            "Le fait que le serveur soit en JCJ actif ne signifie pas PVP à vue. Il est interdit de simplement s'amener face à quelqu'un et le taper sans raison, même si d'un coup, vous vous dites 'Et si je devenais bandit l'espace d'un instant ?'.",
    },
    'Consentement pour PVP': {
        definition:
            "Toutes interactions découlant d'une défaite/victoire PVP amènera forcément parfois à des choses désagréables. Trouvez premièrement une entente qui mène à un consentement, si la personne ne consent pas, l'acte se fera malgré tout (Dans la limite des règles agréées) et une ellipse sera faite.",
    },
    "Ne faites pas ce que vous ne voulez pas qu'on vous fasse": {
        definition:
            'Ne vous cacher pas derrière le consentement quand vous êtes dans la position de ‘victime’ si l’acte est similaire à ce que vous avez joué en ‘tortionnaire’.',
    },
    'Démarrer un combat': {
        definition:
            "Lorsque vous désirez débuter un combat, une émote doit être faite avec un dialogue. Lorsque la personne prend note de l'émote et y répond avec une autre, alors l'agresseur fera /pvp start. Bonne chance.",
    },
    "Vol lors d'un combat": {
        definition:
            "Vous pouvez voler vos ennemis mis au sol dans la limite d'un objet par personne au sol. (exemple: Vous volez 10 pièces d’or à l’une de vos victimes puis les potions de soin de l’autre dans le cas d’une victoire face à deux personnes.)",
    },
    "Intervention lors d'un combat": {
        definition:
            "N'importe qui, qui aperçoit un combat déjà débuté pourra intervenir sans émotes et participer à celui-ci. Cette règle permet les embuscades.",
    },
    "Fin d'un combat": {
        definition:
            'Un combat PVP se termine lorsque la personne est au sol. Vous êtes donc à la merci de votre agresseur, il pourra soit vous voler, vous emmener, soit vous laisser sur place. Quitter la scène suite à une défaite sera sévèrement puni.',
    },
    'Combat au jet de dés': {
        definition:
            "Un combat pourra tout de même se faire au jet de dés si les personnes tombent en accord sur l'utilisation de ceux-ci. Ça ne veut pas dire que les dés seront le PvP primaire.",
    },
    'Capturer une victime': {
        definition:
            'Si vous gagnez et faites de votre victime une personne capturée temporairement, laissez une chance à la personne de se libérer. Des indices, des portes non verrouillées, peu importe. Soyez Fairplay.',
    },
    'Fuir un combat': {
        definition:
            'Vous pouvez tenter de fuir un combat ou abandonner après 1 minute, mais votre opposant peut vous poursuivre. L’utilisation de /home, /warp et autres systèmes de téléportation est interdite.',
    },
    'Combat avec des thralls': {
        definition:
            'Les combats avec des thralls sont autorisés sous surveillance staff. Les thralls vanilla et AOC sont les seuls autorisés en PvP. Ils peuvent participer uniquement durant une guerre de clan, et seulement si un staff est présent.',
    },
    "Relèvement d'alliés": {
        definition:
            "Lors d'un combat, il est interdit de relever ses alliés. Si le compteur d'inconscience arrive à terme, vous devez vous mettre en inconscience par émote et ne pas vous éloigner.",
    },
    'Interdiction des soins en PvP': {
        definition:
            'Les soins sont interdits durant le PvP. Les orbes de soins, orbes offensives, potions de soins, nourriture curative ou tout autre soin sont interdits.',
    },
    'Duel PVP (non-amical)': {
        definition:
            "Lors d'un duel PVP, le/la perdant(e) devra utiliser l'ability 'Se blesser' afin d’avoir un statut blessé pendant 3 heures, guérissable par les médecins.",
    },
    'Armes et armures validées pour le PvP': {
        definition:
            'Les armures et armes validées pour le PvP sont les armes vanilla, Shima Compendium et AOC. Cette liste peut évoluer après des tests sur les armes et armures des autres mods du serveur.',
    },
    'Vol pendant la course poursuite': {
        definition:
            'Le vol est interdit dans un but de course poursuite. Voler à la vitesse de l’éclair contre quelqu’un de terrestre n’est pas fairplay. Les thralls ne pourront pas suivre une personne volant.',
    },
}

const clanWarPvpRules = {
    'Supervision par le staff': {
        definition:
            'Les guerres de clans seront toujours supervisées par le staff au vu des possibles désaccords que cela pourrait créer.',
    },
    'Limitation des thralls': {
        definition:
            'Les thralls AOC et Vanilla seront les seuls autorisés et seront limités à 15 pour un maximum de 3 par personne.',
    },
    'Règles du PvP joueur contre joueur classique': {
        definition:
            "Les règles du PVP classique s'appliquent. Personne ne se relève une fois mis au sol.",
    },
    'Armes interdites': {
        definition:
            "Les armes suivantes sont interdites en PvP lors d'une guerre de clan :",
    },
    'Armes interdites listées': [
        'Armes Exiles Extrême non PvP-Stable',
        'Shoulder Pets autorisés sauf les fées pour le healing',
        'Bâtons de magie AOC',
        'Magie interdites en PvP au-delà du rang 2',
        'DMT sauf Bespoke',
        'Thralls/Pet autre que vanilla et AoC',
        'Bow of the Highborn',
        'Ailes et capacités de vol en tout genre (Interdit en PvP mais PvE également)',
        'Vanir Windcutters (WARRIOR Mutator)',
        'Sword of Essari',
        'Armes et consommables de plague',
        'Blood Cascade (Objet - Sort des vampires du mod Indrid. Interdit en PvP mais PvE également)',
        'Orbes offensives',
        'Objets de soin (orbes, flèches, sorts, nourriture, etc)',
    ],
}
</script>

<template>
    <LandingContainer>
        <LandingSectionhead>
            <template v-slot:title>Règlement du serveur Le Hameau </template>
            <template v-slot:desc
                >Ce règlement est susceptible à tout changement allant de
                l'ajout à la suppression comme à la modification de celui-ci.
            </template>
        </LandingSectionhead>
        <h2 class="text-4xl lg:text-5xl font-bold lg:tracking-tight">
            Termes à connaitre
        </h2>
        <LandingRpTerms :rules="rpTerms" />
        <h2 class="text-4xl lg:text-5xl font-bold lg:tracking-tight">
            Règlement du serveur
        </h2>
        <LandingRpTerms :rules="serverRules" />
        <h2 class="text-4xl lg:text-5xl font-bold lg:tracking-tight">
            Règles sur les acts
        </h2>
        <LandingRpTerms :rules="actRules" />
        <h2 class="text-4xl lg:text-5xl font-bold lg:tracking-tight">
            Règles suivi RP
        </h2>
        <LandingRpTerms :rules="suiviRpRules" />
        <h2 class="text-4xl lg:text-5xl font-bold lg:tracking-tight">
            Règles Mort RP/Reroll
        </h2>
        <LandingRpTerms :rules="mortRpRerollRules" />
        <h2 class="text-4xl lg:text-5xl font-bold lg:tracking-tight">
            Règles Absences
        </h2>
        <LandingRpTerms :rules="absencesRules" />
        <h2 class="text-4xl lg:text-5xl font-bold lg:tracking-tight">
            Règles constructions
        </h2>
        <LandingRpTerms :rules="constructionAndClanRules" />
        <h2 class="text-4xl lg:text-5xl font-bold lg:tracking-tight">
            Règles Esclavage
        </h2>
        <LandingRpTerms :rules="slaveryRules" />
        <h2 class="text-4xl lg:text-5xl font-bold lg:tracking-tight">
            Règles métier
        </h2>
        <LandingRpTerms :rules="professionRules" />
        <h2 class="text-4xl lg:text-5xl font-bold lg:tracking-tight">
            Règles PVP
        </h2>
        <LandingRpTerms :rules="pvpRules" />
        <h2 class="text-4xl lg:text-5xl font-bold lg:tracking-tight">
            Règles Guerre de Clan
        </h2>
        <LandingRpTerms :rules="clanWarPvpRules" />
    </LandingContainer>
</template>
