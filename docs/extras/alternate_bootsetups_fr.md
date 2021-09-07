# Modes de boot alternatifs

Si vous avez besoin de dépanner quelque chose, ou si vous voulez essayer une configuration de démarrage différente, lisez ce qui suit.

!!! danger "Ai-je besoin de cela ?"
	À moins de rencontrer des problèmes avec le démarrage de la console ou Atmosphère lui-même, il est fortement recommandé d’utiliser le guide principal au lieu de celui-ci. Ces guides sont fournis pour des raisons d’exhaustivité.

&nbsp;

### Chainload Fusee depuis Hekate


!!! tip "Ce dont vous aurez besoin"
    - La dernière version [d'Hekate](https://github.com/CTCaer/hekate/releases/)
    - La dernière version [d'Atmosphere](https://github.com/Atmosphere-NX/Atmosphere/releases) 
        - Vous devez télécharger le dossier compressé zip et le payload  `fusee.bin`
    - <a href="../../files/extras/hekate_ipl.ini" download>hekate_ipl.ini</a>


### Instructions

!!! tip ""
    1. Insérez votre carte SD dans votre PC
    2. Copiez *le contenu* de l'archive Atmosphère `.zip` à la racine de votre carte SD
    3. Copiez le fichier `fusee.bin` dans le dossier `atmosphere` de votre carte SD
    4. copiez le dossier `bootloader` de l'archive Hekate `.zip` à la racine de votre carte SD
    5. Copiez le fichier `hekate_ipl.ini` dans le dossier `bootloader` de votre carte SD
    6. La préparation est terminée, vous pouvez maintenant démarrer sous un CFW en injectant le payload hekate_ctcaer `.bin` de l'archive Hekate


&nbsp;

### Fusee sans Hekate


!!! tip "Ce dont vous aurez besoin"
    - La dernière version d'[Atmosphere](https://github.com/Atmosphere-NX/Atmosphere/releases) 
        - Vous devez télécharger le dossier compressé zip et le payload  `fusee.bin`
    
### Instructions

!!! tip ""
    1. Insérez votre carte SD dans votre PC
    2. Copiez *le contenu* de l'archive Atmosphère `.zip` à la racine de votre carte SD
    3. La préparation est terminée, vous pouvez maintenant démarrer sous un CFW en injectant le payload `fusee.bin`
