---
aliases:
  - alias
  - aliases
  - How to/Add aliases to note
permalink: aliases
cssclasses:
  - soft-embed
---

Ha egy fájlra különböző nevekkel szeretnél hivatkozni, érdemes _álnévként_ (alias) megadni a jegyzetben. Egy alias egy alternatív név a jegyzet számára.

Használj álneveket olyan esetekben, mint rövidítések, becenevek, vagy amikor egy jegyzetre más nyelven szeretnél utalni.

Ha csak egy adott helyen szeretnéd megváltoztatni a hivatkozás megjelenését, akkor nézd meg [[Internal links#Change the link display text|A hivatkozás megjelenésének módosítása]].

![[Internal links#^callout-internal-links-link-text]]

## Álnevek hozzáadása egy jegyzethez

Egy jegyzethez alias hozzáadásához adj hozzá egy `aliases` tulajdonságot a jegyzet [[Properties|Tulajdonságaihoz]]. Az aliasokat **mindig listaként** kell formázni YAML-ban.

```md
---
aliases:
  - Doggo
  - Woofer
  - Yapper
---

# Dog
```

## Hivatkozás jegyzetre álnevek segítségével

Jegyzetre aliason keresztül hivatkozni:

1. Kezd el beírni az alias nevét egy [[Internal links|belső hivatkozásban]]. Az alias megjelenik a javaslatok listájában, egy **ívelt nyíl ikon** mellett.
2. Nyomd meg az **Enter** gombot az alias kiválasztásához.

Az Obsidian létrehozza a hivatkozást az alias egyéni megjelenítési szövegével, például: `[[Mesterséges Intelligencia|MI]]`.

> [!note]  
> Az Obsidian nem egyszerűen az aliasra mutató hivatkozást (`[[MI]]`) hoz létre, hanem az **`[[Mesterséges Intelligencia|MI]]`** formátumot alkalmazza, hogy biztosítsa az **interoperabilitást** más alkalmazásokkal, amelyek a Wikilink formátumot használják.

## Álnevekhez tartozó nem kapcsolt említések keresése

A [[Backlinks|Visszahivatkozások]] segítségével megtalálhatod az aliasokra történő **nem kapcsolt említéseket**.

Például, miután az "MI" aliasként lett megadva a "Mesterséges intelligencia" jegyzet számára, láthatod az "MI" említéseit más jegyzetekben.

Ha egy **nem kapcsolt említést** egy aliashoz kötsz, az Obsidian az említést egy [[Internal links|belső hivatkozássá]] alakítja, amely az alias egyéni megjelenítési szövegeként működik.
