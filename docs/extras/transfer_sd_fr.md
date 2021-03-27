# Changement de carte SD

Le but de cette page est de transférer le contenu d’une carte SD à une autre. La méthode pour ce faire sera différente, selon que vous utilisez une partition pour votre emuMMC sur votre carte SD ou non.

Nous allons utiliser [hekate](https://github.com/CTCaer/hekate/releases/) pour créer un backup et pour pouvoir restaurer votre emuMMC, donc assurez vous d'avoir la dernière version sur votre carte SD.

## Instructions

Vous devez d’abord vérifier si votre emuMMC est partitionnée ou sous forme de fichiers :
    
1.  Injectez le payload Hekate.
2.  Appuyez sur `emuMMC`.
3.  Dans `emuMMC Info & Selection`, lisez le texte à coté de `Type`.
    - Si vous avez une emuMMC, vous devriez voit `SD Raw Partition` ou `SD File`.

-----
### Si vous utilisez une emuMMC sous forme de fichiers `SD File`, **ou** si vous n'avez pas d'emuMMC :
        
1.  Retirez votre carte SD (après avoir éteint votre console).   
2.  Insérez votre "ancienne" carte SD dans votre ordinateur.
3.  Copiez le contenu de votre carte SD sur votre ordinateur.
4.  Éjectez votre carte SD et insérez votre "nouvelle" carte SD.
5.  Formatez votre "nouvelle" carte SD en FAT32 si ce n'est pas déjà le cas.
    - Pour ce faire, vous pouvez utiliser [guiformat](http://ridgecrop.co.uk/index.htm?guiformat.htm) sur Windows.
6.  Copiez les fichiers de votre PC sur votre "nouvelle" carte SD et vous avez terminé.

-----
### Si vous utilisez une emuMMC partitionnée (`SD Raw Partition`) :
    
!!!warning "Espace nécessaire pour le backup"
    Vous aurez besoin d’au moins 30 Go d’espace libre pour être en mesure de sauvegarder et de restaurer l’emuMMC !

1.  Injectez le payload Hekate.
2.  Dans le menu principal, apuuyez sur `Tools`, puis sur `Backup eMMC` et mettez `SD emuMMC Raw Partition` sur `ON`.
3.  Lancez le backup pour `SD emuMMC BOOT0 & BOOT1` et `SD emuMMC RAW GPP` (Note : raw gpp peut prendre un certain temps).
4.  Une fois les deux backups terminés, retournez sur le menu principal, retirez votre carte SD et insérez-la dans votre PC.
5.  Si Windows vous demande de formater un lecteur, refusez et sélectionnez le lecteur avec votre contenu SD.
6.  Copiez le contenu de votre carte SD sur votre PC.
7.  Suivez les instructions de [cette page](https://switchgui.de/switch-guide/user_guide/emummc/partitioning_sd_fr/) pour partitionner la "nouvelle" carte SD pour une configuration emuMMC.
8.  Une fois que c’est fait, éteignez votre Switch, retirez votre carte SD de votre Switch et insérez la dans votre PC.
9.  Copiez le contenu de votre "ancienne" carte SD sur votre "nouvelle".
10. Allez dans le dossier `/backup/<identifiant>/` sur votre carte SD et déplacez les fichiers `BOOT0`, `BOOT1` et `rawnand.bin.xx` dans le dossier `restore`.
11. Éjectez la carte SD et insérez-la dans votre Switch.
12. Injectez le payload Hekate.
13. Dans le menu principal, apuuyez sur `Tools`, puis sur `Restore eMMC`, mettez `SD emuMMC Raw Partition` (en bas de l'écran) sur `ON`.
14. Lancez la restauration du backup en appuyant sur `SD emuMMC BOOT0 & BOOT1` et `SD emuMMC RAW GPP` (Note : raw gpp peut prendre un certain temps).
    - Il est très important que, pour ces deux restaurations l'option `SD emuMMC Raw Partition` soit activée, sinon vous allez écraser votre sysMMC, et ce n'est pas du tout ce que vous voulez !
15. Votre emuMMC est maintenant opérationelle et vous devriez pouvoir la lancer via `Launch` -> `Atmosphere FSS0 EmuMMC` depuis Hekate.
