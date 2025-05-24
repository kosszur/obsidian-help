---
aliases:
  - How to/Embed files
  - Linking notes and files/Embedding files
cssclasses:
  - soft-embed
permalink: embeds
---

Tanuld meg, hogyan ágyazhatsz be más jegyzeteket és médiát a jegyzeteidbe. A fájlok beágyazásával újrahasznosíthatod a tartalmat a tárolódon belül.

Egy fájl beágyazásához a tárolódban helyezz el egy felkiáltójelet (`!`) egy [[Internal links|belső hivatkozás]] elé. Beágyazhatod a fájlokat az összes támogatott formátumban ([[Accepted file formats]]).

> [!tip] Drag and Drop beágyazás  
> Asztali számítógépen a támogatott fájlokat közvetlenül áthúzhatod a jegyzetbe, így automatikusan beágyazódnak.

## Jegyzet beágyazása egy másik jegyzetbe

Egy jegyzet beágyazásához:

```md
![[Internal links]]
```

Beágyazhatsz hivatkozásokat [[Internal links#Link to a heading in a note|címsorokhoz]] és [[Internal links#Link to a block in a note|blokkokhoz]] is.

```md
![[Internal links#^b15695]]
```

Az alábbi szöveg egy beágyazott blokk példája:

![[Internal links#^b15695]]

## Kép beágyazása egy jegyzetbe

Egy kép beágyazásához:

```md
![[Engelbart.jpg]]
```

![[Engelbart.jpg#outline]]

A kép méretét módosíthatod a következő formátum használatával: `|640x480`, ahol 640 a szélesség és 480 a magasság.

```md
![[Engelbart.jpg|100x145]]
```

Ha csak a szélességet adod meg, a kép az eredeti méretarány szerint skálázódik. Például: `![[Engelbart.jpg|100]]`.

![[Engelbart.jpg#outline|100]]

Külső webhelyen tárolt képet Markdown hivatkozással is beágyazhatsz. A szélesség és magasság ugyanúgy vezérelhető, mint egy wikihivatkozás esetében.

```md
![250](https://publish-01.obsidian.md/access/f786db9fac45774fa4f0d8112e232d67/Attachments/Engelbart.jpg)
```

![250](https://publish-01.obsidian.md/access/f786db9fac45774fa4f0d8112e232d67/Attachments/Engelbart.jpg)


## Hangfájl beágyazása egy jegyzetbe

Hangfájl beágyazásához:

```md
![[Excerpt from Mother of All Demos (1968).ogg]]
```

![[Excerpt from Mother of All Demos (1968).ogg]]

## PDF beágyazása egy jegyzetbe

PDF beágyazásához:

```md
![[Document.pdf]]
```

Egy adott oldalt is megnyithatsz a PDF-ben, ha `#page=N` értéket adsz a link céljához, ahol `N` a kívánt oldal száma:

```md
![[Document.pdf#page=3]]
```

A beágyazott PDF néző magasságát pixelben is meghatározhatod, ha `#height=[szám]` paramétert adsz a hivatkozáshoz. Például:

```md
![[Document.pdf#height=400]]
```

## Lista beágyazása egy jegyzetbe

Egy másik jegyzetből származó lista beágyazásához először adj hozzá egy [[Internal links#Hivatkozás egy blokkra egy jegyzetben|blokkazonosítót]] a listához:

```md

- list item 1
- list item 2

^my-list-id
```

Ezután hivatkozz a listára a blokkazonosító segítségével:

```md
![[My note#^my-list-id]]
```

## Keresési eredmények beágyazása

![[Search#Embed search results in a note]]
