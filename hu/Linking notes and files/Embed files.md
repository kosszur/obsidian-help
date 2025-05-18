---
aliases:
  - How to/Embed files
  - Linking notes and files/Embedding files
cssclasses:
  - soft-embed
permalink: embeds
---

Tanuld meg, hogyan ágyazhatsz be más jegyzeteket és médiát a jegyzeteidbe. A fájlok beágyazásával **újrahasznosíthatod** a tartalmat a tárolódon belül.

Egy fájl beágyazásához a tárolódban **helyezz el egy felkiáltójelet (`!`)** egy [[Internal links|belső hivatkozás]] elé.  
Beágyazhatod a fájlokat az **összes támogatott formátumban** ([[Accepted file formats]]).

> [!tip] Drag and Drop beágyazás  
> **Asztali számítógépen** a támogatott fájlokat **közvetlenül áthúzhatod** a jegyzetbe, így **automatikusan beágyazódnak**.

## Jegyzet beágyazása egy másik jegyzetbe

Egy jegyzet beágyazásához:

```md
![[Internal links]]
```

Beágyazhatsz hivatkozásokat [[Internal links#Link to a heading in a note|címsorokhoz]] és [[Internal links#Link to a block in a note|blokkokhoz]] is.

```md
![[Internal links#^b15695]]
```

Az alábbi szöveg egy **beágyazott blokk példája**:

![[Internal links#^b15695]]

## Kép beágyazása egy jegyzetbe

Egy kép beágyazásához:

```md
![[Engelbart.jpg]]
```

![[Engelbart.jpg#outline]]

A kép **méretét módosíthatod** a következő formátum használatával: 
`|640x480`, ahol **640** a szélesség és **480** a magasság.

```md
![[Engelbart.jpg|100x145]]
```

Ha **csak a szélességet adod meg**, a kép **az eredeti méretarány szerint skálázódik**.  
Például: `![[Engelbart.jpg|100]]`.

![[Engelbart.jpg#outline|100]]

Külső webhelyen tárolt képet **Markdown hivatkozással is beágyazhatsz**.  
A szélesség és magasság **ugyanúgy vezérelhető**, mint egy wikihivatkozás esetében.

```md
![250](https://publish-01.obsidian.md/access/f786db9fac45774fa4f0d8112e232d67/Attachments/Engelbart.jpg)
```

![250](https://publish-01.obsidian.md/access/f786db9fac45774fa4f0d8112e232d67/Attachments/Engelbart.jpg)
