---
aliases:
  - Advanced topics/HTML sanitization
  - Editing and formatting/Using HTML
---
Az Obsidian támogatja a HTML-t, hogy jegyzeteid megjelenítését testre szabhassad, vagy akár [[Embed web pages|weboldalakat ágyazhass be]]. A HTML engedélyezése jegyzeteidben **bizonyos kockázatokkal** járhat. Annak érdekében, hogy a **káros kódok ne okozhassanak problémát**, az Obsidian _tisztítja_ az jegyzeteidben található HTML-t.  

> [!example]  
> A `<script>` elem normál esetben lehetővé teszi JavaScript futtatását **betöltéskor**. Ha az Obsidian **nem tisztítaná a HTML-t**, egy támadó rávehetne arra, hogy olyan szöveget illessz be, amely **érzékeny információkat** gyűjt össze a gépedről, majd visszaküldi neki.

Mivel a Markdown szintaxis **nem támogat** minden formázási lehetőséget, a tisztított HTML használata egy további eszköz lehet a jegyzeteid minőségének javítására. Itt van néhány gyakori HTML használati példa.  

> [!info]  
> További részletek a `<iframe>` elem használatáról a [[Embed web pages|Weboldalak beágyazása]] című részben találhatók.

### Megjegyzések

A [[Basic formatting syntax#Comments|Markdown megjegyzések]] az **ajánlott módja** a jegyzeteiden belüli **rejtett megjegyzések** hozzáadásának. Azonban bizonyos Markdown-feldolgozási módszerek, például a [Pandoc](https://pandoc.org), **korlátozottan támogatják** a Markdown megjegyzéseket. Ilyen esetekben használhatod a következő HTML formátumot: `<!-- HTML Megjegyzés -->`.

### Aláhúzás

Ha gyorsan szeretnél **aláhúzni** egy elemet jegyzeteidben, használhatod `<u>Példa</u>` formátumban, ami így jelenik meg: <u>aláhúzott szöveg</u>.

### Span/Div

A **Span** és **Div** HTML címkék segítségével egyéni osztályokat alkalmazhatsz egy **[[CSS snippets|CSS kódrészletből]]**, vagy egyedi **meghatározott stílust** egy kijelölt szövegre. Például, `<span style="font-family: cursive">szöveged</span>` segítségével könnyedén <span style="font-family: cursive">megváltoztathatod a betűtípust</span>.

## Áthúzás

Szükséged van áthúzott <s>szövegre</s>? Használj `<s>ez</s>` formátumot az áthúzáshoz.
