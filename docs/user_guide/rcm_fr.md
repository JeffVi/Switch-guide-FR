# RCM

RCM (ReCovery Mode) est un mode pour la Switch qui permet à Nintendo d'envoyer des commandes à la console pour effectuer différentes tâches. Il a été découvert que sur des Switches non patchées, il est possible d'envoyer un payload afin de surcharger le buffer mémoire et ainsi accéder au système. C'est ce que l'on utilise ici pour lancer atmosphère.

!!!tip "emuNAND vs emuMMC vs sysNAND"
	- sysNAND est le diminutif de System NAND, qui correspond à la mémoire interne de la Switch.
	- emuNAND est le diminutif de emulated NAND, ce qui veut dire que l'entièreté de votre NAND (mémoire du système) va tourner sur la carte microSD avec un Custom Firmware (CFW). Le contenu de cette NAND émulée (jeux, applications, sauvegardes, paramètres, etc.) est *complètement séparé* de votre sysNAND.
	- emuMMC est le nom de l'emuNAND qui est utilisé par la console. À part le nom, il n'y a aucune différence avec l'emuNAND.

----

### emuNAND CFW (**Recommandé**)

!!!tip "Prérequis pour une emuNAND"
	- Une carte microSD de 64GB ou plus

	#### Avantages d'utiliser l'emuNAND plutôt que le CFW sur la sysNAND :
	
	- Utiliser des applications homebrew comme un éditeur de sauvegardes, utiliser des codes de triche dans des jeux hors ligne sans "salir" ou affecter votre sysNAND. Ainsi votre sysNAND peut être utilisée en ligne sans risque de bannissement de la console.
	- Permettre aux pocesseurs des Switches patchées d'utiliser Caffeine pour mettre à jour leur emuNAND et l'utiliser en ligne, tout en gardant leur sysNAND à une version antérieure et vulnérable.

&nbsp;

#### [Continuer pour entrer en RCM <i class="fa fa-arrow-circle-right fa-lg"></i>](emummc/entering_rcm_fr.md)
-----


### sysNAND CFW (**Non recommandé**)

Cette partie s'adresse aux personnes ne disposant pas d'une carte microSD d'au moins 64GB, ou qui ont une raison personnelle de ne pas utiliser une emuNAND.

!!!note "Note"
	Si vous créez une emuNAND, vous pourrez toujours lancer un CFW sur votre sysNAND si vous le souhaitez. Vous n'avez pas besoin de suivre spécifiquement le guide ci-dessous, tous les fichiers sont identiques. Vous avez simplement à lancer "sysNAND CFW" depuis Hekate/Nyx.

&nbsp;

#### [Continuer sur la préparation de la SD (sysNAND CFW) (**Non recommandé**) <i class="fa fa-arrow-circle-right fa-lg"></i>](sysnand/sd_preparation_fr.md)
