## Quelles versions du firmware sont actuellement hackables ?

!!! tip ""
    Actuellement, deux versions matérielles de la Switch existent. Toute Switch achetée ou fabriquée avant mi-2018 dispose d’un bug bootrom qui nous permet d’exécuter du code quelle que soit la version firmware de la Switch. Lorsque Nintendo met à jour le système CFW aura cependant généralement besoin d’une mise à jour pour en tenir compte. 
    Ce bug ne peut pas être corrigé par Nintendo une fois que la console quitte l’usine, à moins que la console ne soit envoyée pour réparation. Cela signifie que tous les firmwares actuels et futurs seront en mesure de lancer un CFW grâce à cet exploit sur l’ancienne version matérielle.

    Toute console achetée après août 2018 est **probablement** patchée. Cela inclut les dernières unités produites, appelées « boîte rouge » ou « Mariko ».
    Mariko est un modèle patché, mais qui peut posséder sur un firmware vulnérable.
    Actuellement, la seule façon de savoir si votre Switch est hackable est en essayant d’envoyer un payload en RCM.
    Même patchées, de nombreuses consoles en 8.0.1 et moins seront hackables dans une certaine mesure à l’avenir (voir la section [Dois-je mettre à jour mon Firmware ?](#dois-je-mettre-à-jour-mon-firmware) pour des informations beaucoup plus détaillées).
    Le numéro de série au dos de la boîte peut éventuellement vous dire quelles consoles sont patchées et lesquelles ne le sont pas. 
    Voir <a href="https://gbatemp.net/threads/switch-informations-by-serial-number.481215/" target="_blank">ici</a> pour une liste à jour.


## Comment puis-je utiliser la faille ? Comment puis-je démarrer en RCM ?

!!!tip ""
    Pour lancer un CFW en utilisant la faille fusée-gelée, la Switch doit être en "Recovery Mode"(RCM). 
    La façon la plus simple d’entrer en RCM est en reliant le pin 10 à la terre dans le rail joycon droit et en maintenant VOL+ au démarrage. 
    De nombreuses méthodes existent, cf. [cette page](user_guide/emummc/entering_rcm_fr.md) pour plus d'informations. 
    Une fois que la Switch est en RCM, elle doit être connectée à un ordinateur, un téléphone ou un dongle pour recevoir un payload.

    Cette procédure devra être répétée chaque fois que la Switch démarre à partir d’un état complètement « off » (i.e. si elle est complètement éteinte), sinon la Switch va démarrer normalement (stock).


## Qu’est-ce qu'un bon jig ? Puis-je utiliser un trombone ?

!!!tip ""
    La plupart des gens préfèrent utiliser des jigs imprimés en 3D pour entrer dans en RCM. 
    Ces jigs sont fabriqués de façon à ce qu’ils se glissent dans le rail du joycon droit et ont un morceau de fil en métal qui fait un ponts entre le pin 10 et l’un des pins de terre. 
    Beaucoup de modèles de jigs différents existent, mais il est important de comprendre que ces jigs peuvent endommager la Switch si ils sont mal faits.

    Puisque le fil dans le jig est censé toucher les pins à l’intérieur du rail joycon de la Switch, il est important que le fil employé soit mince, pas rigide et pas plié/pas pointu. 
    Les trombones forment des jigs potentiellement dangereux, car ils sont fabriqués à partir d’un matériau dur, sont rigides, pointus, et peuvent facilement rayer les pads à l’intérieur de la Switch. 
    Un bon jig a un fil de 0,2mm de diamètre qui est plié d’une manière à ce que l’extrémité du fil ne gratte pas sur les pads. 
    Vous pouvez également télécharger et imprimer en 3D votre propre jig et utiliser les photos de [ce site web](https://www.thingiverse.com/thing:2892320) pour vous guider sur la façon de plier le fil correctement.


## Y a-t-il un moyen plus facile d’entrer en RCM ?

!!!tip ""
    Pour entrer plus facilement en RCM, il existe une solution appelée « AutoRCM ». 
    Une fois mis en place, cette méthode fera toujours démarrer la Switch en RCM, même sans jig. 
    Cela fonctionne un « brick » de la Switch, mais d’une manière contrôlée. 
    La Switch détecte que quelque chose ne va pas et entre en RCM pour se faire réparer. 
    Le gros inconvénient de cette méthode est qu’il est impossible de démarrer la Switch sans un ordinateur, un téléphone ou un dongle. De plus, il faudra obligatoirement une carte SD contenant les fichiers de CFW appropriés. En outre, si la batterie de la Switch est complètement drainée, la Switch devra être charger à au moins 10% dans Hekate avant de lancer Atmosphère, sinon la Switch refusera de démarrer en raison d'une batterie trop faible. Recharger la consolle pendant qu'elle est en RCM n’est pas recommandée car c’est très lent. L'AutoRCM peut être supprimé, mais il est conseillé de garder un backup (sauvegarde) de la  NAND et de BOOT0/1 avant de l’utiliser.

    De nombreux téléphones Android sont en mesure d’envoyer un payload à la Switch, ce qui en fait un moyen portable parfait pour lancer un CFW. Différentes conceptions pour les dongles portables existent, allant des projets Raspberry Pi Zero et Arduino aux dongles internes, qui fonctionnent de façon complètement autonomes. Ces derniers ne doivent être utilisés que par des utilisateurs avancés, car ils nécessitent une soudure sur la carte mère de la Switch elle-même.


## Dois-je mettre à jour mon Firmware ?

!!!tip ""

    Si votre Switch fait partie des nouvelles versions qui ont corrigé l’exploit du RCM et que vous êtes sur un firmware 7.0.1 ou moins, vous ne devriez pas mettre à jour si vous souhaitez pouvoir lancer un CFW dans un avenir pas trop lointain.

    Si votre Switch fait partie des anciennes versions (non patchées) et que cela ne vous dérange pas d’avoir à utiliser des jigs/hardmods/AutoRCM et d’envoyer un payload depuis votre ordinateur, téléphone ou dongle chaque fois que vous voulez lancer un CFW, alors il est tout à fait possible de mettre à jour. 
    Si vous voulez avoir la chance de peut-être, un jour, ne pas avoir à utiliser un appareil externe, alors il est recommandé de rester sur un FW aussi bas que possible. 
    Méfiez-vous que cela signifie que vous allez potentiellement devoir attendre très longtemps (des années) pour que cela se produise (si cela se produit !). Des exploits pour lancer un CFW via le navigateur existent pour les firmwares jusqu’à 7.0.1.

    Le downgrade de la switch est possible, mais il nécessite l’utilisation d’AutoRCM et d’un bootloader/payload spécial pour contourner les différents mécanismes anti-downgrades de la Switch. 
    Cela ne fonctionnera pas sur un système non patché, et est pratiquement inutile pour la plupart des utilisateurs.
    Sur chaque boot, le firmware de la Switch compare le nombre de fusibles électroniques qui ont été brûlés et le nombre de fusibles électroniques qui devraient être brûlés. 
    Les mises à jour majeures de la Switch, ou mises à jour dans lesquelles une vulnérabilité système a été patchée, brûlent irréversiblement l’un des 64 « fusibles électroniques » de la Switch. 
    *Si jamais la Switch détecte qu’un plus grand nombre de fusibles électroniques ont été brûlés que ce qui était prévu prévu (ce qui signifie qu’un downgrade s’est produit), elle refusera de démarrer. Remplacer les fusibles électroniques n’est pas une option.*
    Vous pouvez trouver plus d’informations sur les fusibles <a href="https://switchbrew.org/wiki/Fuses#Anti-downgrade" target="_blank">ici</a>
    Atmosphère 1.2.5 fonctionne très bien avec la nouvelle mise à jour du firmware 13.2.0 sur les unités non patchées. La situation des unités patchées est celle-ci :

    - **"Anciennes"** *Switch patchée (HAC-001) : Ne mettez PAS à jour au-delà de 7.0.1. Les consoles tournant sur 7.0.1 et moins finiront par obtenir un CFW. Les unités patchées qui sont au firmware 8.0.0 ou 8.0.1 recevront probablement des homebrews.*

    - **"Nouvelles"** *Switch (HAC-001-01) : Ne mettez PAS à jour au-delà de 8.0.1. Les consoles tournant sur 8.0.1 et moins recevront probablement des homebrews. Les consoles tournant sur 8.1.0 et plus ne seront certainement jamais hackables et peuvent être mises à jour.*

    - **Switch Lite** *(HDH-001) : Ne mettez PAS à jour au-delà de 8.0.1. Les consoles tournant sur 8.0.1 et moins recevront probablement des homebrews. Les consoles tournant sur 8.1.0 et plus ne seront certainement jamais hackables et peuvent être mises à jour.*

    Une méthode de mise à jour sans brûler de fusibles électroniques existe, mais, comme pour le downgrade, il vous oblige à utiliser AutoRCM et d'envoyer un payload via USB à chaque fois que vous souhaitez démarrer votre console. En effet, la démarer normalement, ne cerait-ce qu'une fois ferait instantanément brûler les fusibles électroniques. Notez que d’autres mécanismes anti-downgrade existent, rendant par exemple impossible de démarrer des cartouches de jeu sur un firmware inférieur à 4.1/9.0.0 si la Switch a déjà lancé un jeu sous firmware 4.1+/9.0.0+. Cela ne peut être évité en désactivant complètement le lecteur de cartouches de jeux en étant sous firmware 4.1+/9.0.0+, ce qui est très peu pratique pour la plupart des utilisateurs.


## Utiliser des homebrew peut-il être dangereux ? Vais-je être banni(e) ?

!!!tip ""
    Le Switch fonctionne avec beaucoup de signaux de télémétrie, et a été surnommée le «telemetry monster» par plusieurs développeurs. 
    Tant que la Switch est connectée à Internet, Nintendo reçoit des rapports sur un grand nombre d’actions effectuées par la Switch et a la possibilité de se connecter ou d’agir en fonction . 
    Même si la Switch est hors ligne et se connecte à Internet à un moment ultérieur, Nintendo reçoit toujours des informations sur ce qui s’est passé pendant que la Switch était déconnectée.
 
    Pour désactiver une partie de cette télémétrie, il est conseillé de désactiver l’envoi de rapports d’erreur dans les paramètres système de la Switch. 
 
    Nintendo reçoit encore beaucoup d’informations, même avec ces options désactivées. 
    Nous ne pouvons pas non plus savoir si Nintendo décide un jour de chercher quelque chose dans les logs de la Switch et de bannir les gens rétrospectivement. 
    Ils ont également montré leur volonté d'étendre leur système de télémétrie au fur et à mesure des mises à jour du firmware.
 
    !!!tip "Actuellement, tous les bans ont été pour des actions très évidentes, en particulier:"
        - Des développeurs utilisant leurs Switch pour poke et faire du "reverse-engineering" des réponses des serveurs de Nintendo
        - Des personnes qui piratent des jeux et les utilisent en ligne
        - Des personnes remplaçant leurs images de profil par des images personnalisées
        - Des personnes utilisant des éditeurs de sauvegardes pour débloquer du contenu qui n’est pas encore disponible et l’utiliser en ligne (Splatoon 2)
        - Des personnes qui trichent en ligne en général (modification des statistiques des carts dans MK8)
        - Les gens qui installent des homebrews au format NSP, que Nintendo peut détecter avec leur télémétrie


    Atmosphère arrête certains, mais ***pas tous*** les signaux de télémétrie de Nintendo, et empêche les rapports de crash d’être envoyés. Cela signifie que Nintendo ne peut pas savoir si quelque chose, que ce soit un homebrew ou un jeux, s’est écrasé, et Atmosphere renvoie le journal de crash sur la carte SD pour aider les développeurs homebrew à diagnostiquer les problèmes. Toutefois, Nintendo reçoit toujours des informations sur les jeux qui ont été joués, et les rapport d’information du système général.

    Atmosphère n’est pas une solution miracle, et rien ne dit que Nintendo ne décidera pas un jour de bannir des consoles qui ont lancé des homebrew inoffensifs. Si vous avez peur d’être banni, alors n’utilisez pas d'homebrew pour l’instant. Atmosphère prend désormais en charge l'emuMMC (emuNAND) : une copie du logiciel systèm de la Switch, fonctionnant entièrement à partir de la carte SD. 
    Cela efface les risques de bans du fait que l’emuMMC est exécutée en quarantaine et hors ligne, ne touchant pas la mémoire interne. Vous serez toujours en mesure de démarrer dans le firmware officiel (OFW) pour jouer en ligne.

    Pour les unités patchées, dépendantes de Déjà-Vu, la sysNAND devra toujours être sur un firmware inférieur à 4.1. Pour les consoles de 5.0 à 7.0.1 Déjà-Vu n’est pas encore tout à fait opérationel, mais il le sera bientôt (veuillez également noter que les firmwares 8.0.0+ ne fonctionneront jamais avec Déjà-Vu). Vous pouvez utiliser une emuMMC mise à jour dédiée au jeu en ligne/propre, tandis que votre sysNAND sera utilisée hors ligne pour le CFW.
	
    Nous ne recommandons pas l’utilisation de ReiNX ou de SX OS pour de nombreuses raisons, la principale est qu’ils utilisent beaucoup d'éléments de la solution Atmosphère et n’offrent aucun avantage réel (rien qu’Atmosphère n’offre pas déjà).
    Nous ne recommandons pas non plus Kosmos, car avec sa grande quantité d’extras ajoutés en plus d’Atmosphère, il est difficile de résoudre des problèmes spécifiques. De plus Kosmos a été **archivé**.
    Tous ces CFW alternatifs ont également tendance à utiliser des configurations non conventionnelles qui peuvent causer des problèmes qui rendent difficile le dépannage, ce qui est une autre raison pour laquelle nous préférons utiliser Atmosphère.
    En outre, il est conseillé d’utiliser 90DNS qui bloque les connexions à tous les serveurs de Nintendo. Si vous utilisez une emuNAND pour lancer un CFW et gardez votre sysNAND propre pour jouer en ligne, vous devez utiliser 90DNS sur votre emuNAND.
    * Note : Garder votre emuNAND « sale » et votre sysNAND « propre » se rapporte principalement à ceux qui utilisent l’exploit RCM. Les utilisateurs utilisant Nereba ou Caffeine feront le contraire.*

## Quels sont les formats des homebrews ?

!!!tip ""

    Les homebrews peuvent être compilés dans deux formats différents, à savoir les formats `nro` et les formats `bin`.

    - Les fichiers au format `nro` sont placés dans le dossier `switch` sur votre carte SD et peuvent être lancés en utilisant le menu homebrew.
    - Les fichiers au format `bin` sont utilisés comme des payloads et peuvent être envoyés en RCM en utilisant un injecteur de payload comme tegraRCMGUI sur Windows ou fusee-interfacee-tk sous Linux.
   
**Risques des homebrew**
*Soyez prudent avec le lancement d'un homebrew téléchargé sur intenet ou dans un pack ! Si vous ne connaissez pas la source, il est préférable de ne pas le lancer.*
*Un homebrew peut potentiellement endommager votre système ! Atmosphère offre des protections contre les méthodes de briques communes, mais leur fonctioonnement n'est pas garanti dans toutes les situations !*


## Quelle microSD/formattage devrais-je utiliser ?

!!!tip ""
    Les cartes microSD de 32 Go ou moins peuvent être utilisées pour lancer des homebrews, mais ne sont pas recommandées car celles-ci ne vous permettront pas d’avoir un backup complet de la NAND et/ou une emuMMC.

    La taille recommandée de la carte microSD est de 128 Go. Cela vous permettra de faire un backup complet de la NAND ainsi que d’avoir suffisamment d’espace pour exécuter une emuNAND tout en ayant suffisamment d’espace pour lancer des homebrews.

    Le format de système de fichiers recommandé est FAT32. Bien que la Switch prenne en charge le format exFAT par le biais d’une mise à jour supplémentaire de Nintendo, ce système de fichiers est toujours sujet à la corruption et, par conséquent, n’est pas conseillé.



## Fausses cartes microSD

!!!tip ""
    N’achetez pas de cartes microSD sur des sites comme eBay. 
    Ces cartes microSD sont souvent des "fausses" et ne possèdent pas la quantité de stockage annoncée, ce qui se traduira par la corruption des données si elle est utilisée. 
    Amazon a eu quelques problèmes avec des fausses cartes SD, nous vous recommandons donc de les acheter dans un magasin "physique". Même sur les sites dignes de confiance, *toujours, toujours vérifier les commentaires sur un produit avant d’acheter !*

    
    Si vous suspectez voutre carte dêtre une fausse, vous pouvez suivre les instructions données <a href="https://3ds.eiphax.tech/sd.html" target="_blank">ici</a> (*en anglais*) pour vérifier l’intégrité de votre carte SD.



## Mes homebrews ne s'affichent pas sur le menu

!!!tip ""
    Il s’agit d’un problème affectant principalement les utilisateurs de macOS, mais qui peut aussi se produire sur d’autres appareils. Si vous êtes en mesure de lancer le menu homebrew, mais que vous ne voyez qu'une partie ou aucun de vos homebrews, vous aurez besoin de réinitialiser l'archive bit avec Hekate.

    1. Lancez Hekate en suivant [ces instructions](user_guide/emummc/sending_payload_fr.md) si vous ne savez plus comment faire.
    2. Appuyez sur `Tools`.
    3. Dans le coin inférieur gauche appuyez sur `Archive bit * AutoRCM`
    4. Appuyez sur `Fix Archive bit`. Cela peut prendre un certain temps.
    5. Appuyez sur `Close` dans le coin supérieur droit.
    6. Appuyez sur `Home` pour revenir au menu principal.
    7. Lancez le CFW Atmosphère (si vous ne savez plus comment faire, se renseigner [ici](user_guide/emummc/launching_cfw_fr.md)).
