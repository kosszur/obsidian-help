---
permalink: glossary
---
Ez a szószedet az Obsidian gyakori terminológiáját tartalmazza.

## Alias

Az **alias** egy [[#property|tulajdonság]] típus, amely alternatív neveket határoz meg egy [[#note|jegyzet]] számára.

## Csatolmány

A **csatolmány** egy [[Accepted file formats|elfogadott fájlformátum]], amelyet a tárolón kívül hoztak létre, majd később hozzáadtak.

## Parancs

A **parancs** egy művelet, amelyet végrehajthatsz úgy, hogy kiválasztod a [[Command palette|Parancs paletta]] menüből, vagy hozzárendeled egy [[#hotkey|gyorsbillentyűhöz]].

## Beágyazás

A **beágyazás** azt jelenti, hogy egy külső tartalomra mutató hivatkozást közvetlenül a tartalommal helyettesítesz, például egy kép beillesztése a jegyzetedbe. Lásd még: [[Embed files|Fájlok beágyazása]].

## Frontmatter

A **frontmatter** lehetőséget biztosít [[#property|tulajdonságok]] meghatározására azáltal, hogy [YAML](https://yaml.org/) vagy [JSON](https://www.json.org/) formátumot adsz meg a jegyzet tetején. Lásd még: [[Properties#Property format|Tulajdonságok formátuma]].

## Grafikon

A **grafikon** egy vizualizáció, amely kiemeli a kapcsolatokat a [[#note|jegyzetek]] között. Lásd még: [[Graph view|Grafikon nézet]].

## Gyorsbillentyű

A **gyorsbillentyű** egy billentyűparancs egy [[#command|parancshoz]]. Lásd még: [[Hotkeys|Gyorsbillentyűk]] és [[Hotkeys|Hogyan használjuk a gyorsbillentyűket]].

## Hivatkozás

A **hivatkozás** egy másik jegyzetre vagy fájlra mutat. Egy [[Internal links|belső hivatkozás]] egy fájlra mutat a jelenlegi tárolóban. Egy [[Basic formatting syntax#External links|külső hivatkozás]] pedig egy tárolón kívüli helyre, jellemzően egy weboldalra mutat.

## Fő terület

A **fő terület** az Obsidian alkalmazás központi része, ahol elsődlegesen [[#note|jegyzeteket]] szerkeszthetsz.

## Markdown

A Markdown egy jelölőnyelv szövegformázáshoz, és az Obsidian által használt elsődleges fájlformátum, `.md` fájlok. Lásd még: [[Basic formatting syntax|Alapvető formázási szintaxis]].

## Jegyzet

A **jegyzet** egy Markdown fájl egy [[#vault|tárolón]] belül.

## Bővítmény

A **bővítmény** további funkciókkal bővíti az Obsidian-t.

- [[Core plugins|Alap bővítmények]]: Az Obsidian csapat által készített és alapértelmezetten elérhető bővítmények.
- [[Community plugins|Közösségi bővítmények]]: Külső fejlesztők által készített bővítmények, amelyeket először [[Community plugins#Install a community plugin|telepíteni]] kell a használathoz.

Saját bővítményt is készíthetsz: [Bővítmény készítése](https://docs.obsidian.md/Plugins/Getting+started/Build+a+plugin).

## Különálló ablak

Alapértelmezés szerint minden jegyzet egy tárolón belül ugyanabban az alkalmazásablakban nyílik meg. A **különálló ablak** lehetővé teszi, hogy ugyanazon tároló jegyzeteit külön ablakokban nyisd meg, például egy második képernyőn való megjelenítéshez.

Lásd még: [[Pop-out windows|Különálló ablakok]].

## Tulajdonság

A [[Properties|Tulajdonságok]] meghatározzák egy jegyzet további információit, például egy határidőt vagy a szerző nevét.

## Szalag

A **szalag** egy olyan terület, amelyben gyakran használt műveleti ikonokat találhatsz.

Az asztali verzióban ez a függőleges terület a bal oldalon található.

A mobil verzióban egy menü gomb ( ![[lucide-menu.svg#icon]] ) jeleníti meg a [[#status bar|állapotsávban]].

## Oldalsáv

Egy terület, amely támogató [[#view|nézeteket]] tartalmaz, és [[#tab|fülek]] szerint van rendezve. Az oldalsáv több [[#tab group|fülcsoport]] szerint is felosztható.

Az Obsidian asztali verziójában két oldalsáv található, egy-egy oldalán a [[#main area|fő területnek]]. Mindkét oldalsáv elérhető az alkalmazás bal felső és jobb felső sarkában található ikonokkal, valamint balra vagy jobbra húzással. A jobb felső ikon hosszan nyomva tartva nyitható meg az ablak.

## Snippet

Egy **snippet**, vagyis egy [[CSS snippets|CSS snippet]], módosítja az Obsidian megjelenését, hasonlóan egy [[#theme|témához]]. A témákkal ellentétben egyszerre több snippet is alkalmazható.

## Állapotsáv

Az **állapotsáv** az Obsidian alkalmazásban az alapvető statisztikákat és állapotokat jeleníti meg. Az asztali verzióban a jobb alsó sarokban található, míg mobil eszközökön az alkalmazás alján helyezkedik el.

## Fül

A **fül** egy [[#view|nézetet]] tartalmaz. A füleket áthelyezheted a [[#main area|fő területen]] és az [[#sidebar|oldalsávokon]]. Lásd még: [[Tabs|Fülek]].

## Fülcsoport

A **fülcsoport** egy [[#tab|fülekből]] álló gyűjtemény a [[#main area|fő területen]]. A fülek egy fülcsoportban egymásra halmozhatók.

## Címke

A **címke** egy olyan szó, amely kettős kereszt (`#`) jellel kezdődik, például `#könyv`. A címkéket elsősorban a kapcsolódó [[#note|jegyzetek]] keresésére használják.

## Téma

A **téma** megváltoztatja az Obsidian alkalmazás kinézetét [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) segítségével. Egy témát módosíthatsz [[#snippet|snippek]] használatával.

## Tároló

`Aliasok: helyi tároló, helyi adatok`

A **tároló** egy mappa a fájlrendszeredben, amely tartalmazza a [[#note|jegyzeteket]] és egy `.obsidian` mappát az Obsidian-specifikus konfigurációval. Lásd még: [[How Obsidian stores data|Hogyan tárolja az Obsidian az adatokat]].

### Távoli tároló

`Aliasok: távoli adatok`

A [[Local and remote vaults|távoli tároló]] a helyi tárolód másolata, amelyet az [[Introduction to Obsidian Sync|Obsidian Sync]] segítségével tartanak karban. A távoli tároló adatai a helyi adatok változásai alapján frissülnek.

## Nézet

Egy **nézet** információkat jelenít meg, például a [[Search|Keresés nézetet]].
