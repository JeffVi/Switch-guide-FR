<a href="https://discord.gg/C29hYvh" target="_blank"><img style="float: right;" src="img/discord.png"></a>

# NH Switch Guide

Un guide collaboratif de la communauté des "Helpers" et du "Staff" de Nintendo Homebrew, traduit par un "Fantastic Dreamer". *From stock to Atmosphère !*

&nbsp;

!!! tip "Aide Discord"
    Pour une assistance *en anglais* en direct avec ce guide, contactez **#switch-assistance** sur le [Discord Nintendo Homebrew](https://discord.gg/C29hYvh).
    
    Pour une assistance, une question, une remarque, une proposition ou une correction à propos de ce guide, n'hésitez pas à rejoindre le [Discord NX FR](https://discord.gg/Qe6aKneVMy), serveur *en français* !

### Qu’est-ce que homebrew ?

!!! tip ""
    Homebrew est un terme pour les logiciels non-officiels écrits par des amateurs et des développeurs amateurs pour les systèmes propriétaires (comme la Switch).

    Cela peut inclure des éditeurs de sauvegardes, des jeux, des émulateurs et plus encore.

    Homebrew peut être exécuté gratuitement sur votre Switch via un CFW tant que vous avez un système de «première génération», avec une version logicielle de 12.0.0 ou moins, et un câble USB-C.

### Qu’est-ce qu'un Custom Firmware ?

!!! tip ""
    Un Custom Firmware (“CFW”) est un logiciel qui modifie le logiciel système (firmware système).
    Atmosphère, par exemple, le fait en tournant à l'arrière plan du système et en appliquand des "patches" pendant que le système est allumé.

    Cela permet d’étendre les fonctionnalités de leur système en donnant aux homebrews des niveaux plus élevés de permission que la plupart des exploits "userland" et qui peut donc être utilisé pour fournir des fonctionnalités supplémentaires pour les développeurs homebrew et les utilisateurs, comme par exemple de pouvoir modder des jeu en utilisant LayeredFS.

    Le CFW peut être mis en place sur n’importe quelle console de première génération sur n’importe quelle version (mais nécessitera des outils supplémentaires).

### Qu’est-ce que ce guide installe ?

!!! tip ""
    Ce guide a pour objectif final de prendre une Switch non modifiée à l'état "stock" (nom de l'état sans modifications) au CFW Atmosphère.

    fusée-gelée est actuellement la meilleure méthode de lancement du CFW qui nous donne presque un contrôle total du système. Il utilise une vulnérabilité dans le bootROM des systèmes Switch de première génération, ce qui nous permet d’envoyer n’importe quel payload dans le mode de récupération de la Switch (RCM), au lieu de seulement ceux que Nintendo a autorisé.

### Que puis-je faire avec un Custom Firmware ?

!!! tip ""
    * Customisez votre menu HOME avec des thèmes personnalisés créés par d'autres utilisateurs
    * Utilisez des “ROM hacks” pour les jeux que vous possédez
    * Récupérer, éditer, et restaurer des sauvegardes pour de nombrex jeux
    * Jouer à des jeux rétros avec divers émulateurs, comme RetroArch
    * Mettre à jour votre système en toute sécurité sans risque de ne plus avoir accès aux homebrews

### Que dois-je savoir avant de démarrer ?

!!! tip ""
    Avant de commencer le guide, vous devez connaître les risques du piratage de la Switch : chaque fois que vous modifiez votre système, il y a toujours le risque d’un brick IRRÉCUPÉRABLE. Ils sont rares, mais il y a toujours toujours une possibilité alors assurez-vous de suivre PRÉCISÉMENT TOUTES les instruction.

    Ce guide porte sur les consoles Switch de première génération dans toutes les régions sur un firmware 12.0.0 ou moins.

    Vous aurez besoin **de l’un** des éléments suivants afin de poursuivre avec ce guide :

    - Un câble USB-A vers USB-C, et un PC
    - Un câble USB-OTG, un câble USB-A vers USB-C et un appareil Android
		- Cela ne fonctionne pas sur tous les téléphones Android
    - Un câble USB-C, et un appareil Android avec un port USB-C
    - Un adaptateur Lightning-OTG, un câble USB-A vers USB-C et un appareil iOS jailbreaké
        - Cette méthode n’est pas présentée dans ce guide, mais vous pouvez en savoir plus à ce sujet sur [ce site](https://mologie.github.io/nxboot/)


    Vous aurez également besoin d’une carte micro SD d’au moins 64 gigaoctets si vous prévoyez de suivre ce guide et créer une emuMMC, ce qui est plus sûr et fortement recommandé. Si vous devez utiliser une carte SD plus petite, il est possible d'utiliser la sysMMC, mais c'est fortement déconseillé.

    Enfin, vous aurez besoin d’un moyen d’accéder au mode Récupération. (Cela sera expliqué plus en détail dans la section *Entrer en RCM*)

Si tout se passe comme prévu, vous ne perdrez pas de données et vous retrouverez de nouveau tout ce avec quoi vous avez commencé (jeux, compte Nintendo, sauvegardes, etc. seront préservés).

Gardez votre appareil branché et chargé tout au long du processus afin d’éviter la perte de données ou les dommages causés par une panne de courant inattendue.

Le Custom Firmware n’est pas permanent avec les méthodes actuelles, et sera supprimé lors du redémarrage du système.

**Il est conseillé de lire l’intégralité du guide, du début à la fin, une ou plusieurs fois, avant de réellement se lancer dans les manipulations**

&nbsp;

#### [Continuer sur la première étape <i class="fa fa-arrow-circle-right fa-lg"></i>](user_guide/getting_started_fr.md) 
