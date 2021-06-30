## AutoRCM

!!! tip "Qu'est-ce que AutoRCM ?"
	L'AutoRCM pousse la console à croire qu'elle est brick (inutilisable), ce qui la pousse à automatiquement passer en RCM pour être réparée, sans avoir besoin de jig. Puisque le RCM est à l'origine créé pour les réparateurs, c'est une fonctionnalité native de l'appareil, aussi appelé "softbrick". Si vous n'êtes pas prudent, une mauvaise utilisation de l'AutoRCM peut créer de vrais **dégats** sur votre appareil, tout particulièrement s'il s'agit d'un modèle qui ne peut pas recevoir de payload (comme les Mariko). Faites bien attention en utilisant cette fonctionnalité : la consolle ne pourra plus démarrer sans une aide extérieure (vous aurez besoin d'un PC, d'un téléphone, ou de tout autre appareil pouvant injecter un payload).

	Note : Si l’écran de la console reste noir lorsque vous appuyez sur le bouton d’alimentation après l’activation d’AutoRCM, n’oubliez pas que c'est normal. La console est en RCM.

!!! warning "Si vous n'avez pas encore une sauvegarde (backup) de vos BOOT0/1"
	Vous voulez vraiment détruire votre console, hein ? Si vous n’avez pas encore effectué de sauvegarde BOOT0/1, il est recommandé d’en faire une **MAINTENANT**.

	1. Lancez Hekate
	2. Allez dans `Tools` et sélectionnez `Backup eMMC`
	3. Appuyez sur `eMMC BOOT0 & BOOT1` et attendez la fin du processus.

!!! danger "Inconvénients de AutoRCM"
	Il y a quelques inconvénients que vous devriez considérer avant d’installer AutoRCM :

	- Gardez à l'esprit que votre console ne peut plus démarrer sans une aide extérieure après avoir été éteinte.
		Note : Le mode Veille n’est pas considéré comme « éteindre» la console. Le mode veille fonctionnera toujours comme prévu et est totalement inchangé par l'AutoRCM.
	- Une fois complètement déchargée, votre Switch prendra beaucoup de temps à charger en RCM. Pour résoudre ce problème, chargez la console pendant une vingtaine de minutes avant de démarrer dans Hekate et de choisir une option de démarrage. Une fois le démarrege effectué, la console va de nouveau charger à une vitesse normale (avec une icône de batterie dans le coin).

!!! tip "Avantages de AutoRCM"
	AutoRCM peut être une bonne solution :

	- Si vous avez eu des difficultés pour entrer en RCM (c.-à-d. que vous utilisiez la méthode du papier d’aluminium), maintenant vous pouvez entrer en RCM sans aucune difficulté.
	- Si vous voulez garder les fusibles (fuses) non brûlés, vous pouvez le faire avec AutoRCM, car la Switch n’aura jamais l'occasion de les brûler.
		Note : La mise à jour de la console lors du démarrage dans la configuration « stock » de Hekate va effacer AutoRCM au prochain redémarrage. Pour l'éviter, pensez à mettre à jour tout en utilisant le CFW, ou assurez-vous d’utiliser un jig après le redémarrage de la console pour de nouveau entrer en RCM.
	- Il est plus facile d’injecter un payload car il n’est plus nécessaire d’utiliser votre jig pour démarrer en RCM.

!!! tip "Informations complémentaires"
	- Cette méthode corrompt un byte dans vos partitions BOOT0 et BOOT1. C’est pourquoi une sauvegarde de ceux-ci est recommandé.
  - Cette version d’AutoRCM peut presque toujours être supprimée, alors ne paniquez pas si cela ne fonctionne pas comme vous le souhaitez.

Si, malgré tous les avertissements ci-dessus, vous souhaitez toujours installer AutoRCM, et que vous comprenez les risques, faites ce qui suit :

1. Lancez Hekate
2. Allez dans `Tools`
3. En bas du menu, appuyez sur `Arch Bit • AutoRCM • Touch • Pkg1/2`
4. Appuyez sur `AutoRCM`. Cela affichera un `ON` à côté de l'option une fois le processus mis en place.
