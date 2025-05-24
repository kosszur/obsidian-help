---
aliases:
  - How to/Internal link
  - How to/Link to blocks
cssclasses:
  - soft-embed
description: Tanuld meg, hogyan hivatkozhatsz jegyzetekre, mellékletekre és egyéb fájlokra a jegyzeteidből.
mobile: true
permalink: links
publish: true
---

Tanuld meg, hogyan hivatkozhatsz jegyzetekre, mellékletekre és egyéb fájlokra a jegyzeteidből, az úgynevezett _belső hivatkozásokkal_. A jegyzetek összekapcsolásával tudáshálózatot hozhatsz létre. ^b15695

Az Obsidian automatikusan frissíti a belső hivatkozásokat a tárolódban, ha átnevezel egy fájlt.  
Ha inkább megerősítést szeretnél kapni előtte, ezt kikapcsolhatod a következő helyen:

Beállítások → Fájlok és hivatkozások → Belső hivatkozások automatikus frissítése

## Támogatott formátumok belső hivatkozásokhoz

Az Obsidian az alábbi hivatkozási formátumokat támogatja:

- Wikilink: `[[Három törvény a mozgásról]]`
- Markdown: `[Három törvény a mozgásról](Három%20törvény%20a%20mozgásról.md)`

Az alábbi példák egyenértékűek—ugyanúgy jelennek meg a szerkesztőben, és ugyanarra a jegyzetre mutatnak.

> [!note]  
> Markdown formátum használatakor győződj meg róla, hogy a hivatkozási cél helyesen van URL-kódolva.  Például a szóköz `%20` karakterré alakul.

Alapértelmezés szerint az Obsidian a kompaktabb formátum miatt a Wikilink formátumot használja. Ha számodra az interoperabilitás fontos, akkor kikapcsolhatod a Wikilinket, és használhatsz Markdown hivatkozásokat.

A Markdown formátum bekapcsolása:

1. Nyisd meg a Beállítások menüt.
2. A Fájlok és hivatkozások alatt kapcsold ki a Használj \[\[Wikilink\]\] formátumot opciót.

Még ha letiltod a Wikilink formátumot, akkor is használhatod az automatikus kitöltést két szögletes zárójel beírásával: `[[`.  Amikor kiválasztod egyik ajánlott fájlt, az Obsidian Markdown hivatkozást hoz létre.

## Fájlra mutató hivatkozás létrehozása

A szerkesztési nézetben hivatkozás létrehozásához az alábbi módszerek egyikét használhatod:

- Írd be a `[[` karaktereket a szerkesztőben, majd válaszd ki a fájlt, amelyre hivatkozni szeretnél.
- Jelölj ki szöveget a szerkesztőben, majd gépeld be a `[[` karaktereket.
- Nyisd meg a [[Command palette|Parancspalettát]], majd válaszd a Belső hivatkozás hozzáadása opciót.

![[Quick switcher#^search-autocomplete-large]]

Bármelyik [[Accepted file formats|támogatott fájlformátumra]] hivatkozhatsz, de a Markdown formátumon kívüli fájlokhoz a fájlkiterjesztést is hozzá kell adnod, például: `[[Figure 1.png]]`.

> [!tip]  
> Ha egy belső hivatkozás elé felkiáltójelet (`!`) helyezel, az Obsidian beágyazza a hivatkozott tartalmat. További részletekért lásd: [[Embed Files|Fájlok beágyazása]].

## Címsorra mutató hivatkozás egy jegyzetben

Hivatkozhatsz jegyzeteken belüli konkrét címsorokra, más néven _horgonyhivatkozásokra_.

**Címsor hivatkozása ugyanabban a jegyzetben**

Ha egy címsorra szeretnél hivatkozni ugyanabban a jegyzetben, gépeld be `[[#`, hogy megjelenjen a jegyzetben lévő címsorok listája.

Például:  `[[#Kapcsolt fájl előnézete]]` egy hivatkozást hoz létre a [[#Kapcsolt fájl előnézete]] címsorra.

**Címsor hivatkozása egy másik jegyzetben**

Ha egy címsorra egy másik jegyzetben szeretnél hivatkozni, adj hozzá egy kettőskeresztet (`#`) a hivatkozás végéhez, majd a címsor szövegét.

Példa:  `[[Obsidian#A hivatkozások első osztályú elemek]]` egy hivatkozást hoz létre a [[Obsidian#A hivatkozások első osztályú elemek]] címsorra.

**Alcímsorokra mutató hivatkozás**

Többszörös kettőskereszt (`#`) karakterekkel hivatkozhatsz alcímsorokra is.

Példa:  `[[Help and support#Kérdések és tanácsok#Hibák jelentése és funkciók kérése]]` egy hivatkozást hoz létre a [[Help and support#Kérdések és tanácsok#Hibák jelentése és funkciók kérése]] alcímre.

**Címsorok keresése az egész tárolóban**

A teljes tárolóban címsorokat kereshetsz a következő formátummal: `[[## címsor]]`.

Például:  `[[##` keresés általánosan a tárolóban címsorokra. `[[## csapat]]` keresés minden olyan címsorra, amely tartalmazza a _csapat_ szót.

> [!info]- Képernyőkép címsorhivatkozás kereséséről  
>  
> ![[internal-links-header.png#interface]]

## Hivatkozás egy blokkra egy jegyzetben

Egy blokk egy egységnyi szöveg a jegyzetedben, például egy bekezdés, idézet vagy listaelem.

Blokkra hivatkozhatsz úgy, hogy a hivatkozás végéhez hozzáadod a `#^` karaktereket, majd egy egyedi blokkazonosítót. Például:  `[[2023-01-01#^37066d]]`.  Szerencsére nem kell manuálisan megkeresned az azonosítót—amikor beírod a `^` jelet, megjelenik egy javaslati lista, amelyből kiválaszthatod a megfelelő blokkot.

*Egyszerű bekezdések* esetében, helyezd a blokkazonosítót a sor végére:

```md
A gyors lila drágakő száguld át a bekezdésen villámsebességgel. Tollal a kezében és egy gemkapoccsal a másikban, Gemmy azon dolgozik, hogy a jegyzetelés világát boldogabb hellyé tegye. ^37066d
```

*Strukturált blokkok* (listák, idézetek, kiemelések, táblázatok) esetében, a blokkazonosítónak külön sorban kell lennie, előtte és utána egy üres sorral:

```md
> A gyors lila drágakő száguld át a bekezdésen villámsebességgel. Tollal a kezében és egy gemkapoccsal a másikban, Gemmy azon dolgozik, hogy a jegyzetelés világát boldogabb hellyé tegye.

^37066f

Ez Gemmy, a Segítőtlen asszisztens története.
```

*Konkrét sorok listán belül*  A blokkazonosító közvetlenül a listaelem végére kerülhet:

```mathjax
- Gemmy
    $$Paperclip / Pen$$ 
    ^37006f
- Unhelpful assistant
```

> [!warning] Nem támogatjuk hivatkozás létrehozását idézetek, kiemelések és táblázatok egyes részeihez.

**Blokkok keresése az egész tárolóban**

A teljes tárolóban kereshetsz blokkokat a következő formátummal: `[[^^block]]`.  Mivel több elem minősül blokknak, mint a [[#Link to a heading in a note|címsorhivatkozásoknál]], a lista sokkal hosszabb lesz.

> [!info]- Képernyőkép blokk hivatkozás kereséséről ![[link-block-heading.png#interface]]

Ember által olvasható blokkazonosítót úgy hozhatsz létre, hogy egy szóközt adsz a blokk végéhez, majd az azonosítót. A blokkazonosító csak latin betűket, számokat és kötőjeleket tartalmazhat.

Példa:  Adj hozzá `^quote-of-the-day` azonosítót egy blokk végére:

```md
"Nem a céljaid szintjére emelkedsz, hanem a rendszereid szintjére esel." James Clear ^quote-of-the-day
```

Most erre a blokkra hivatkozhatsz ezzel:  `[[2023-01-01#^quote-of-the-day]]`.

> [!warning] Interoperabilitás  A blokkhivatkozások az Obsidian saját funkciói, és nem részei a szabványos Markdown formátumnak.  A blokkhivatkozásokat tartalmazó linkek nem működnek az Obsidianon kívül.

## Hivatkozás megjelenítési szövegének módosítása

Alapértelmezés szerint az Obsidian a hivatkozásokat az eredeti szövegükkel jeleníti meg. Például:  
- `[[Példa]]` így jelenik meg: [[Példa]]  
- `[[Példa#Részletek]]` így jelenik meg: [[Példa#Részletek]]

A hivatkozás megjelenítését testreszabhatod a következő módon:

**Wikilink formátum**  
Használj függőleges vonalat (`|`) a megjelenített szöveg módosításához.

- `[[Példa|Egyedi név]]` így jelenik meg: [[Példa|Egyedi név]]  
- `[[Példa#Részletek|Szakasznév]]` így jelenik meg: [[Példa#Részletek|Szakasznév]]

**Markdown formátum**  
Használj `[Megjelenített szöveg](Hivatkozás URL)` formátumot a testreszabáshoz.

- `[Egyedi név](Példa.md)` így jelenik meg: [Egyedi név](Példa.md)  
- `[Szakasznév](Példa.md#Részletek)` így jelenik meg: [Szakasznév](Példa.md#Részletek)

Ez a módszer hasznos egyedi esetekben, amikor egy adott kontextusban módosítani szeretnéd a hivatkozás megjelenését. Ha egy alternatív hivatkozási nevet szeretnél beállítani, amelyet ismételten használhatsz a tárolódban, fontold meg az [[Aliases|aliasok]] használatát.

Példa:  
Ha rendszeresen a `[[Három törvény a mozgásról]]` jegyzetre `[[A 3 törvény]]` néven hivatkozol, adj hozzá "3 törvény" aliasként—így nem kell egyéni megjelenítési szöveget írnod minden alkalommal.

> [!tip]  
> Használd a [[#Change the link display text|hivatkozás megjelenítési szövegét]], amikor *egy adott helyen* testre szeretnéd szabni a hivatkozás megjelenését.  
>  
> Használj [[Aliases|aliasokat]], ha *különböző nevekkel* szeretnél hivatkozni ugyanarra a jegyzetre a tárolódban. ^callout-internal-links-link-text

## Kapcsolt fájl előnézete

> [!note]  
> A kapcsolt fájlok előnézetének használatához először engedélyezned kell a [[Page preview|Lap előnézetet]].

Egy kapcsolt fájl előnézetéhez tartsd lenyomva a `Ctrl` (macOS-en `Cmd`) billentyűt, miközben ráviszed a kurzort a hivatkozásra. Az előnézet megjelenik a kurzor mellett, így gyorsan megnézheted a fájl tartalmát.

