---
permalink: symlinks
---
A tárolóban használhatsz [szimbolikus hivatkozásokat](https://en.wikipedia.org/wiki/Symbolic_link) (symlinks) és [csomópontokat](https://learn.microsoft.com/en-us/windows/win32/fileio/hard-links-and-junctions#junctions), hogy fájlokat tárolj a tárolón kívül, valamint a [[How Obsidian stores data#Global settings|rendszer mappában]].

> [!danger] Csak saját felelősségre  
> Határozottan **nem ajánljuk** a szimbolikus hivatkozások használatát. Ha a tárolódban szimbolikus hivatkozásokat vagy csomópontokat használsz, az adatvesztéshez vagy sérüléshez, illetve az Obsidian összeomlásához vezethet. Győződj meg róla, hogy rendszeresen biztonsági mentést készítesz a tárolódról és beállításaidról.

Az alábbiakban ismertetjük néhány korlátozást vagy problémát, amelyeket érdemes figyelembe venni:

- A hivatkozás hurkok nem engedélyezettek, hogy megakadályozzuk az Obsidian végtelen ciklusok miatti összeomlását.
- A szimbolikus hivatkozások céljainak teljesen el kell különülniük a tároló gyökérkönyvtárától vagy más hivatkozások célpontjaitól. Az **elkülönülés** azt jelenti, hogy egy mappa nem tartalmazhat egy másikat vagy fordítva. Az Obsidian figyelmen kívül hagy minden hivatkozást a tároló szülőmappájára, vagy egy mappából egy másik mappába ugyanazon tárolón belül. Ez biztosítja, hogy ne legyenek duplikált fájlok a tárolódban, amelyek miatt a hivatkozások nehezen kezelhetők lehetnek.
- A szimbolikus hivatkozások nem működnek megfelelően az Obsidian Sync vagy _bármilyen más szinkronizálási megoldással_. Ha egy szimbolikus hivatkozás célja egy másik Obsidian tárolóval szinkronizált mappa, akkor adatkonfliktusok vagy adatvesztés léphet fel. Egyes szinkronizáló eszközök, például a Git, nem követik a szimbolikus hivatkozásokat, hanem csak a **hivatkozás útvonalát** szinkronizálják, ami nem kívánt eredményekhez vezethet, ha így osztod meg a tárolódat másokkal.
- Az Obsidian fájlkezelője nem tud fájlokat mozgatni eltérő meghajtók között, ezért ha egy másik meghajtón lévő mappára mutató hivatkozást használsz, nem tudsz fájlokat áthúzni abba vagy más mappákba az Obsidian fájlkezelőjén belül. (Ehelyett az operációs rendszer fájlkezelőjét kell használnod, és az Obsidian ezt törlésként és egy új fájl létrehozásaként fogja érzékelni. Az Obsidian **nem frissíti** azokat a hivatkozásokat, amelyek az adott fájl elérési útvonalától függtek.)
- A fájlokra mutató szimbolikus hivatkozások (_nem_ mappákra mutató hivatkozások) **előfordulhat, hogy működnek**, de jelenleg **nem támogatottak hivatalosan**. Az Obsidian nem figyeli az alkalmazáson kívüli változásokat, így ha közvetlenül módosítasz egy fájlt, az Obsidian nem érzékeli ezt, és nem frissíti a keresési indexeket sem.
- Ha megosztás céljából a `.obsidian/` mappán belül hozol létre szimbolikus hivatkozásokat, **nagyon nagy az esélye, hogy elrontod a beállításaidat**, hacsak **nem tudod pontosan, mit csinálsz**. Ha ezt az utat választod, **legalább készíts biztonsági mentéseket**.
