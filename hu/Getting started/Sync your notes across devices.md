---
aliases:
  - Jegyzetek szinkronizálása eszközök között
  - getting-started/sync-your-notes-across-devices
cssclasses:
  - soft-embed
description: Hogyan szinkronizálhatod az Obsidian jegyzeteidet eszközök és platformok között.
mobile: true
permalink: sync-notes
publish: true
---
Az Obsidian jegyzeteket helyileg tárolja az eszközödön, így mindig hozzáférhetsz hozzájuk, még offline is. Ha több eszközön szeretnéd elérni a jegyzeteidet, be kell állítanod egy szinkronizálási módszert.

Ez az útmutató a leggyakoribb szinkronizálási módszereket ismerteti, beleértve a tippeket az adatvesztés elkerülésére és a zökkenőmentes élmény biztosítására.

Ajánljuk, hogy olvasd el a [[Back up your Obsidian files|biztonsági mentési útmutatónkat]] is, hogy megóvd az adataidat.

## Szinkronizálási módszerek

Az Obsidian jegyzeteid egyszerű fájlokként vannak tárolva egy [[Local and remote vaults|tároló]] nevű mappában. Ez azt jelenti, hogy számos módja van az adataid szinkronizálásának.

Az alábbiakban néhány gyakran használt szinkronizálási módszert sorolunk fel, amelyeket az [Obsidian közösség](https://obsidian.md/community) tagjai ajánlottak:

1. **Elsődleges szinkronizálás**: [[#Obsidian Sync]]
2. **Harmadik fél által kínált felhőalapú szinkronizálás**: [[#iCloud]], [[#OneDrive]], és [[#Google Drive]]
3. **Helyi szinkronizálás**: [[#Syncthing]]
4. **Verziókezelés**: [[#Git]] és [[#Working Copy]]

## Obsidian Sync

**Ajánlott rendszerek**: `Windows`, `macOS`, `Linux`, `iOS`, `Android`

A legegyszerűbb és hivatalosan támogatott szinkronizálási módszer az Obsidian saját megoldása: [[Introduction to Obsidian Sync|Obsidian Sync]].

Az Obsidian Sync végponttól végpontig titkosított a maximális adatvédelem érdekében, és zökkenőmentesen integrálódik az Obsidian alkalmazásba.

Kövesd a [[Set up Obsidian Sync|beállítási útmutatót]] az Obsidian Sync konfigurálásához.

> [!Important] Kerüld az Obsidian Sync egyidejű használatát más felhőalapú szolgáltatásokkal, például Dropbox vagy OneDrive **ugyanazon tároló esetén**, mivel ez adatütközéseket és fájlmeghibásodást okozhat.

## iCloud

**Ajánlott rendszerek**: `macOS`, `iOS`, `iPadOS`

Az iCloud használható a tárolók szinkronizálására iOS és macOS között. Azonban az **iCloud Drive Windows-on** fájlduplikációt vagy sérülést okozhat.

**Tároló létrehozása és tárolása iCloud Drive-ban**:

- **iCloud Drive engedélyezése**:
    - macOS-en: Lépj a **Rendszerbeállítások → Apple ID → iCloud → iCloud Drive** menübe.
    - iOS-en: Lépj a **Beállítások → [Neved] → iCloud → iCloud Drive** menübe.
- **Új tároló létrehozása az iCloudban**:
    - macOS-en:
        1. Nyisd meg az **Obsidian** alkalmazást, és válaszd a **Új tároló létrehozása** lehetőséget.
        2. A fájlválasztóban navigálj az **iCloud Drive → Obsidian** mappába.
        3. Hozz létre egy mappát a tárolód számára, és nevezd el.
        4. Kattints a **Létrehozás** gombra a befejezéshez.
    - iOS-en:
        1. Nyisd meg az **Obsidian** alkalmazást, és koppints a **Új tároló létrehozása** opcióra.
        2. Adj nevet a tárolódnak.
        3. Kapcsold be a **Tárolás iCloudban** lehetőséget.
        4. Koppints a **Létrehozás** gombra.
- **A tároló megnyitása egy másik Apple eszközön**:  
    - Egy másik macOS vagy iOS eszközön nyisd meg az **Obsidian** alkalmazást, lépj a [[Manage vaults|Tárolóváltó]] menübe, és válaszd a **Mappa megnyitása tárolóként** lehetőséget. Navigálj az **iCloud Drive → Obsidian** mappába.

> [!Tip] Legjobb gyakorlatok  
> - **macOS 14 (Sonoma) és korábbi verziók esetén**: Tiltsd le az **Optimalizált Mac Tárolás** funkciót az iCloud beállításokban, hogy megelőzd a fájlok eltávolítását. Ez a beállítás minden iCloud-tárolásra hatással van az eszközön, nem csak az Obsidianra.  
> - **macOS 15 (Sequoia) esetén**: Kattints jobb gombbal az **Obsidian** mappára az iCloud Drive-ban, majd válaszd a **Letöltöttként tartás** lehetőséget.

## OneDrive

**Ajánlott rendszerek**: `Windows`, `macOS` (korlátozott funkcionalitás Androidon)

[OneDrive](https://support.microsoft.com/en-us/office/Sync-with-OneDrive-bb89981b-e382-4969-b8fd-d413a90b6db3#ID0EAABAAA=Set_up) népszerű felhőalapú tárolási lehetőség Windows és macOS felhasználók számára. Azonban Androidon korlátozott működéssel rendelkezik, és hivatalosan nem támogatja az Obsidian tárolók szinkronizálását iOS-en.

> [!Important] Mielőtt OneDrive-ot használnád szinkronizálásra, győződj meg róla, hogy a tároló mappa be van állítva **Mindig tartsa ezen az eszközön** módra. Ez megakadályozza, hogy a OneDrive eltávolítsa a fájlokat, és így az Obsidian ne tekintse őket hiányzónak.

**Tároló létrehozása és tárolása OneDrive-ban**:

1. **OneDrive beállítása**:
   - Windows esetén: Jelentkezz be a OneDrive alkalmazáson keresztül vagy a Microsoft fiókod segítségével.
   - macOS esetén: Töltsd le a OneDrive alkalmazást, és jelentkezz be.
2. **Új tároló létrehozása OneDrive-ban**:
   - Windows/macOS:
     1. Nyisd meg a **File Explorer** (Windows) vagy a **Finder** (macOS) alkalmazást, és navigálj a **OneDrive → Documents** mappába.
     2. Hozz létre egy új mappát (például "Obsidian Vault").
     3. Nyisd meg az **Obsidian** alkalmazást, kattints a **Új tároló létrehozása** lehetőségre, és válaszd ki a OneDrive mappát.
3. **A tároló megnyitása egy másik eszközön**:
   - Egy másik eszközön nyisd meg az **Obsidian** alkalmazást, lépj a [[Manage vaults|Tárolóváltó]] menübe, és válaszd a **Mappa megnyitása tárolóként** lehetőséget. Navigálj a **OneDrive → Documents** mappába.

> [!Note] A OneDrive nem feltétlenül működik megfelelően Androidon. Fontold meg olyan alkalmazások használatát, mint a [Dropsync](https://play.google.com/store/apps/details?id=com.ttxapps.dropsync) vagy a [FolderSync](https://play.google.com/store/apps/details?id=dk.tacit.android.foldersync.lite).

> [!Tip] Legjobb gyakorlatok:
> - Mindig tartsd a tároló fájljaidat **Offline elérhetőként**, kattints jobb gombbal a mappára, majd válaszd a **Mindig tartsa ezen az eszközön** lehetőséget.
> - Kerüld a OneDrive **Files On-Demand** funkcióját a tárolók esetében, hogy elkerüld a szinkronizálási problémákat.

## Google Drive

**Ajánlott rendszerek**: `Windows`, `macOS`, `Android` (korlátozott funkcionalitás iOS-en)

[Google Drive](https://support.google.com/drive/answer/10838124?hl=en) egy másik népszerű felhőalapú tárolási megoldás. Bár hivatalosan nem támogatja az Obsidian tárolók szinkronizálását, harmadik féltől származó alkalmazások és bővítmények segítségével szinkronizálható több eszköz között.

> [!Important] A Google Drive nem hivatalosan támogatott Obsidian tárolók szinkronizálására iOS-en. Fontold meg egy harmadik fél megoldását vagy bővítmény használatát iOS-en történő szinkronizáláshoz.

**Tároló létrehozása és tárolása Google Drive-ban**:

1. **Google Drive beállítása**:
    - Windows vagy macOS esetén: Töltsd le a Google Drive alkalmazást, és jelentkezz be.
    - Android esetén: Győződj meg róla, hogy a Google Drive engedélyezve van és bejelentkeztél.
2. **Új tároló létrehozása Google Drive-ban**:
    - Windows/macOS:
        1. Nyisd meg a **File Explorer** (Windows) vagy **Finder** (macOS) alkalmazást, és navigálj a **Google Drive** mappába.
        2. Hozz létre egy új mappát (például "Obsidian Tároló").
        3. Nyisd meg az **Obsidian** alkalmazást, kattints a **Új tároló létrehozása** gombra, és válaszd ki a Google Drive mappát.
3. **A tároló megnyitása egy másik eszközön**:
    - Egy másik eszközön nyisd meg az **Obsidian** alkalmazást, lépj a [[Manage vaults|Tárolóváltó]] menübe, és válaszd a **Mappa megnyitása tárolóként** lehetőséget. Navigálj a Google Drive mappádba.

> [!Tip] Legjobb gyakorlatok:
> - Állítsd be a tároló fájlokat **Offline elérhetőként** a Google Drive-ban, hogy elkerüld az adatátviteli problémákat.
> - iOS esetén fontold meg alternatív módszereket, például [[Introduction to Obsidian Sync|Obsidian Sync]], [[#iCloud]], vagy használd a **Remotely Save** bővítményt.

## Syncthing

**Ajánlott rendszerek**: `Windows`, `macOS`, `Linux`, `Android`

A Syncthing egy decentralizált fájlszinkronizáló eszköz, amely nem támaszkodik felhőalapú tárolásra. Közvetlenül szinkronizálja a tárolódat az eszközök között hálózaton vagy az interneten keresztül.

**Tároló létrehozása és tárolása a Syncthing segítségével**:

1. **Syncthing beállítása**:
   - Telepítsd a Syncthinget minden eszközre. A telepítési útmutatókat megtalálod a [Syncthing weboldalon](https://syncthing.net/).
2. **Megosztott mappa létrehozása és konfigurálása**:
   - Minden eszközön:
     1. Nyisd meg a Syncthinget, és hozz létre egy megosztott mappát. Állítsd be a mappa elérési útját az Obsidian tárolódnak megfelelően.
     2. Győződj meg róla, hogy minden eszközön ugyanazt a mappát választottad ki.
     3. Konfiguráld a mappa szinkronizálási beállításait (például **Küldés és Fogadás** a kétirányú szinkronizáláshoz).
3. **A tároló megnyitása az Obsidianban**:
   - Miután a mappa szinkronizálódott az eszközök között, nyisd meg az **Obsidian** alkalmazást, lépj a [[Manage vaults|Tárolóváltó]] menübe, és válaszd a **Mappa megnyitása tárolóként** lehetőséget.

> [!Note] A Syncthing akkor működik a legjobban, ha legalább egy eszköz folyamatosan be van kapcsolva a folyamatos szinkronizálás biztosítása érdekében.

> [!Tip] Legjobb gyakorlatok:
> - Helyi szinkronizálás esetén győződj meg róla, hogy minden eszköz ugyanahhoz a hálózathoz csatlakozik.
> - Zárd ki az `.obsidian` mappát a szinkronizálásból, ha külön beállításokat szeretnél az egyes eszközökön.
> - Használj kizárási mintákat, hogy elkerüld az ideiglenes vagy biztonsági mentési fájlok szinkronizálását.

## Git

**Ajánlott rendszerek**: `Windows`, `macOS`, `Linux`

A **Git** egy verziókezelő rendszer, amely lehetővé teszi a változások nyomon követését, másokkal való együttműködést és a tárolók szinkronizálását olyan szolgáltatásokon keresztül, mint a GitHub, GitLab vagy egy saját üzemeltetésű szerver.

**Tároló szinkronizálása Git segítségével**:

1. **Távoli tárhely beállítása**:
    - Hozz létre egy tárolót egy Git tárhelyszolgáltatáson (például GitHub, GitLab vagy egy saját szerveren).
2. **Tároló szinkronizálása**:
    1. Nyiss meg egy terminált vagy Git GUI-t (például GitKraken, Sourcetree).
    2. Inicializálj egy Git tárolót a tárolód mappájában a `git init` paranccsal.
    3. Add hozzá a távoli tárhelyet: `git remote add origin [URL]`.
    4. Mentsd el a változásokat: `git add .` és `git commit -m "Üzeneted"`.
    5. Küldd fel a változásokat: `git push origin main`.
3. **Változások lehívása más eszközökön**:
    - Klónozd a tárolót egy másik eszközön, és hívd le a változásokat a `git pull origin main` paranccsal.

> [!Note] A Git erős verziókezelési lehetőséget biztosít, de a szinkronizálás nem automatikus. A változásokat manuálisan kell feltölteni és lehívni.

## iPhone és iPad szinkronizálás

**Ajánlott lehetőségek**:
- [[Introduction to Obsidian Sync|Obsidian Sync]]
- [[#iCloud]]

> [!Important] Kerüld ugyanazon tároló szinkronizálását több szolgáltatás között (például az Obsidian Sync és az iCloud egyidejű használatát), mivel ez adatütközésekhez és fájlkárosodáshoz vezethet.

**Nem támogatott lehetőségek**:
Az alábbi szolgáltatások hivatalosan nem támogatottak iOS-en, de egyes felhasználók találtak megoldásokat harmadik fél eszközök vagy bővítmények használatával:

- Dropbox
- Google Drive
- OneDrive
- Syncthing

Néhány felhasználó sikeresen használta olyan bővítményeket, mint a **Remotely Save** vagy **LiveSync**, hogy szinkronizálja tárolóit iOS-en. Azonban ezek a módszerek nem hivatalosan támogatottak, és az eredmények eltérőek lehetnek.

### Working Copy

**Ajánlott rendszerek**: `iOS`  
**Szükséges**: [[#Git]]

A **Working Copy** egy Git kliens iOS-re, amely lehetővé teszi tárolók klónozását, módosítások mentését és feltöltését egy Git tárolóba. Jól működik az Obsidian tárolók szinkronizálására Git segítségével, bár egyes funkciókhoz alkalmazáson belüli vásárlás szükséges.

**Tároló szinkronizálása Working Copy segítségével**:

1. **Working Copy telepítése**:
    - Töltsd le a **[Working Copy](https://apps.apple.com/us/app/working-copy-git-client/id896694807)** alkalmazást iPhone-ra vagy iPadre.
2. **Git tároló klónozása**:
    - Nyisd meg a Working Copy alkalmazást, koppints az **Add Repository** opcióra, és add meg a tároló URL-jét (pl. GitHub, GitLab).
3. **Tároló összekapcsolása Obsidian-nal**:
    - Kapcsold össze a klónozott tároló mappáját egy üres tárolóval az **Obsidian** alkalmazásban.
4. **Változások mentése és feltöltése**:
    - Az Obsidianban végzett szerkesztések után használd a Working Copy alkalmazást a **Commit** és **Push** műveletekhez, hogy mentett változásokat feltöltsd a távoli tárolóba.
    - Más eszközökön húzd le a változásokat Git segítségével a tároló szinkronizálásához.

> [!Note] Bár a Working Copy nem hivatalosan támogatott, sok felhasználó sikeresen használja az Obsidian tárolók Git alapú szinkronizálására.



## Összehasonlítás

Minden szinkronizálási módszernek megvannak a maga előnyei és hátrányai, beleértve a költségeket, adatvédelmet és funkciókat.

|                                                  | Végponttól végpontig<br>titkosítás | Verzió<br>előzmények |
| ------------------------------------------------ | ---------------------------------- | ------------------- |
| [[Introduction to Obsidian Sync|Obsidian Sync]]  | ✅                                  | ✅                   |
| iCloud                                           | Opcionális                        | ❌                   |
| OneDrive                                         | ❌                                  | ❌                   |
| Google Drive                                     | ❌                                  | ❌                   |
| Syncthing                                        | Opcionális                        | ✅                   |
| Git                                              | ❌                                  | ✅                   |

## Gyakran ismételt kérdések

**Miért nem támogatja hivatalosan az Obsidian az én szinkronizálási szolgáltatásomat?**

Egyes jegyzetelő alkalmazások egyszerre csak egy fájlhoz férnek hozzá, míg az Obsidian teljes tárolóra való hozzáférést igényel funkcióihoz (pl. hivatkozások frissítése fájl átnevezésekor). Ez nehézségeket okozhat egyes szolgáltatások számára az Obsidian megbízható működéséhez.

**Miért kell a fájlokat „Offline elérhető” állapotban tartanom?**

Ha a OneDrive vagy az iCloud eltávolítja a fájlokat (pl. **Files On-Demand** vagy **Optimalizált Mac Tárolás** funkcióval), az Obsidian nem tudja elérni őket, ami szinkronizálási problémákat okozhat. Állítsd be a tároló mappáját **Mindig tartsa ezen az eszközön** (OneDrive) vagy győződj meg róla, hogy az **Letöltöttként tartás** engedélyezve van (iCloud).

**Hogyan kezelhetem a különböző konfigurációkat a tárolóim számára?**

Az Obsidian lehetővé teszi, hogy egyedi konfigurációs mappát állíts be eszközönként a [[Configuration folder|Konfigurációs mappák]] funkcióval.

