## Restaurer un backup (sauvegarde) de la NAND de la Switch

!!! danger "Attention :" 	
	-Cela réinitialisera toutes vos sauvegardes, jeux, version système et autres paramètres système au point où vous avez fait la sauvegarde de la NAND. Gardez cela à l’esprit, car vous n’avez probablement pas à restaurer un backup de la NAND sauf si vous avez brické votre switch ou que vous voulez retourner en ligne en toute sécurité après avoir utilisé un CFW.
	
	-Si vous allez restaurer une vielle NAND qui va modifier votre firmware, il est préférable de créer une deuxième sauvegarde (backup) de la NAND avant de restaurer le premier au cas où quelque chose se passe mal.

### Ce dont vous aurez besoin :
- Votre `rawnand.bin` (combiné ou en 15 ou 30 parties)
- Votre `BOOT0` et `BOOT1`
	- S'il vous manque l’un des fichiers ci-dessus, demandez de l’aide sur le serveur Discord [Nintendo Homebrew](https://discord.gg/C29hYvh) *en anglais*.
- Le payload <a href="https://github.com/CTCaer/hekate/releases/" target="_blank">Hekate</a>
- Une carte microSD de plus de 32 Go

### Instructions :

Avant de commencer, vérifiez si vous avez une arborescence de fichiers appelé `backup/[id de la NAND en 8 caractères]/restore` sur votre carte SD.

!!! warning "Si vous ne voyez pas de dossier backup ou de dossier [id de la NAND en 8 caractères] sur votre carte SD :"
	Cela signifie que vous n’avez pas fait de sauvegarde de votre NAND, il est fortement recommandé d’en faire un dès que possible. Suivez les étapes ci-dessous pour en faire une.

	1. Lancez la dernière version du payload Hekate sur votre Switch.
	2. Allez à `Tools > Backup eMMC > eMMC BOOT0 & BOOT1` et attendez la fin du processus.
	3. Une fois terminé, vous avez un dossier `backup/[id de la NAND en 8 caractères]/restore` sur votre carte SD. Continuez avec l'étape un de ce guide.

1. Copiez votre `rawnand.bin` (combiné ou en 15 ou 30 parties), `BOOT0`, et `BOOT1` dans le dossier `backup/[id de la NAND en 8 caractères]/restore` sur votre carte SD.
2. Mettez votre carte SD dans votre Switch et lancez Hekate.
3. Allez à `Tools > Restore eMMC`. Sélectionnez `Restore eMMC BOOT0 & BOOT1`. Attendez que le processus se termine.
4. Dans le même menu, sélectionnez `eMMC RAW GPP` et attendez que le processus se termine. Cela va prendre un long moment.

!!! danger "Si vous modifiez la version du système avec la restauration de la NAND"
	Si la version de sécurité sur laquelle vous étiez avant d’effectuer la restauration de la NAND est plus élevé que la sauvegarde de la NAND elle-même, vous devez activer AutoRCM de ne pas rester coincé dans une boucle de démarrage.
	Une mise à jour du système est considérée comme une version de sécurité lorsqu’un fusible est brûlé, vous pouvez regarder **<a href="https://switchbrew.org/wiki/Fuses#Anti-downgrade" target=blank>quelles versions brûlent les fusibles ici</a>**.

	Si vous avez activé AutoRCM avant de passer à une nouvelle version de sécurité (et que vous l'avez toujours activé après la mise à jour), vous n’avez pas à le faire.

	1. Dans le menu Hekate, allez dans `Tools` et aller au bas de la page où vous trouverez un bouton appelé `Archive bit - AutoRCM`
	2. Appuyez sur le bouton `AutoRCM` et vous verrez le message `ON`affiché. Cela signifie qu’il est activé.
