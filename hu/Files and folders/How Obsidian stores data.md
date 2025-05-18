---
aliases:
  - Haladó témák/Az Obsidian adatkezelése
description: Ez az oldal ismerteti, hogyan tárolja az Obsidian az adatokat az eszközödön.
mobile: true
permalink: data-storage
publish: true
---

Az Obsidian a jegyzeteidet [[Basic formatting syntax|Markdown-formázású]] sima szöveg fájlokként tárolja egy _tárolóban_. A tároló egy mappa a helyi fájlrendszereden, amely magában foglalhat almappákat is.

Mivel a jegyzetek egyszerű szövegfájlok, más szövegszerkesztőkkel és fájlkezelőkkel is szerkesztheted és kezelheted őket. Az Obsidian automatikusan frissíti a tárolódat, hogy kövesse a külső változtatásokat.

A tárolót bárhová létrehozhatod, ahol az operációs rendszered engedélyezi. Az Obsidian szinkronizálható [[Introduction to Obsidian Sync|Obsidian Sync]], Dropbox, iCloud, OneDrive, Git és számos más harmadik fél szolgáltatással.

Több mappát is megnyithatsz különálló tárolóként, például hogy elkülönítsd a munka és az iskola jegyzeteit.

> [!warning] Tárolók tárolón belül  
> Mivel az [[Internal links|Belső hivatkozások]] egy adott tárolóra vonatkoznak, **nem ajánlott tárolókat létrehozni tárolón belül**, mivel a hivatkozások esetleg nem frissülnek megfelelően.

## Tároló beállítások

Az Obsidian létrehoz egy `.obsidian` [[configuration folder|konfigurációs mappát]] a tároló gyökérmappájában, amely tartalmazza az adott tárolóra vonatkozó beállításokat, például a [[hotkeys|gyorsbillentyűket]], [[themes|témákat]], és [[community plugins|közösségi bővítményeket]].

Alapértelmezés szerint a legtöbb operációs rendszer elrejti a ponttal (`.`) kezdődő mappákat, ezért szükség lehet a fájlkezelő beállításainak frissítésére, hogy láthatóvá váljanak.

- **macOS**: A Finderben nyomd meg a `Cmd+Shift+.` (pont) billentyűkombinációt a rejtett fájlok megjelenítéséhez.
- **Windows**: [Rejtett fájlok megjelenítése](https://support.microsoft.com/en-us/windows/show-hidden-files-0320fe58-0117-fd59-6851-9b7f9840fdb2)
- **GNU/Linux**: A legtöbb fájlkezelőben nyomd meg a `Ctrl + h` billentyűkombinációt a rejtett fájlok megjelenítéséhez.

> [!tip] `.obsidian` hozzáadása Githez  
> Az `.obsidian/workspace.json` és `.obsidian/workspaces.json` fájlok tárolják az aktuális munkaterület elrendezését, és frissülnek, amikor új fájlt nyitsz meg. Ha a tárolódat [Git](https://git-scm.com) segítségével kezeled, érdemes lehet ezeket a fájlokat hozzáadni a `.gitignore` fájlhoz.

## Globális beállítások

Az Obsidian a globális beállításokat egy rendszer mappában tárolja. A rendszer mappa helye az operációs rendszertől függ:

- **macOS**: `/Users/felhasználónév/Library/Application Support/obsidian`
- **Windows**: `%APPDATA%\Obsidian\`
- **Linux**: `$XDG_CONFIG_HOME/obsidian/` vagy `~/.config/obsidian/`

> [!warning] Ne hozz létre tárolót a rendszer mappában. Ez adatkárosodást vagy adatvesztést okozhat.

## IndexedDB

Az IndexedDB egy alacsony szintű, kliensoldali adatbázis, amelyet az Obsidian háttértárolásra használ. Segít fenntartani az [[Introduction to Obsidian Sync|Obsidian Sync]] kapcsolatok állapotát, és megőrzi a [[#Metadata cache|metaadat gyorsítótárat]] az alkalmazás bezárásakor.

> [!warning] Ha az Apple [Lockdown Mode](<https://support.apple.com/en-us/105120>) engedélyezve van, és az Obsidian nincs kizárva, ezek az adatbázis-fájlok nem mentődnek el, és az alkalmazás minden indításkor újra kell indexelnie őket.

### Metaadat gyorsítótár

Az alkalmazás gyors működésének érdekében az Obsidian helyileg tárolja a tároló fájljaira vonatkozó **metaadat gyorsítótárat**. Ez az adat segíti több funkció működését az alkalmazásban, például a Grafikon nézetet és a Vázlat nézetet.

Az Obsidian szinkronban tartja ezt a gyorsítótárat a tároló fájljaival, de előfordulhat, hogy az adatok eltérnek az alapul szolgáló fájloktól. Ha ez megtörténik, az *Fájlok és hivatkozások* szekcióban újraépítheted a metaadat gyorsítótárat az alkalmazás beállításaiban.
