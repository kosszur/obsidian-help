---
aliases:
  - Stacked tabs
  - Linked pane
  - Pane layout
  - User interface/Use tabs in Obsidian
permalink: tabs
---
A fülek az Obsidianban hasonlóan működnek, mint más alkalmazásokban, például webböngészőkben.

Az Obsidianban tetszőleges számú fület nyithatsz meg. A fülek elrendezését testreszabhatod, és az így kialakított elrendezés megmarad, amíg legközelebb meg nem nyitod az alkalmazást.

## Új fül megnyitása

Az alkalmazásablak tetején, a jobb oldalon található utolsó fül mellett válaszd a **Új fül** ( ![[lucide-plus.svg#icon]] ) lehetőséget, vagy használd a következő billentyűparancsokat:

- **Windows és Linux:** `Ctrl+t`
- **macOS:** `Cmd+t`

## Hivatkozás megnyitása

Kattints egy hivatkozásra az Obsidianban, hogy az aktív fülön nyíljon meg.

Ha egy hivatkozást új fülön szeretnél megnyitni, nyomd meg a `Ctrl` (vagy macOS-en `Cmd`) billentyűt, majd kattints a hivatkozásra.

Az alábbi módosítóbillentyűkkel különböző módon nyithatsz meg hivatkozásokat:

|Művelet|MacOS|Windows/Linux|
|---|---|---|
|**Navigáció**|_Nincs_|_Nincs_|
|**Új fül**|`⌘` (+ `Shift` forrásnézetben)|`Ctrl` (+ `Shift` forrásnézetben)|
|**Új fülcsoport**|`⌘` `⌥`| `Ctrl` `Alt`|
|**Új ablak**|`⌘` `⌥` `Shift`|`Ctrl` `Alt` `Shift`|

## Fülek és ablakok szervezése

Minden fül egy _fülcsoporthoz_ tartozik. A füleket húzással átrendezheted egy fülcsoporton belül, áthelyezheted másik fülcsoportba, vagy létrehozhatsz új fülcsoportot. Asztali verzióban a füleket áthúzhatod az ablakon kívülre, hogy különálló [[Pop-out windows|felugró ablakban]] nyíljanak meg.

Az oldalsávban lévő fülek csak az ikont mutatják. Az ikon fölé húzva egy tooltip jelenik meg a fül címével.

### Fülek átrendezése

A fülek sorrendjének módosításához húzd el a fület a fülcsoporton belül.

Húzás közben _ejtési zónák_—területek, ahová a fület helyezheted—kiemelődnek. Az ejtési zóna határozza meg, hol helyezkedik el a fül. Egyes fülek csak az oldalsávokban lehetnek.

### Fülcsoport felosztása

Jobb kattintással egy fülre válaszd a **Felosztás jobbra** vagy **Felosztás lefelé** lehetőséget, hogy új fülcsoportot hozz létre az adott füllel.

Egy fülcsoportot úgy is feloszthatsz, ha egy fület lehúzol egy másik fülcsoport aljára.

### Fülcsoport átméretezése

A fülcsoport átméretezéséhez húzd a kurzort a fülcsoport széléhez. A szél kiemelődik, ha átméretezhetővé válik.

Az oldalsávokat hasonló módon átméretezheted, hogy több helyet biztosíts a középső fülcsoportok számára.

### Fül áthelyezése új ablakba

**Húzás és ejtés:**

- Válaszd ki és húzd a fület az alkalmazásablakon kívülre, hogy új ablakban nyíljon meg.

**Parancspaletta:**

- Nyisd meg a Parancspalettát, és válaszd a **Jelenlegi fül mozgatása új ablakba** lehetőséget.

### Fül áthelyezése másik ablakba

Egy fület egy másik meglévő ablakba való áthelyezéshez húzd át a fület a célablakba.

### Fül rögzítése

Egy fül rögzítéséhez kattints jobb gombbal a fülre, majd válaszd a **Rögzítés** lehetőséget. A rögzített fülben megnyitott hivatkozások mindig külön fülön nyílnak meg.

Egy rögzített fül feloldásához kattints jobb gombbal a fülre, majd válaszd a **Rögzítés feloldása** lehetőséget.

## Váltás másik fülre

Válaszd ki a kívánt fület a váltáshoz, vagy használd az alábbi billentyűparancsokat:

| Váltás                 | MacOS            | Windows/Linux        |
|------------------------|------------------|----------------------|
| **Következő fül**      | `⌃`+`⇥`          | `Ctrl`+`Tab`         |
| **Előző fül**         | `⌃`+`⇧`+`⇥`      | `Ctrl`+`Shift`+`Tab` |
| **Első fül balra**    | `⌘`+`1`           | `Ctrl`+`1`           |
| **2. és 8. fül között** | `⌘`+`2`..`8`     | `Ctrl`+`2`..`8`      |
| **Utolsó fül jobbra** | `⌘`+`9`           | `Ctrl`+`9`           |
| **Nemrég bezárt fül** | `⌘`+`⇧`+`t`      | `Ctrl`+`Shift`+`t`   |

## Fülcsoportok egymásra helyezése

Az Obsidianban a fülek egymásra helyezhetők, így azok átlapolva jelennek meg ugyanabban a fülcsoportban.

A jegyzetek egymásra helyezéséhez válaszd a lefelé mutató nyilat a fülcsoport jobb felső sarkában, majd válaszd a **Jegyzetek egymásra helyezése** lehetőséget.

![tab-stacks](https://user-images.githubusercontent.com/693981/188205363-0f24b2a5-3706-4a8c-b38b-7a66baa68ce6.gif)

A fülhalmok inspirációját [Andy Matuschak csúszó jegyzetei](https://notes.andymatuschak.org/) adták.

## Kapcsolt nézetek

A _kapcsolt nézetek_ olyan fülek, amelyek egy másik fülre hivatkoznak. Ha a hivatkozott fül tartalma változik, a kapcsolt nézet is frissül.

Jegyzetfülek esetén az alábbi bővítményeket használhatod kapcsolt nézetként:

- [[Graph view]] (helyi)
- [[Backlinks]]
- [[Outline]]

Kapcsolt nézet megnyitása egy jegyzetfül számára:

1. Válaszd a **További lehetőségek** (![[lucide-more-horizontal.svg#icon]]) ikont a jegyzet jobb felső sarkában.
2. A **Kapcsolt nézet megnyitása** alatt válaszd ki a kívánt nézetet.

## Elrendezések mentése

Az ablakelrendezések mentéséhez és visszaállításához használd a [[Workspaces]] bővítményt.

