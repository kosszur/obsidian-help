---
permalink: obsidian-flavored-markdown
---
Az Obsidian maximális funkcionalitásra törekszik anélkül, hogy megtörné a meglévő formátumokat. Ennek eredményeként a [[Basic formatting syntax|Markdown]] különböző változatait kombináljuk.

Az Obsidian támogatja a [CommonMark](https://commonmark.org/), [GitHub Flavored Markdown](https://github.github.com/gfm/) és [LaTeX](https://www.latex-project.org/) formátumokat. Az Obsidian **nem támogatja** a Markdown formázás vagy üres sorok használatát **HTML címkék belsejében**.

### Támogatott Markdown kiegészítések

| Szintaxis       | Leírás                                                                |
| --------------- | --------------------------------------------------------------------- |
| `[[Hivatkozás]]` | [[Internal links|Belső hivatkozások]]                               |
| `![[Hivatkozás]]` | [[Embed files|Beágyazott fájlok]]                                   |
| `![[Hivatkozás#^id]]` | [[Internal links#Link to a block in a note|Blokk hivatkozások]] |
| `^id` | [[Internal links#Link to a block in a note|Blokk meghatározás]]                 |
| `[^id]` | [[Basic formatting syntax#Footnotes|Lábjegyzetek]]                            |
| `%%Szöveg%%` | [[Basic formatting syntax#Comments|Megjegyzések]]                       |
| `~~Szöveg~~` | [[Basic formatting syntax#Bold, italics, highlights|Áthúzott szöveg]]   |
| `==Szöveg==` | [[Basic formatting syntax#Bold, italics, highlights|Kiemelt szöveg]]    |
| `` ``` `` | [[Basic formatting syntax#Code blocks|Kódrészletek]]                        |
| `- [ ]` | [[Basic formatting syntax#Task lists|Nem teljesített feladat]]               |
| `- [x]` | [[Basic formatting syntax#Task lists|Teljesített feladat]]                    |
| `> [!note]` | [[Callouts|Kiemelt megjegyzések]]                                        |
| (lásd a hivatkozást) | [[Advanced formatting syntax#Tables|Táblázatok]]                |

