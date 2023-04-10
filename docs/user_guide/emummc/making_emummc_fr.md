# Créer l'EmuMMC, obtenir ses keys, et réaliser les sauvegardes essentielles (backups)

&nbsp;

### Créer l'emuMMC

!!!warning "Avant de commencer"
    Si vous ne prévoyez pas d'utiliser internet sur votre emuMMC, il est recommendé d'allumer votre Switch normalement et de supprimer tous les réseaux wifi. Vous pourrez de nouveau les ajouter à votre sysnand après avoir terminé ce guide.

!!!tip ""
    1. Entrez en RCM et injectez le payload Hekate.
    2. Utilisez l’écran tactile pour aller sur `emuMMC`
    3. Cliquez sur `Create emuMMC`, puis sur `SD Partition`
    4. Cliquez sur `Part 1`. La création de l'emuMMC va commencer. Une fois qu’elle est terminée, revenez au menu emuMMC en utilisant le bouton `Close`
    5. Cliquez sur `Change emuMMC`, puis sur `SD RAW 1`
    6. Retournez sur le menu principal

!!!warning "Après la création de l'emuMMC"
    Votre sysMMC et emuMMC ne partagent pas le même dossier Nintendo ! Après avoir créé votre emuMMC, copiez le dossier `Nintendo` à la racine de votre carte sd dans le dossier `emummc\RAW1`.

-----

### Créer un backup de la NAND


!!! danger "Important"
    Un backup (sauvegarde) de la NAND est crucial. Il peut être utilisé pour réparer le système en cas d'urgence.

	Une fois la sauvegarde terminée, **gardez-la dans un endroit sûr.** La meilleure sauvegarde est celle que vous avez mais dont vous n'avez jamais besoin, et la pire sauvegarde est celle dont vous avez besoin mais que vous n'avez pas. Pour économiser de l’espace, il est recommandé de compresser le résultat final dans un fichier « .zip » ou quelque chose de similaire.

	Il est fortement recommandé d’utiliser une carte SD formatée en FAT32 et dont l’espace libre est d’au moins 32 gigaoctets. Cela fonctionnera évidemment sur des cartes plus petites, mais ce n’est pas idéal.

### Instructions

!!! tip ""
    1. Entrez en RCM et injectez le payload Hekate.
    2. Utilisez l'écran tactile pour accéder à `Tools` puis à `Backup eMMC`.
    3. Cliquez sur `eMMC BOOT0 & BOOT1`.
       - Cela ne devrait prendre que quelques secondes, mais si votre carte SD est très lente, cela peut prendre jusqu'à une minute.
    4. Cliquez sur `Close` pour continuer, puis cliquez sur `eMMC RAW GPP`.
       - Cela prendra beaucoup de temps. Attendez-vous à devoir attendre entre 10 minutes et une heure (ou plus, si votre carte SD est très lente).
       - Sur les cartes SD en FAT32, ou les cartes qui ont moins de 32 gigaoctets d’espace disponible, la NAND sera divisée en fichiers de 1 ou 2 gigaoctets.
          - Hekate cessera de créer ces fichiers lorsqu’il sera à court d’espace. Si cela se produit, procédez comme suit :
          - Éteignez la console.
          - Insérez votre carte SD dans votre PC.
          - Déplacez tous les fichiers du dossier `backup` de votre carte SD vers votre PC afin de le conserver précieusement.
          - Insérez votre carte SD dans votre Switch.
          - Entrez de nouveau en RCM, injectez de nouveau Hekate, et reprenez la création du backup en allant dans `Tools` > `Backup eMMC` > `eMMC RAW GPP`.
          - Répétez la procédure jusqu'à ce que la totalité de la NAND soit sauvegardée.
    5. Appuyez sur `Close` > `Home` > `Power Off`.
    6. Insérez votre carte SD dans votre PC.
    7. Copiez le dossier `backup` de votre carte SD vers votre PC afin de le conserver précieusement. Vous pouvez ensuite le supprimer de votre SD sans crainte.

&nbsp;

-----

### Obtenir les clés (keys) uniques de votre console

!!! danger "Important"
    Ces clés sont essentielles à avoir. En cas d’urgence, elles peuvent être utilisés conjointement avec votre sauvegarde NAND et d’autres outils pour restaurer votre console à un état de fonctionnement.
    
!!!tip ""
    1. Entrez en RCM et injectez le payload Hekate
    2. Cliquez sur le bouton `Payloads` et lancez Lockpick_RCM.bin.
    3. Si Lockpick_RCM vous demande de choisir entre SysNAND et EmuNAND, choisissez SysNAND en naviguant avec les boutons de volume et en validant avec le bouton power. Si ce n’est pas le cas, continuez à l’étape 4.
    4. Lockpick_RCM devrait maintenant vous informer que vos clés ont été sauvegardées dans `/switch/prod.keys` sur la carte SD.
    5. Appuyez sur un bouton pour revenir au menu.
    6. Allez sur `Power off` avec les boutons de volume et validez avec le bouton power.
    7. Insérez votre carte SD dans votre PC.
    8. Copiez le fichier `prod.keys` du dossier `switch` de votre carte SD card sur votre PC afin de le conserver précieusement. *Ne les supprimez pas de la carte SD !*

&nbsp;

#### [Continuer vers lancer un CFW <i class="fa fa-arrow-circle-right fa-lg"></i>](launching_cfw_fr.md)
