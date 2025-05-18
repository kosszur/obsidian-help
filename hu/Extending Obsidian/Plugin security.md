---
permalink: plugin-security
---
Az Obsidian csapata komolyan veszi a biztonságot. Ez az oldal elmagyarázza a közösségi bővítmények telepítésével járó kockázatokat, valamint azt, hogy az Obsidian csapata mit tesz ezek kezelésére.

## Korlátozott mód

Az Obsidian alapértelmezés szerint **Korlátozott módban** fut, hogy megakadályozza a harmadik fél által készített kódok végrehajtását. Csak akkor kapcsold ki a korlátozott módot, ha **megbízol** a telepíteni kívánt bővítmények szerzőiben.

A **Korlátozott mód kikapcsolása**:

1. Nyisd meg a **Beállítások** menüt.
2. A bal oldali menüben válaszd a **Közösségi bővítmények** opciót.
3. Kattints a **Közösségi bővítmények bekapcsolása** lehetőségre.

A **Korlátozott mód bekapcsolása**:

1. Nyisd meg a **Beállítások** menüt.
2. A bal oldali menüben válaszd a **Közösségi bővítmények** opciót.
3. A **Korlátozott mód** mellett válaszd a **Bekapcsolás** lehetőséget.

A **telepített bővítmények** a tárolóban **megmaradnak**, még akkor is, ha bekapcsolod a Korlátozott módot, de az Obsidian **figyelmen kívül hagyja** őket.

## Bővítmények lehetőségei

Műszaki korlátok miatt az Obsidian **nem tudja megbízhatóan korlátozni** a bővítmények **hozzáférési szintjeit** vagy **engedélyeit**. Ez azt jelenti, hogy a bővítmények **öröklik** az Obsidian hozzáférési szintjeit. Ennek eredményeként a közösségi bővítmények az alábbiakat tehetik:

- Hozzáférhetnek a számítógépen **tárolt fájlokhoz**.
- **Kapcsolódhatnak** az internethez.
- **További programokat telepíthetnek**.

> [!tip]  
> Ha **érzékeny adatokkal dolgozol**, és közösségi bővítményt szeretnél telepíteni, **ajánlott** egy **független biztonsági audit** elvégzése **használat előtt**.

## Bővítmény-ellenőrzési folyamat

A közösségi bővítmények **kezdeti ellenőrzésen** esnek át, amikor benyújtják őket a bővítmény áruházba. Minden bővítménynek **meg kell felelnie** az [Obsidian fejlesztési irányelveinek](https://docs.obsidian.md/Developer+policies).

Az Obsidian csapata **kis létszámú**, ezért nem tud **minden új bővítménykiadást** manuálisan ellenőrizni. Ehelyett **a közösség segítségére támaszkodunk**, hogy azonosítsa és **jelentse** a bővítményekkel kapcsolatos problémákat.

- Ha **kisebb biztonsági problémát** fedezel fel egy közösségi bővítményben, **nézd meg a bővítmény szerzőjének `security.md` vagy `readme.md` fájlját**, hogyan kell jelenteni.  
  Ha **kritikus sebezhetőséget** találsz, **jelentsd** az esetet [[Help and support#Contact Obsidian support|Obsidian támogatásnak]] is.
- Ha úgy **gyanítod**, hogy egy közösségi bővítmény **rosszindulatú**, **jelentsd** azt [[Help and support#Contact Obsidian support|Obsidian támogatásnak]], vagy küldj **privát üzenetet** a moderátorainknak.
