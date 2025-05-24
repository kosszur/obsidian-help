---
aliases:
  - Obsidian Sync/Obsidian Sync and third-party services
  - Obsidian Sync/Back up your vault
  - backup
permalink: backup
---
Ha még nem készítettél biztonsági mentést a számítógépedről, itt az ideje elkezdeni! Az Obsidian [[File recovery|Fájlhelyreállítás]] bővítménye hasznos eszköz, de csak a jegyzeteidet menti. A biztonság kedvéért a bővítmény által létrehozott pillanatképeket is érdemes menteni.

**Miért készíts biztonsági mentést az adataidról?**

Alapértelmezés szerint az Obsidian jegyzeteidet **helyileg** tárolja az eszközödön, nem a felhőben. Ez azt jelenti, hogy [az adatok teljes mértékben a tieid](https://obsidian.md/about), és te rendelkezel felettük. Azonban a helyi tárolás sérülhet vagy adatvesztés érheti. Nem az a kérdés, hogy előfordul-e, hanem az, hogy mikor. A biztonsági mentés védelmet nyújt ezek ellen az elkerülhetetlen események ellen, és biztosítja, hogy mindig hozzáférj a jegyzeteidhez.

## A szinkronizálás nem egyenlő a biztonsági mentéssel

Az olyan szolgáltatások, mint [[Introduction to Obsidian Sync|Bevezetés az Obsidian Sync-be]], iCloud, OneDrive és Dropbox segítenek szinkronizálni a jegyzeteidet különböző eszközök között. Bár kínálhatnak olyan funkciókat, mint [[Version history|Verziótörténet]], **nem biztonsági mentésre lettek tervezve**. A szinkronizálás frissíti a jegyzeteidet, de nem védi őket adatvesztés ellen.

- **Szinkronizálás:** A szinkronizálás biztosítja, hogy a fájljaid minden eszközön azonosak legyenek. Ha egy fájlt módosítasz egy eszközön, az frissül minden szinkronizált eszközön. A szinkronizáló szolgáltatásoknak nincs „elsődleges” eszközük.
- **Biztonsági mentés:** A biztonsági mentés egy példányt készít az adataidról egy külön helyen, hogy vissza lehessen állítani őket adatvesztés vagy sérülés esetén. A biztonsági mentések nem valós idejű frissítésekre vagy együttműködésre szolgálnak.

A tárolód megfelelő biztonsági mentéséhez használj dedikált biztonsági mentési eszközt, amely egyirányú másolatot készít az adataidról. Ez az eszköz biztonságos mentési helyre küldi az adataidat anélkül, hogy módosítaná azokat az eszközödön.

Ha több eszközön használod a szinkronizálást, válassz ki **egy eszközt**, amely a biztonsági mentési eszközöd lesz. Ez általában a fő vagy „elsődleges” eszközöd, amit a leggyakrabban használsz. Vegyük figyelembe, hogy a legtöbb szinkronizáló szolgáltatás nem ismer el egyetlen eszközt „elsődlegesnek”; ez csak egy fogalom, amely segít a biztonsági mentések kezelésében.

> [!Example] Ha Obsidian Sync-et használsz a laptopodon, táblagépeden, telefonodon és munkahelyi asztali gépeden, de leggyakrabban a munkahelyi gépen dolgozol, ritkábban a laptopodon, és csak alkalmanként a táblagépen vagy telefonon, akkor a munkahelyi asztali gép lenne az „elsődleges eszközöd” a biztonsági mentéshez.

## Közösségi bővítmények használata

Bár az Obsidian csapat hivatalosan nem ajánl egyetlen bővítményt sem, két közösségi bővítmény különösen népszerűvé vált a felhasználók körében a fájlok biztonsági mentésére:

- **[Obsidian Git](https://obsidian.md/plugins?id=obsidian-git):** Használd ezt a bővítményt a tárolód mentéséhez, amely a tartalmát egy [GitHub](https://github.com/) tárba küldi. Ez egy hatékony módja annak, hogy verziókezelést alkalmazz a jegyzeteidre, és biztosítsd azok biztonságát egy távoli szerveren. Azonban vedd figyelembe, hogy az adataidat a GitHub fogja tárolni [[#Felhő alapú szolgáltatások használata|ezzel a módszerrel]].
- **[Local Backup](https://obsidian.md/plugins?id=local-backup):** Ez a bővítmény lehetővé teszi, hogy helyi másolatokat készíts a tárolódról egy választott mappában, amely archiválási lehetőségeket is kínál. Akár egy szinkronizáló mappát, például egy Dropbox mappát is használhatsz, hogy kombináld a helyi és felhő alapú mentéseket. Ez a módszer **jól működik** az alábbi mentési opciókkal.

## Felhő alapú szolgáltatások használata

> [!info] Nem ajánlott, hogy a tárolód helyét közvetlenül a választott mentési szolgáltatásban tartsd.

A biztonsági mentés felhőben történő tárolása egy alternatív és kiegészítő módszer a fizikai adathordozókhoz képest, például külső merevlemezekhez vagy USB meghajtókhoz. Egy külső merevlemez vagy USB meghajtó elveszhet vagy megsérülhet. A legnagyobb előnye a felhőben tárolt fájloknak, hogy bármikor, bárhonnan elérhetők. Hátránya viszont, hogy a legtöbb mentési szolgáltatás egy magántársaság tulajdonában van.

Biztonsági szempontból mindig figyelj az adataid elérésére és védelmére a felhő alapú mentéseknél. [Worldbackupday](https://www.worldbackupday.com/en) naprakész listát vezet az online biztonsági mentési szolgáltatásokról, amelyeket érdemes figyelembe venni.

## Külső meghajtók használata

**Merevlemezek és SSD meghajtók**  A külső merevlemezes biztonsági mentések továbbra is értékesek a növekvő felhőalapú világban, és főként adattárolásra és számítógépes biztonsági mentésekre használatosak. A külső meghajtók legnagyobb hátránya, hogy meghibásodhatnak vagy elveszhetnek. A legnagyobb előnyük viszont, hogy a tárhelyet csak egyszer kell megvásárolni. A külső merevlemezek használata gyakran kombinálható egy [[#Use computer backups|számítógépes biztonsági mentéssel]].

**USB flash meghajtók**  Az USB-meghajtók (más néven pendrive-ok, memóriakártyák vagy kulcsmeghajtók) egyszerű és hatékony módszert kínálnak a gyors biztonsági mentésekhez.

1. Csatlakoztasd az USB-meghajtót a számítógépedhez vagy laptopodhoz.
2. Győződj meg róla, hogy az eszköz felismeri és csatlakoztatja a fájlrendszeredhez. Ha szükséges, formázd az USB-meghajtót úgy, hogy kompatibilis legyen a fájlrendszereddel.
3. Másold át a tárolód mappáját a jelenlegi helyéről az USB-meghajtóra.
4. Biztonságosan válaszd le az USB-meghajtót.
5. Távolítsd el az USB-meghajtót az eszközödről.

> [!tip] Ha az USB-meghajtód érzékeny adatokat tartalmaz, ajánlott biztonságos helyen tárolni, például egy zárt szobában.

## Számítógépes biztonsági mentés használata

Az operációs rendszered lehetőséget biztosít biztonsági mentések készítésére, akár a felhőben, akár egy külső meghajtón.

- **[Windows](https://www.microsoft.com/en-us/windows/learning-center/back-up-files):** Biztonsági mentés OneDrive-ra vagy egy külső meghajtóra. Használhatod a [Rendszer-visszaállítást](https://support.microsoft.com/en-us/windows/use-system-restore-a5ae3ed9-07c4-fd56-45ee-096777ecd14e) is.
- **[Mac](https://support.apple.com/en-us/104984):** Biztonsági mentés külső eszközre a Time Machine segítségével.
- **[Linux](https://linuxize.com/post/how-to-use-rsync-for-local-and-remote-data-transfer-and-synchronization/):** `rsync` használata egy kiválasztott könyvtárba vagy meghajtóra.

## További lépések

Ez a súgóoldal rövid áttekintést nyújt a biztonsági mentési lehetőségekről, de nem teljeskörű. Ha részletesebb információkat keresel, látogasd meg a [Worldbackupday.com](https://www.worldbackupday.com/en) weboldalt, vagy kérdezd meg más Obsidian felhasználókat a [közösségünkben](https://obsidian.md/community), hogyan kezelik a biztonsági mentéseket!

