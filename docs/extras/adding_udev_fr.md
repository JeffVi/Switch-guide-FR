# Linux - Lancer un payload sans être un super-utilisateur

Cette section détaille comment ajouter une règle udev pour vous laisser envoyer un payload à la Nintendo Switch sans avoir besoin d’utiliser `sudo`.

!!! tip ""
    Les instructions suivantes ne fonctionnent que si vous avez un système qui implémente `udev`. La pluspart des distributions actuelles contiennent `systemd` qui inclus une implémentation `udev`.

!!! tip ""
    Réalisez les instructions suivantes pendant que votre Switch n'est **pas** connectée à votre ordinateur.

&nbsp;

## Option 1 : Ajout manuel de règles et de groupes

!!! tip ""
    Les instructions suivantes ne sont pas pour les débutants. Ne le faites que si vous comprenez ce que vous faites.

### Création d’un nouveau groupe

Pour commencer, nous allons créer un nouveau groupe et nous y ajouter.
1. Ouvrez un terminal.
2. Entrez la commande suivante : `sudo groupadd nintendo_switch`.
3. Entrez votre mot de passe lorsque vous y êtes invité.
4. Entrez la commande suivante : `sudo usermod -a -G nintendo_switch $USER`. Assurez-vous que le `G` est en capitale !
5. Fermer le terminal.

### Ajout d’une règle udev

Ensuite, nous allons ajouter une nouvelle règle udev. udev est un gestionnaire d’appareil pour le noyau linux. La règle que nous allons spécifier est que, si la switch est connectée en RCM, le groupe auquel appartient la Switch sera le groupe que nous avons créé dans la section précédente.

1. Ouvrez un terminal.
2. Passer en mode super-utilisateur avec la commande suivante : `sudo su`. Entrez votre mot de passe lorsque vous y êtes invité.
3. Entrez la commande suivante : `mkdir -p /etc/udev/rules.d`.
4. Entrez la commande suivante : `echo 'SUBSYSTEMS=="usb", ATTRS{manufacturer}=="NVIDIA Corp.", ATTRS{product}=="APX", GROUP="nintendo_switch"' > /etc/udev/rules.d/10-switch.rules`.
5. Entrez la commande suivante : `udevadm control --reload`.
6. Entrez la commande suivante : `udevadm trigger`.
7. Déconnectez-vous et reconnectez-vous.

Vous devriez maintenant être en mesure de lancer un payload sans avoir besoin d'utiliser `sudo`.

&nbsp;

## Option 2 : Installation d’un paquet avec les règles

!!! tip "Note:"
    Ces règles permettront à **N'IMPORTE QUEL UTILISATEUR** d’accéder à votre Switch via USB, pas seulement **votre** utilisateur.

Vous pouvez simplement suivre les instructions sur <a href="https://github.com/pheki/nx-udev" target="_blank">nx-udev</a>, ou si vous êtes sur Ubuntu/Debian :

1. Téléchargez <a href="https://github.com/pheki/nx-udev/releases/latest/download/nx-udev_latest_all.deb
" target="_blank">nx-udev_latest_all.deb</a>.
2. Ouvrez un terminal dans le même emplacement que votre téléchargement.
3. Lancez la commande `sudo dpkg -i nx-udev_latest_all.deb` pour installer le packet.

Vous devriez maintenant être en mesure de lancer un payload sans avoir besoin d'utiliser `sudo`.
