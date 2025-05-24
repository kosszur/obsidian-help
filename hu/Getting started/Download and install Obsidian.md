---
permalink: install
---
Az Obsidian elérhető minden jelentős asztali és mobil platformon. Az alábbiakban felsoroljuk az Obsidian letöltésének és telepítésének támogatott módjait.

## Obsidian telepítése Windowsra

1. Nyisd meg a böngészőt, és látogasd meg a [Download Obsidian](https://obsidian.md/download) weboldalt.
2. A **Windows** szekció alatt kattints a **Universal** lehetőségre a telepítő fájl letöltéséhez.
3. Nyisd meg a telepítő fájlt, és kövesd az utasításokat.
4. Indítsd el az Obsidian-t ugyanúgy, mint bármelyik másik alkalmazást.

## Obsidian telepítése macOS-re

1. Nyisd meg a böngészőt, és látogasd meg a [Download Obsidian](https://obsidian.md/download) weboldalt.
2. A **macOS** szekció alatt kattints a **Universal** lehetőségre a telepítő fájl letöltéséhez.
3. Nyisd meg a telepítő fájlt.
4. A megnyíló ablakban húzd az Obsidian alkalmazást az Applications mappába.
5. Indítsd el az Obsidian-t ugyanúgy, mint bármelyik másik alkalmazást.

## Obsidian telepítése Linuxra

Ha Linuxot használsz, többféleképpen is telepítheted az Obsidian-t. Kövesd a csomagkezelődnek megfelelő utasításokat.

### Obsidian telepítése Snap segítségével

1. Nyisd meg a böngészőt, és látogasd meg a [Download Obsidian](https://obsidian.md/download) weboldalt.
2. A **Linux** szekció alatt kattints a **Snap** lehetőségre a telepítő fájl letöltéséhez.
3. Nyiss meg egy terminált, és navigálj a letöltött telepítő fájl mappájába.
4. A terminálban futtasd az alábbi parancsot a Snap csomag telepítéséhez: (A `--dangerous` kapcsoló szükséges, mert a Snapet létrehozó Canonical nem vizsgálta át a csomagot. A `--classic` kapcsoló lehetővé teszi az Obsidian számára, hogy hozzáférjen a tárolódhoz a sandboxon kívül.)

   ```bash
   snap install obsidian_<version>_<arch>.snap --dangerous --classic
   ```
   
5. Indítsd el az Obsidian-t ugyanúgy, mint bármelyik másik alkalmazást.

### Obsidian telepítése AppImage segítségével

1. Nyisd meg a böngészőt, és látogasd meg a [Download Obsidian](https://obsidian.md/download) weboldalt.
2. A **Linux** szekció alatt kattints az **AppImage** lehetőségre a telepítő fájl letöltéséhez.
3. Nyiss meg egy terminált, és navigálj a letöltött telepítő fájl mappájába.
4. A terminálban futtasd az alábbi parancsot az Obsidian megnyitásához:

   ```bash
   chmod u+x Obsidian-<version>.AppImage
   ./Obsidian-<version>.AppImage
   ```

Megjegyzés: Chromebookokon a `libnss3-dev` csomagot telepíteni kell, különben a következő hibaüzenetet kaphatod: `error while loading shared libraries: libnss3.so: cannot open shared object file: No such file or directory`.

### Obsidian telepítése Flatpak segítségével

1. A terminálban futtasd az alábbi parancsot az Obsidian telepítéséhez:

   ```bash
   flatpak install flathub md.obsidian.Obsidian
   ```

2. Az Obsidian megnyitásához futtasd az alábbi parancsot:

   ```bash
   flatpak run md.obsidian.Obsidian
   ```

## Obsidian telepítése Androidra

1. Keresd meg az Obsidian alkalmazást a [Play Áruházban](https://play.google.com/store/apps/details?id=md.obsidian).
2. Koppints a **Telepítés** gombra az alkalmazás letöltéséhez.
3. Indítsd el az Obsidian-t ugyanúgy, mint bármelyik másik alkalmazást.

Az Androidos APK fájlt opcionálisan letöltheted a [Download Obsidian](https://obsidian.md/download) oldalról.

## Obsidian telepítése iPhone-ra és iPadre

1. Keresd meg az Obsidian alkalmazást az [App Store-ban](https://apps.apple.com/us/app/obsidian-connected-notes/id1557175442).
2. Koppints a **Letöltés** gombra az alkalmazás telepítéséhez.
3. Indítsd el az Obsidian-t ugyanúgy, mint bármelyik másik alkalmazást.

