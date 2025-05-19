# Obsidian Súgó

Ez a tároló tartalmazza az [Obsidian Súgó dokumentáció](https://help.obsidian.md/) forrását,  
valamint minden támogatott nyelvhez tartozó fordításokat.

⚠ **Ne nyiss itt hibajelentéseket vagy funkciókéréseket az Obsidianhoz**!  
Az ilyen bejegyzések **lezárásra kerülnek**, és **átirányítunk a fórumra**.

Az egyes nyelvekhez tartozó dokumentáció **önálló tárolók**,  
amelyekhez egy **megfelelő [Obsidian Publish](https://help.obsidian.md/Obsidian+Publish/Introduction+to+Obsidian+Publish) weboldal kapcsolódik**.

| Nyelv | URL                                   |
| -------- | --------------------------------------- |
| `en`     | https://help.obsidian.md/               |
| `ar`     | https://publish.obsidian.md/help-ar/    |
| `da`     | https://publish.obsidian.md/help-da/    |
| `es`     | https://publish.obsidian.md/help-es/    |
| `it`     | https://publish.obsidian.md/help-it/    |
| `ja`     | https://publish.obsidian.md/help-ja/    |
| `ko`     | https://publish.obsidian.md/help-ko/    |
| `pt-br`  | https://publish.obsidian.md/help-pt-br/ |
| `ru`     | https://publish.obsidian.md/help-ru/    |
| `vi`     | https://publish.obsidian.md/help-vi/    |
| `zh`     | https://publish.obsidian.md/help-zh/    |

## Hozzájárulás

Az Obsidian Súgó dokumentációhoz való hozzájárulás lépései:

1. **Fork-old** az [obsidian-help](https://github.com/obsidianmd/obsidian-help) tárolót.
2. Az Obsidian tárolóváltójában válaszd az **Mappa megnyitása tárolóként** lehetőséget.
3. Válaszd ki a fordításhoz tartozó almappát, például `/en/`.  
   **Ne nyisd meg a gyökérmappát**, mert ez **hibás linkfrissítéseket eredményezhet**.

Hozzájárulási lehetőségek:

- **Helyesírási hibák és elírások javítása**:  
  Ha egy **elírást vagy kisebb módosítást** szeretnél javítani, küldj be egy **pull requestet**.  
  Kis szerkesztésekhez használhatod a **GitHub webes felületét**, nem szükséges a tároló klónozása.
- **Hiányzó vagy elavult tartalom hozzáadása**:  
  Ha **hiányzó vagy elavult tartalmat** szeretnél hozzáadni, kérlek **először** [nyiss egy hibajelentést](https://github.com/obsidianmd/obsidian-help/issues/new), mielőtt dolgozni kezdesz rajta.

Az angol nyelvű dokumentációhoz **minden hozzájárulásnak követnie kell**  
a **[Stílus útmutatót](https://help.obsidian.md/Contributing+to+Obsidian/Style+guide)**.

## Fordítások

### Új fordítás hozzáadása

Új fordítás létrehozásához másold az egész `en` mappát, majd nevezd át az adott nyelvhez tartozó [ISO 639-1](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) kódnak megfelelően, kisbetűkkel.

Minden fordításnak **a lehető legközelebb kell állnia** az angol dokumentációhoz (`en`).

### Naprakészen tartás

Ahogy új funkciókat adunk hozzá, és továbbfejlesztjük az angol dokumentációt, a fordítások idővel **elavulhatnak**.

A fordítás **utolsó frissítése óta bekövetkezett módosítások megtekintéséhez** futtasd az alábbi parancsot a terminálban:

```bash
git diff <COMMIT_SHA> HEAD -- en/
```


Cseréld ki `<COMMIT_SHA>` értékét a **fordítás legutóbbi változtatásait tartalmazó commit hash-re**.

> **Megjegyzés**: Ha egy fordítás **túlságosan lemarad** az angol verzióhoz képest, **esetlegesen eltávolítjuk** azt.

## Útiterv

Az Obsidian Súgó dokumentáció az évek során **jelentősen bővült**.  
Jelenleg dolgozunk néhány tartalom **újraszervezésén**, hogy **könnyebben megtalálható és érthető** legyen.

A következő mappákban lévő dokumentációkat **frissítettük** az **új szervezési struktúrára és stílus útmutatóra**.  
Ha egy fordításon dolgozol, **ezek biztonságosan fordíthatók** (kivéve kisebb frissítéseket).

- [x] Hozzájárulás az Obsidianhoz
- [x] Fejlesztők
- [x] Szerkesztés és formázás
- [x] Az Obsidian bővítése
- [x] Első lépések
- [x] Licencek és fizetés
- [x] Obsidian Publish
- [x] Obsidian Sync
- [x] Bővítmények

## Kreditek

Ha szeretnéd, hogy a neved megjelenjen a [Kreditek](https://help.obsidian.md/Obsidian/Credits) oldalon,  
add hozzá magad a [Credits](https://github.com/obsidianmd/obsidian-help/blob/master/en/Obsidian/Credits.md) fájlhoz, és az **adott fordításhoz** is.

## További erőforrások

- [Stílus útmutató](https://help.obsidian.md/Contributing+to+Obsidian/Style+guide)
- [Fordítások](https://help.obsidian.md/Contributing+to+Obsidian/Translations)
