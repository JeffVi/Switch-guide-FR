## Partitionner sous Linux

!!! danger "Identification de la carte SD"
	Assurez-vous à 100 % d’utiliser votre carte microSD pendant les étapes suivantes. Si vous n’êtes pas prudent, vous pouvez finir par effacer l’ensemble de votre système de fichiers linux. Nous ne sommes pas responsables de la perte de données en cas de mauvaise manipulation.

!!! warning "À qui s'adresse cette page ?"
	Cette section s’adresse aux personnes qui ne veulent pas laisser un outil modifier automatiquement leur SD, et qui veulent le faire manuellement pour plus de contrôle sur ce qui est créé.

!!! tip "Ce dont vous aurez besoin (Linux)"
    - La dernière version de `gparted`
    - La dernière version de `fdisk`
    - Un accès à un compte administrateur.

### Manuel d'instructions (Linux)

1. Ouvrez un terminal.
2. Lancez `sudo fdisk -l`. Entrez votre mot de passe si vous le devez. Cela permettra d'afficher des informations sur tous les lecteurs connectés à votre ordinateur. Utilisez les informations sur la taille des fichiers pour identifier votre carte microSD. Plus précisément, prenez note de la ligne après `Disk `. Cela va ressembler à `/dev/xxx`, où `xxx` sera différent selon votre système (pas forcément 3 caractères). Il ne se TERMINE PAS par un chiffre.
3. Lancez `sudo gparted <value>`. Entrez votre mot de passe si vous le devez. Remplacez `<value>` par l'information obtenue à l'étape 2.
4. Vous verrez une liste de partitions sur votre carte SD. Allez à `Device` -> `Create partition table`. Sélectionnez `msdos` comme type de partition (partition type) et sélectionnez Apply. Cela va supprimer toutes les partitions existantes sur votre carte SD.
5. Allez à `Partition` -> `New`. Réalisez les modifications suivantes :
    - Mettez `Free space following (MiB)` à `30000`. 
    - Mettez `Free space preceding (MiB)` à `1`. 
    - Mettez `File system` à `fat32`. 
    - Mettez le `Label` à `sMicroSD`. 
    - Ne touchez à rien d'autre et appuyez sur `Add`.

		![gparted](../img/gparted.png)

1. En haut de gparted, vous verrez maintenant un grand espace gris vers la droite. Effectuez un clic droit sur cet espace, sélectionnez `New`.
2. Mettez `File system` à `linux-swap`. Mettez `Label` à `emuMMC`. Ne touchez à rien d'autre et appuyez sur `Add`.
3. Cliquez sur l’icône de contrôle dans la barre d’outils.
4. Attendez la fin de l'opération. Ça pourrait prendre un moment.
5. Fermez `gparted`.

!!!info "Erreur NOFAT dans Hekate"
	Cette erreur peut se produire après avoir effectué les étapes précédentes avec une microSD de 64 Go. La raison est qu'Hekate s’attend à ce que la partition FAT32 utilise une taille de cluster de 32k, que gparted ne fait par défaut que si la partition est supérieure à 32 Go, ce qui n'est probablement pas le cas sur une microSD de 64 Go. **Cela effacera toutes les données sur votre partition FAT32**.

	Pour résoudre ce problème, suivez ces instructions :

	1. Ouvrez un terminal.
	2. Lancez `sudo fdisk -l`. Entrez votre mot de passe si vous le devez. Cela permettra d'afficher des informations sur tous les lecteurs connectés à votre ordinateur. Utilisez les informations sur la taille des fichiers pour identifier votre carte microSD. Plus précisément, prenez note de la ligne après `Disk `. Cela va ressembler à `/dev/xxx`, où `xxx` sera différent selon votre système (pas forcément 3 caractères). Il ne se TERMINE PAS par un chiffre.
	3. Lancez `sudo mkdosfs <value> -s 64 -F 32 -I`. Entrez votre mot de passe si vous le devez. Remplacez `<value>` par l'information obtenue à l'étape 2.
	4. Attendez que l'opération se termine. Selon la taille de votre carte microSD, cela peut prendre un certain temps.
	5. Lancez `sudo fatlabel <value> "sMicroSD"`. Entrez votre mot de passe si vous le devez. Remplacez `<value>` par l'information obtenue à l'étape 2.

&nbsp;

#### [Continuer sur la préparation de la SD <i class="fa fa-arrow-circle-right fa-lg"></i>](sd_preparation_fr.md)
