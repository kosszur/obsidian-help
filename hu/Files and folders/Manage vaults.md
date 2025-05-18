---
aliases:
  - Felhasználói felület/Tárolóváltó
  - Hogyan dolgozz több tárolóval
  - Tárolóváltó
permalink: manage-vaults
---
A **tároló** egy mappa a fájlrendszeredben, amely tartalmazza a jegyzeteidet, [[attachments|csatolmányokat]], valamint az Obsidian-specifikus beállításokat tartalmazó [[configuration folder|konfigurációs mappát]]. További információért lásd: [[How Obsidian stores data|Hogyan tárolja az Obsidian az adatokat]].

A tárolók kezeléséhez használhatod a **Tárolóváltót**. Az *Tárolóprofil* megnyílik, amikor először elindítod az Obsidian-t.

Egy meglévő tárolóból a tárolóváltó megnyitásához válaszd a **Tárolóprofil** gombot ( ![[lucide-chevrons-up-down.svg#icon]]) a [[Sidebar|bal oldali oldalsáv]] alján. Vagy válaszd a **Másik tároló megnyitása** opciót a [[command palette|Parancspalettában]].

## Új tároló létrehozása

1. Nyisd meg az Obsidian-t a számítógépeden.
2. A bal alsó sarokban válaszd a **Tárolóprofil** gombot ( ![[lucide-chevrons-up-down.svg#icon]]).
3. Egy menü jelenik meg. Válaszd a **Tárolók kezelése...** lehetőséget.
3. A **Új tároló létrehozása** opciónál kattints a **Létrehozás** gombra.
4. Az **Tároló neve** mezőben add meg az új tárolód nevét.
5. Kattints a **Tallózás** gombra, hogy kiválaszd, hova szeretnéd létrehozni az új tárolót.
6. Kattints a **Létrehozás** gombra.

## Tároló létrehozása meglévő mappából

1. Nyisd meg az Obsidian-t a számítógépeden.
2. A bal alsó sarokban válaszd a **Tárolóprofil** gombot ( ![[lucide-chevrons-up-down.svg#icon]]).
3. Egy menü jelenik meg. Válaszd a **Tárolók kezelése...** lehetőséget.
3. A **Meglévő mappa megnyitása tárolóként** opciónál kattints a **Megnyitás** gombra.
4. A fájlkezelőben válaszd ki azt a mappát, amelyet tárolóként szeretnél használni.
5. Kattints a **Megnyitás** gombra.

> [!tip] Tároló megnyitása az Obsidian Sync segítségével  
> Ha egy távoli tárolót szeretnél megnyitni az Obsidian Sync segítségével, lásd: [[Set up Obsidian Sync|Obsidian Sync beállítása]].

## Tároló átnevezése

Mivel a tároló neve megegyezik az alapul szolgáló mappa nevével, a tároló átnevezése a mappa nevét is módosítja.

1. Nyisd meg az Obsidian-t a számítógépeden.
2. A bal alsó sarokban válaszd a **Tárolóprofil** gombot ( ![[lucide-chevrons-up-down.svg#icon]]).
3. Egy menü jelenik meg. Válaszd a **Tárolók kezelése...** lehetőséget.
4. A tárolólistában kattints a **További lehetőségek** gombra ( ![[lucide-more-horizontal.svg]] ) az átnevezni kívánt tároló mellett.
5. Válaszd a **Tároló átnevezése** opciót.
6. Írd be az új nevet a tárolónak, majd nyomd meg az `Enter`-t.

## Tároló áthelyezése másik mappába

1. Nyisd meg az Obsidian-t a számítógépeden.
2. A bal alsó sarokban válaszd a **Tárolóprofil** gombot ( ![[lucide-chevrons-up-down.svg#icon]]).
3. Egy menü jelenik meg. Válaszd a **Tárolók kezelése...** lehetőséget.
4. Zárd be az aktuális tároló ablakát, hagyva a **Tárolók kezelése** ablakot nyitva.
5. A tárolólistában kattints a **További lehetőségek** gombra ( ![[lucide-more-horizontal.svg]] ) az áthelyezni kívánt tároló mellett.
6. Válaszd a **Tároló áthelyezése** lehetőséget, majd válaszd ki az új helyet.

Egyes operációs rendszerek nem teszik lehetővé a tároló áthelyezését a Tárolóváltóval. Ilyen esetekben manuálisan kell áthelyezned a tárolót:

1. Zárd be az Obsidian-t.
2. Mozgasd a tároló mappáját egy új helyre, elkerülve más szolgáltatások által szinkronizált mappákat.
3. Nyisd újra az Obsidian-t.
4. Kattints a **Tárolóprofil** ikonra a bal alsó sarokban ( ![[lucide-chevrons-up-down.svg#icon]]).
5. A felugró menüben válaszd a **Tárolók kezelése...** lehetőséget.
6. A **Mappa megnyitása tárolóként** opciónál kattints a **Megnyitás** gombra.
7. Navigálj az új tároló mappádhoz, és válaszd ki.
8. Kattints a **Megnyitás** gombra.
9. Ellenőrizd, hogy a tároló tartalma változatlan maradt. Szükség esetén újra engedélyezheted a közösségi bővítményeket a **Beállítások → Közösségi bővítmények → Korlátozott mód kikapcsolása** menüben.

## Tároló eltávolítása

Egy tároló eltávolítása **csak** a tároló listából törli azt.

1. Nyisd meg az Obsidian-t a számítógépeden.
2. A bal alsó sarokban válaszd a **Tárolóprofil** gombot ( ![[lucide-chevrons-up-down.svg#icon]]).
3. Egy menü jelenik meg. Válaszd a **Tárolók kezelése...** lehetőséget.
4. A tárolólistában kattints a **További lehetőségek** gombra ( ![[lucide-more-horizontal.svg]] ) az eltávolítani kívánt tároló mellett.
5. Válaszd a **Eltávolítás a listából** opciót.

## Beállítások átvitele másik tárolóra

Ha ugyanazokat a beállításokat szeretnéd használni egy másik tárolónál, másold át a `.obsidian` mappát az eredeti tároló gyökérmappájából a cél tároló gyökérmappájába a fájlkezelőd vagy terminálod segítségével.

Előfordulhat, hogy újra kell indítanod az Obsidian-t, hogy a módosítások életbe lépjenek.

> [!note] Hol található a `.obsidian` mappa?
> Alapértelmezés szerint a legtöbb operációs rendszer elrejti a ponttal (`.`) kezdődő mappákat. További információért és a `.obsidian` mappa eléréséhez lásd: [[How Obsidian stores data#Vault settings|Tároló beállítások]] és [[Configuration folder|Konfigurációs mappák]].
