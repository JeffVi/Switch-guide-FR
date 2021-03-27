# Tenir votre système à jour

Cette page explique comment vous pouvez maintenir votre système à jour.

Après avoir suivi notre guide, votre système sera composé de trois éléments de base qui peuvent être mis à jour. Atmosphère, Hekate et votre firmware système (version de la console).

## Mettre Atmosphère à jour

Lors de la mise à jour d'Atmosphère assurez-vous de toujours **lire les changements apportés** (*certes en anglais mais faites un effort !*). Ils peuvent énumérer les modifications importantes apportées à votre système.

Lorsqu’une nouvelle version d’Atmosphère sort, vous pouvez mettre à jour Atmosphère en suivant ces étapes :

1. Éteignez votre Nintendo Switch et insérez votre carte SD dans votre ordinateur.
2. Téléchargez la dernière version <a href="https://github.com/Atmosphere-NX/Atmosphere/releases" target="_blank">d'Atmosphère</a> (téléchargez l'archive `atmosphere-(version)-master-(version)+hbl-(version)+hbmenu-(version).zip` depuis les assets).
3. Copiez *le contenu* de l'archive Atmosphere `.zip` à la racine de votre carte SD.
    - Si vous êtes invité à remplacer/fusionner des fichiers, faites-le.
4. (Si votre Hekate n’est pas sur la dernière version) Mettez à jour Hekate via les étapes ci-dessous
5. Remetez votre carte SD dans votre Switch et lancez le CFW.

## Mettre Hekate à jour

Lors de la mise à jour d'Hekate assurez-vous de toujours **lire les changements apportés** (*certes en anglais mais faites un effort !*). Ils peuvent énumérer les modifications importantes apportées à votre système.

Lorsqu’une nouvelle version d’Hekate sort, vous pouvez mettre à jour Atmosphère en suivant ces étapes :

1. Éteignez votre Nintendo Switch et insérez votre carte SD dans votre ordinateur.
2. Téléchargez la dernière version <a href="https://github.com/CTCaer/Hekate/releases/" target="_blank">d'Hekate</a> (téléchargez l'archive `hekate_ctcaer_(version).zip` depuis les assets).
3. Copiez le dossier `bootloader` de l'archive Hekate `.zip` à la racine de votre carte SD. to the root of your SD card. Si vous êtes invité à remplacer/fusionner des fichiers, faites-le.
4. Remettez votre carte SD dans votre Switch et lancez Hekate.
5. Allez à l’onglet Options en haut à droite de l’écran. Mettez `Update Reboot 2 Payload` en bas à droite sur ON (si ce n'est pas déjà le cas). Appuyez sur `Save Options` en bas de l’écran.

## Mettre votre firmware à jour

Vérifiez toujours **avant** de mettre à jour votre firmware système si la dernière version d’Atmosphère, **ainsi** que la dernière version de Hekate, prennent en charge la version firmware que vous mettez à jour.

Actuellement, la dernière version prise en charge par Atmosphere et Hekate est: **11.0.1**.

En outre, certaines versions de firmwares mettent à jour le firmware du lecteur de cartouche. Référez-vous au le tableau ci-dessous pour plus d’informations à ce sujet.

| Votre version actuelle                 | La version que vous souhaitez installer            | Màj du lecteur de cartouche ? |
| -------------------------------------- | -------------------------------------------------- | ----------------------------- |
| En dessous de 4.0.0                    | En dessous de 4.0.0                                | Non                           |
| En dessous de 4.0.0                    | Au dessus de 4.0.0                                 | Oui                           |
| Entre 4.0.0 *inclus* et 9.0.0 *exclu*  | Entre 4.1.0 *inclus* et 9.0.0 *exclu*              | Non                           |
| Entre 4.0.0 *inclus* et 9.0.0 *exclu*  | 9.0.0 ou plus                                      | Oui                           |
| Entre 9.0.0 *inclus* et 11.0.0 *exclu* | Entre 9.1.0 *inclus* et 11.0.0 *exclu*             | Non                           |
| Entre 9.0.0 *inclus* et 11.0.0 *exclu* | 11.0.0 ou plus                                     | Oui                           |
| À partir de 11.0.0                     | Dernière version supportée par Atmosphere & Hekate | Non                           |

Si une des versions que vous mettez à jour met également à jour le firmware du lecteur de cartouche, vous ne serez pas en mesure de réutiliser une version en dessous de cette version sans rendre le lecteur de cartouche inutilisable (sous la version utilisée en tout cas).

Atmosphère (et Hekate) sont livrés livrés avec des patchs qui désactivent automatiquement le lecteur de cartouche s’il est détecté que le système a une mise à jour pour le lecteur de cartouche. Si vous démarrez en RCM à chaque boot de la console (par exemple en utilisant AutoRCM), cela signifie que le lecteur de cartouche ne sera pas mise à jour et vous pourrez ainsi réaliser un "downgrade". Si cela se produit, vous ne serez pas en mesure d’utiliser le lecteur de cartouche tant que vous êtes sur le firmware le plus récent.

Sinon, vous pouvez mettre à jour en toute sécurité votre firmware système à travers les paramètres du système de la console.

!!!warning "Note sur l'AutoRCM"
    Si vous avez activé AutoRCM et que vous mettez à jour votre système pendant que vous êtes en "stock" (c.à.d. sans CFW), **la mise à jour désactivera AutoRCM** et vous devrez entrer en RCM manuellement pour lancer à nouveau le CFW.
    Pour éviter que l’AutoRCM ne soit désactivé, démarrez en CFW sur votre sysMMC et mettez à jour depuis les paramètres système de la console, car le démarrage sans AutoRCM <ins> brûlera les fusibles préservés</ins>.

### À propos de l'emuMMC

sysMMC et emuMMC ont des firmwares système séparés et doivent être mis à jour indépendamment.

Si vous gardez votre emuMMC hors ligne, vous devrez utiliser une cartouche de jeu pour mettre à jour votre firmware système,ou bien la synchroniser avec une autre Nintendo Switch ou bien copier le firmware mis à jour de votre sysMMC.

## Mise à jour de l’emuMMC en utilisant un firmware mis à jour sur votre sysMMC

!!!warning "Avez vous un backup (sauvegarde) de votre eMMC ?"
    Ne vous lancez pas dans ce guide sans faire un backup de votre GPP RAW et des BOOT 0/1 de votre eMMC !

    Vous pouvez apprendre à en faire un [ici](../user_guide/sysnand/making_essential_backups_fr.md).

!!!danger "Downgrade"
    Ce guide est fait pour mettre à jour votre emuMMC. Il n'est **pas** fait pour réaliser un downgrade. Le downgrade en général, sysMMC ou emuMMC, n’est pas recommandé et n’en vaut pas la peine. Le downgrade est également très dangereux et peut entraîner de graves complications même lorsqu’il est effectué correctement.

### Ce dont vous aurez besoin

!!!tip ""
    - La dernière version de <a href="https://github.com/suchmememanyskill/TegraExplorer/releases" target="_blank">TegraExplorer</a>
    - La dernière version <a href="https://github.com/Atmosphere-NX/Atmosphere/releases" target="_blank">d'Atmosphère</a>

### Préparation de votre carte SD

1. Insérez votre carte microSD dans votre ordinateur.
2. Téléchargez `TegraExplorer.bin`.
3. Mettez à jour Atmosphère et Hekate en utilisant les guides sur cette page.
4. Si vous ne l'avez pas déjà fait, mettez à jour votre sysMMC.

### Récupération du firmware de votre sysMMC

1. Assurez-vous que votre sysMMC est à jour. Si votre sysMMC n’est pas à jour, mettez-le à jour dans les paramètres de la console.
2. Injectez `TegraExplorer.bin` (de la même façon que vous injectez n'importe quel payload, comme Hekate par exemple).
3. En utilisant le stick et le bouton A, sélectionnez `Dump Firmware`.
4. Attendez environ 1-2 minutes pour que le processus copie votre firmware.
5. Une fois terminé, appuyez sur n’importe quel bouton.
6. Sélectionnez `Reboot to atmosphere/reboot_payload.bin`.

### Mettre à jour votre emuMMC avec Daybreak

1. Dans Hekate, allez dans `Launch -> Atmosphere FSS0 Emu`.
2. Une fois démarré, maintenez `R` tout en lançant un jeu pour démarrer le menu homebrew.
3. Trouvez Daybreak et lancez-le.
4. Appuyez sur `Install` et allez dans `tegraexplorer/Firmware/<votre numéro de firmware>`.
5. Appuyer sur `Continue` et `Preserve settings`.
    - Si vous vous voyez `Warning: exFAT firmware is missing or corrupt`, vous n’avez probablement pas les drivers (pilotes) exFAT installés sur votre sysMMC. Il suffit d’appuyer sur continuer si c’est le cas.
6. Si possible choisissez `Install (FAT32 + exFAT)`, sinon `Install (FAT32)` puis `Continue`.
7. Attendez que Daybreak termine l’installation du firmware.
8. Une fois qu’il aura terminé, il vous demandera si vous voulez redémarrer. Appuyez sur `Reboot`.
9. Une fois redémarré, lancez votre emuMMC et vérifiez que votre système fonctionne. Vous pouvez vérifier que votre système a été correctement mis à jour dans les paramètres de la console.
