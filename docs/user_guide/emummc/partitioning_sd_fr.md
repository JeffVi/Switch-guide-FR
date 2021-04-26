# Partitionnement de la carte SD 

!!!warning "Cela supprimera tout ce qui est présent sur votre carte SD"
	Cela supprimera toutes vos données de votre carte microSD, soyez averti !

!!! warning "Sauvegardez votre dossier Nintendo"
	Avant de commencer, si vous utilisez déjà une carte microSD comme moyen stockage pour vos jeux, vous devriez déplacer le dossier `Nintendo` de la racine de votre carte SD vers votre ordinateur. Ce dossier contient vos jeux téléchargés et les mises à jour.

-----

## Préparations

Ce dont vous aurez besoin :

- La dernière version de <a href="https://github.com/suchmememanyskill/TegraExplorer/releases" target="_blank">TegraExplorer</a>

### Instructions

1. Injectez le payload **TegraExplorer** (et non pas Hekate, ne vous trompez pas car l'option est également disponible sous Hekate) avec votre carte SD de 64 Go (ou plus) insérée dans votre Switch.
	- Si vous avez oublié comment faire, relisez la page [envoyer un payload](sending_payload_fr.md) du guide.
2. Allez sur `Partition the sd` et appuyez sur le bouton A pour entrer dans le menu de formatage de la SD (il est possible de naviguer avec les touches VOL+, VOL- et valider avec le bouton power si vous n'avez pas de joycon attaché).
	- Si vous ne trouvez pas l'option `Partition the sd`, soyez sûr d'avoir inséré la carte SD dans la Switch et sélectionnez `Mount SD`.
3. Choisissez `Fat32 + EmuMMC`.
4. Lisez le message qui s'affiche et sélectionnez `Yes` pour créer la partition et lancer le formatage.
	- Note : Cela supprimera tout ce qui est présent sur votre carte SD. Soyez certains d'avoir récupéré votre dossier Nintendo !
	- Le processus devrait être assez rapide.
5. Appuyez sur un bouton pour retourner au menu.
6. Sélectionnez `Reboot to RCM` pour de nouveau entrer en RCM. Vous pouvez désormais récupérer votre carte SD et l'insérer dans votre PC.

!!! warning "Windows affiche un message d'erreur pour la carte SD"
    Si Windows vous informe que la carte SD est illisible et qu'il veut la formater, ne pas formater ! C’est probablement votre partition emuMMC. Après la partition de votre SD, celle-ci s’affichera sous forme de 2 lecteurs sur votre PC. Utilisez le lecteur accessible.
    
&nbsp;

#### [Continuer sur préparation de la SD <i class="fa fa-arrow-circle-right fa-lg"></i>](sd_preparation_fr.md)
