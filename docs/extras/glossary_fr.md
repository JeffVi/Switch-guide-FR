# Glossaire du hacking

Cette section est consacrée à l'explication d'un certain nombre de termes communs qui sont utilisés lors du hack de la Nintendo Switch ainsi que de relier un certain nombre de ressources qui peuvent aider les développeurs ou les utilisateurs curieux *en anglais*.

## Termes utiles

The following list is in alphabetical order.

- **90DNS** : DNS qui bloque les mises à jour système de la Nintendo Switch. Il peut être parammétré en suivant [ce guide](blocking_updates_fr.md).
- **[Atmosphère](https://github.com/Atmosphere-NX/Atmosphere)** : Le CFW développé par l'organisation Atmosphere-NX sur GitHub et qui est utilisé dans ce guide.
- **AutoRCM** : Une méthode qui corrompt certaines parties de votre boot0 et boot1, ce qui force la Switch à automatiquement démarrer en RCM. Utiliser cette fonctionnalité vous obligera à utiliser un périphérique extérieur (comme un ordinateur, un téléphone ou un dongle) pour pouvoir démarrer votre Switch.
- **boot0 and boot1** : Deux partitions de la NAND de la Switch.
- **CFW** : Acronyme pour custom firmware. Un custom firmware vous permet de modifier la façon de fonctionner de votre console.
- **Déjà Vu** : Une faille non publiée de la Nintendo Switch. L'utilisation de cette "chain" donne accès à "TrustZone", ce qui veut dire pouvoir entrer en CFW. La "TrustZone" utilisée par cette faille a été patché sur les versions 5.0.0 et plus, mais un accès homebrew normal peut être effectué jusqu'au firmware 6.0.1.
- **DNS** : [Domain Name System](https://en.wikipedia.org/wiki/Domain_Name_System). Fondamentalement, c’est le carnet d’adresses d'Internet. Si vous visitez un site Web, c’est le DNS qui vous indique sur quel serveur le site est hébergé.
- **Dongle** : Appareil que vous pouvez brancher dans le port de charge de votre Switch pour envoyer automatiquement un payload si votre Switch est en RCM.
- **Encryption keys** : Les keys utilisées pour chiffrer les fichiers de la Nintendo Switch. Celles-ci peuvent être récupérées en suivant le guide [ici](dumping_title_keys_fr.md).
- **BIS keys** : Des keys spécifiques utilisées pour décrypter la NAND.
- **[fusée-gelée](https://github.com/Qyriad/fusee-launcher/blob/master/report/fusee_gelee.md)/[ShofEL2](https://github.com/fail0verflow/shofel2)** : Deux noms pour deux implémentations différentes d’un même exploit. Il s’agit d’un exploit qui donne un accès bootrom complet à la MRC Tegra X1s de la Nintendo Switch et permet d’exécuter CFW. Cet exploit nécessite un périphérique externe et une petite modification matérielle. fusée-gelée est développé par un ancien développeur ReSwitched, tandis que ShofEL2 est développé par l’équipe failoverfl0w. Ce guide utilise fusée-gelée.
- **[hactool](https://github.com/SciresM/hactool)** : Logiciel utilisé pour décrypter les fichiers de la Nintendo Switch comme les fichiers .XCI et .NSP.
- **[Hekate](https://github.com/CTCaer/hekate)** : Un bootloader pour la Nintendo Switch. Le guide actuel l’utilise en combinaison avec des fichiers essentiels d’Atmosphère pour démarrer un CFW.
- **Homebrew** : Code non signé qui peut être lancé sur la Nintendo Switch. Il existe de nombreux homebrews comme des éditeurs de sauvegarde, des émulateurs, mais peuvent également inclure des jeux complètement originaux. Pour exécuter ce code, vous devez avoir un exploit (faille).
- **Homebrew launcher** : Logiciel développé par l’équipe Switchbrew et qui vous permet d’exécuter d’autres Homebrew.
- **Jig** : Fait référence à un morceau matériel (fil de fer dans un petit support en plastique) que vous pouvez mettre dans le rail Joycon pour entrer en RCM.
- **KIP** : Acronyme pour Kernel Initial Process. Ces fichiers peuvent être chargés lorsque la Switch démarre en CFW et fournir des fonctionnalités supplémentaires.
- **NAND** : Le système de fichiers interne utilisé par la Switch. Contient boot0 et boot1, ainsi que PRODINFO et diverses autres partitions.
- **nx-hbloader** : Programme utilisé pour charger le menu Homebrew du CFW, développé par Switchbrew. Livré avec atmosphère.
- **PRODINFO** : Une partition sur la NAND de votre Switch. Cette partition (avec boot0 et boot1) est la seule de votre Switch qui peut la rendre inopérente si elle est incorrectement modifiée. Atmosphere sauvegarde cette partition au démarrage et elle est incluse dans votre sauvegarde de NAND.
- **ReSwitched** : Une équipe de hacking qui est l’un des principaux développeurs pour Atmosphere.
- **RCM** : Acronyme pour "Recovery Mode". Lorsque vous parlez de piratage de la Switch, cela se réfère généralement au mode de récupération dans la puce Tegra X1 qui est inclus dans la Nintendo Switch. Ce mode peut être lancé en maintenant le bouton d’accueil Tegra X1. Ce bouton n’est pas le même que le bouton d’accueil sur les joycons. Les moyens d’appuyer sur ce bouton peuvent être trouvés [ici](../user_guide/emummc/entering_rcm_fr.md).
- **[TegraRCMGUI](https://github.com/eliboa/TegraRcmGUI/releases)/[fusee-interface-tk](https://github.com/nh-server/fusee-interfacee-tk/releases)** : Logiciel utilisé pour exécuter l’exploit fusée-gelée sur la Switch.
- **Tegra X1** : [Une puce fabriquée par Nvidia qui est utilisée dans la Nintendo Switch.](https://en.wikipedia.org/wiki/Tegra#Tegra_X1)
- **Trinket** : Une petite puce qui est soudé sur la carte mère Switch pour envoyer automatiquement un payload si elle est en RCM.
- **TrustZone** : Le niveau de sécurité le plus élevé sur la Switch.
- **XCI/NSP** : Format utilisé pour copier les jeux, XCI est utilisé pour les copies de cartouches de jeu, tandis que NSP est pour la copie des jeux digitaux. On parle de *dump* de jeux.

## Resources

Les ressources ci-dessous sont pour les utilisateurs et les développeurs intéressés par le développement Homebrew ou pour ceux qui veulent obtenir une compréhension plus technique des différents concepts.

- La [FAQ ReSwitched](https://reswitched.team/faq/) donne un aperçu général du fonctionnement de la Switch.
- [Switchbrew](https://switchbrew.org) est un wiki détaillant le fonctionnement interne du firmware de la Nintendo Switch.
- [documentation libNX](https://switchbrew.github.io/libnx/index.html). LibNX est la bibliothèque utilisée pour développer Homebrew sur la Nintendo Switch.
