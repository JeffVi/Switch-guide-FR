# Préparation de la carte SD

Nous allons maintenant placer les fichiers requis pour le CFW Atmosphère et quelques fichiers homebrew supplémentaires sur la carte SD.

Atmosphère possède son propre bootloader (payload), appelé fusée. Pour les besoins de ce guide, nous utiliserons Hekate à la place, afin que nous puissions récupérer la NAND (stockage interne) du système et profiter d’autres fonctionnalités avancées à l’avenir.

&nbsp;

!!! warning "Extensions de noms de fichiers"
    Si vous utilisez Windows, vous devriez activer l'affichage des extensions de noms de fichiers avant de continuer. Cf. [ce guide](../../extras/showing_file_extensions_fr.md).

&nbsp;

### Ce dont vous avez besoin

!!! tip ""
    - La dernière version de <a href="https://github.com/CTCaer/Hekate/releases/" target="_blank">Hekate</a> (Téléchargez `hekate_ctcaer_(version)_Nyx_(version).zip` dans les assets)
    - Le fichier de configuration Hekate : <a href="../../../files/emu/hekate_ipl.ini" download>hekate_ipl.ini</a>
    - La configuration de redirection DNS (90dns) : <a href="../../../files/emummc.txt" download>emummc.txt</a>
    - Le dossier bootlogo.zip : <a href="../../../files/bootlogos.zip" download>bootlogos.zip</a>
    - La dernière version de <a href="https://github.com/Atmosphere-NX/Atmosphere/releases" target="_blank">Atmosphère</a> (Téléchargez `atmosphere-(version)-master-(version)+hbl-(version)+hbmenu-(version).zip` dans les assets).
    - La dernière version de <a href="https://github.com/shchmue/Lockpick_RCM/releases" target="_blank">Lockpick_RCM</a> (Téléchargez `Lockpick_RCM.bin` dans les assets)
    - La dernière version de <a href="https://github.com/J-D-K/JKSV/releases" target="_blank">JKSV</a> (Téléchargez `JKSV.nro` dans les assets)
    - La dernière version de <a href="https://github.com/mtheall/ftpd/releases" target="_blank">FTPD</a> (Téléchargez `ftpd.nro` dans les assets)
    - La dernière version de <a href="https://github.com/exelix11/SwitchThemeInjector/releases" target="_blank">NXThemeInstaller</a> (Téléchargez `NxThemesInstaller.nro` dans les assets)
    - La dernière version de <a href="https://github.com/joel16/NX-Shell/releases" target="_blank">NX-Shell</a> (Téléchargez `NX-Shell.nro` dans les assets)
    - La dernière version de the <a href="https://github.com/vgmoose/hb-appstore/releases" target="_blank">hbappstore</a> (Téléchargez `appstore.nro` dans les assets)

### Instructions

!!! tip ""
    1. Insérez la carte SD de votre Switch dans votre PC.
    2. Copiez *le contenu* du fichier `.zip` Atmosphere à la racine de votre carte SD.
    3. Copiez le dossier `bootloader` du fichier `.zip` Hekate à la racine de votre carte SD.
    4. Copiez le dossier `bootloader` du fichier `bootlogos.zip` à la racine de votre carte SD.
         - Si on vous demande de fusionner les dossiers, faites le.
    5. Copiez le fichier `hekate_ipl.ini` dans le dossier `bootloader` sur votre carte SD.
    6. Copiez le fichier `Lockpick_RCM.bin` dans le dossier `/bootloader/payloads` sur votre carte SD.
    7. Créez un dossier `hosts` dans le dossier `atmosphere` sur votre carte SD, et mettez le fichier `emummc.txt` à l'intérieur.
    8. Créez un dossier `appstore` dans le dossier `switch` sur votre carte SD, et mettez le fichier `appstore.nro` à l'intérieur.
    9. Copiez les fichiers `JKSV.nro`, `ftpd.nro`, `NX-Shell.nro` et `NxThemesInstaller.nro` dans le dossier `switch` sur votre carte SD.
    10. Si vous utilisiez déjà votre carte microSD comme périphérique de stockage pour vos jeux et que vous avez conservé votre dossier `Nintendo` avant de partitionner votre carte microSD, replacez le à la racine de votre carte microSD.
    11. Réinsérez votre carte SD dans votre Switch.

    !!!danger "À propos du fichier emummc.txt"
        Placer le fichier `emummc.txt` de ce guide dans `/atmosphere/hosts` empêchera votre emuMMC (emuNAND) de se connecter à Nintendo. Ne pas le faire entraînera probablement un banissement de la console.

    !!! tip ""
        Votre carte SD devrait ressembler à ceci. Le dossier `Nintendo` n'est pas présent si vous n'avez jamais utilisé votre carte SD avec votre Switch.
        ![sdfilesimg](../img/sdfiles.png)

&nbsp;

#### [Continuer avec la création de l'EmuMMC <i class="fa fa-arrow-circle-right fa-lg"></i>](making_emummc_fr.md)
