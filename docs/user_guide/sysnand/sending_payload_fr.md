

# Envoyer un payload

!!! warning "Si vous avez été envoyé sur cette page directement"
    Soyez certain d'être [entré en RCM](entering_rcm_fr.md) et d'avoir téléchargé Hekate (si nécessaire, extraire le dossier zip compressé à la racine de votre carte SD) avant de continuer.

Maintenant que votre console est en RCM, nous devons lui envoyer un payload. La méthode diffère en fonction des logiciels que vous avez à disposition, mais le principe reste le même.

&nbsp;

## Windows

### Ce dont vous aurez besoin

!!! tip ""
    - La dernière version de <a href="https://github.com/eliboa/TegraRcmGUI/releases" target="_blank">TegraRcmGUI</a> (le MSI ou le zip)
    - La dernière version de <a href="https://github.com/CTCaer/hekate/releases/" target="_blank">Hekate</a> (le fichier hekate_ctcaer bin ou le dossier compressé hekate_ctcaer zip)
    - Un câble USB-A vers USB-C (ou un simple câble USB-C si votre ordinateur a un port USB-C)

### Instructions

!!! tip ""
    1. Lancez TegraRcmGUI.
    2. Allez dans l'onglet `Settings`, puis appuyez sur `Install Driver` et suivez les instructions à l'écran.
        - Si vous rencontrez des erreurs lors de l'installation du pilote (driver), suivez la section [d'installation du pilote avec Zadig](#installation-du-pilote-avec-zadig) plus bas.
    3. Connectez votre Swith en RCM à votre PC avec le câble USB.
    4. Allez dans l'onglet `Payload` de TegraRcmGUI.
        - Votre Switch devrait être détectée sur l'icône en bas à droite de l'application.
    5. Appuyer sur le dossier à côté du bouton `Inject payload`, naviguez sur votr PC et sélectionnez votre payload (le fichier hekate_ctcare `.bin`).
    6. Cliquez sur `Inject payload` pour lancer Hekate.

### Installation du pilote avec Zadig

!!! tip ""
    Suivez cette procédure si vous avez des difficultés à installer le pilote avec TegraRcmGUI. Vous aurez besoin de la dernière version de <a href="https://zadig.akeo.ie" target="_blank">Zadig</a>.

    1. Lancez Zadig. Dans le menu `Options`, vérifiez que l'option `List All Devices` est activée.
    2. Connectez votre Swith en RCM à votre PC avec le câble USB.
    3. Dans Zadig, sélectionnez "APX" dans la liste des appareils (devices).
    4. Sélectionnez `libusbK (v3.1.0.0)` dans la liste des pilotes (drivers).
    5. Ciquez sur `Install Driver` pour lancer l'installation du pilote.

&nbsp;

## Mac / Linux

### Ce dont vous aurez besoin

!!! tip ""
    - La dernière version de <a href="https://github.com/nh-server/fusee-interfacee-tk/releases" target="_blank">fusee-interfacee-tk</a>
    - La dernière version de <a href="https://github.com/CTCaer/hekate/releases/" target="_blank">Hekate</a> (le fichier hekate_ctcaer bin ou le dossier compressé hekate_ctcaer zip)
    - Un câble USB-A vers USB-C (ou un simple câble USB-C si votre ordinateur a un port USB-C)

### Instructions

!!! tip ""
    1. Téléchargez et lancez le logiciel fusee-interfacee-tk (Si vous êtes sous Linux, vous devrez lancer le programme en tant que super-utilisateur, utilisez la commande `sudo`, ou suivez les instructions de la page [Injection Linux sans root](../../extras/adding_udev_fr.md)).
    2. Connectez votre Swith en RCM à votre PC avec le câble USB.
    3. Attendez que votre Switch soit reconnue dans l'application.
    4. Appuyez sur `Select Payload`, naviguez sur votr PC et sélectionnez votre payload (fichier `.bin`).
    5. Cliquez sur `Send Payload!`pour lancer le payload sélectionné.

&nbsp;

## Android

### Ce dont vous aurez besoin

!!! tip ""
    - La dernière version de <a href="https://github.com/MenosGrante/Rekado/releases" target="_blank">Rekado</a>
        - Vous devrez activer le lancement d'applications de sources inconnues dans les paramètres de votre appareil pour pouvoir l'utiliser
    - La dernière version de <a href="https://github.com/CTCaer/hekate/releases/" target="_blank">Hekate</a> (le fichier hekate_ctcaer bin ou le dossier compressé hekate_ctcaer zip)
    - Un câble USB-C
        - Si votre appareil a un port USB-C, vous pouvez utiliser un câble C-C
        - Si votre appareil n’a qu’un port micro USB, vous aurez besoin d’un adaptateur USB OTG et d’un câble USB A-C
            - Cela **ne fonctionnera pas** sur tous les téléphones !
		
### Instructions

!!! tip ""
    1. Copiez le fichier hekate_ctcaer `.bin` de l'archive Hekate `.zip` sur votre téléphone.
        - Une application comme Amaze File Manager peut le faire.
    2. Lancez Rekado sur votre téléphone.
    3. Allez à `Payloads`, appuyez sur le bouton `+` en bas à droite.
    4. Sélectionnez hekate_ctcaer `.bin` (à l'emplacement où vous l'avez enregistré) pour l'ajouter au menu de Rekado.
    5. **Optionnel, mais recommandé**: Allez dans les paramètres de Rekado et activez `Hide bundled`.
    6. Connectez votre Switch en RCM à votre téléphone à l’aide du câble USB.
    7. S'il vous le demande, autorisez Rekado à accéder à la Switch.
    8. Sélectionnez votre payload `.bin` dans la fenêtre de dialogue qui s'affiche.

&nbsp;

## Chromebook

### Ce dont vous aurez besoin

!!! tip ""
    - Un câble USB-C
    - Si votre chromebook a un port USB-C, notez que cela ne fonctionnera pas à l’aide d’un câble C-C
    - La dernière version de <a href="https://github.com/CTCaer/hekate/releases/" target="_blank">Hekate</a> (le fichier hekate_ctcaer bin ou le dossier compressé hekate_ctcaer zip)

### Instructions
    
!!! tip ""
    1. Allez sur ce [site web](https://switchgui.de/web-payload/) et descendez jusqu'en bas de la page.
    2. Sélectionnez l'option "Upload Payload" et téléversez le fichier hekate_ctcaer `.bin` de l'archive Hekate `.zip`.
    3. Connectez votre Switch en RCM à votre Chromebook à l’aide du câble USB.
    4. Sélectionnez "Do the thing". Une fenêtre va apparaître. Cliquez sur l'option `APX`.
    5. Appuyez sur le bouton Connect afin d'injecter le payload.
    
&nbsp;

!!! danger "Si rien ne se passe après l'injection du payload"
    Si l’écran de votre console reste noir après avoir envoyé Hekate, il est possible que votre payload ait été corrompu ou que votre console soit patchée. Si votre application d’injecteur de payload montre que 0 octets ont été envoyés, alors votre console certainement patché. Vous serez donc dans l'incapacité de continuer avec le reste du guide.

&nbsp;

#### [Continuer sur la création des sauvegardes essentielles (backup) <i class="fa fa-arrow-circle-right fa-lg"></i>](making_essential_backups_fr.md)
