---
aliases:
  - How to/Use callouts
description: Ez az oldal ismerteti, hogyan használhatod a kiemelt megjegyzéseket további tartalom beillesztésére anélkül, hogy megszakítanád a jegyzeteid folyamatát.
mobile: true
publish: true
permalink: callouts
---

Használj kiemelt megjegyzéseket, hogy további tartalmat illessz be a jegyzeteidbe anélkül, hogy megszakítanád azok folyamatát.

Kiemelt megjegyzés létrehozásához adj hozzá `[!info]` címkét egy idézet első sorához, ahol `info` a _típus azonosítója_. A típus azonosító határozza meg, hogy a kiemelt megjegyzés hogyan néz ki és milyen érzetet kelt. Az összes elérhető típus megtekintéséhez lásd: [[#Supported types|Támogatott típusok]].

```markdown
> [!info]
> Ez egy kiemelt megjegyzés blokk.
> Támogatja a **Markdown**, [[Internal links|belső hivatkozásokat]] és [[Embed files|beágyazott fájlokat]]!
> ![[Engelbart.jpg]]
```

> [!info]
> Ez egy kiemelt megjegyzés blokk.
> Támogatja a **Markdown**, [[Internal links|belső hivatkozásokat]] és [[Embed files|beágyazott fájlokat]]!
> ![[Engelbart.jpg]]

A kiemelt megjegyzések natívan támogatottak az [[Introduction to Obsidian Publish|Obsidian Publish]] szolgáltatásban is.

> [!note]  
> Ha az Admonitions bővítményt is használod, frissítsd legalább 8.0.0 verzióra, hogy elkerüld az új kiemelt megjegyzés funkcióval kapcsolatos problémákat.

### Cím módosítása

Alapértelmezés szerint a kiemelt megjegyzés címe azonos a típus azonosítójával, címsor formátumban. A címet módosíthatod úgy, hogy a típus azonosító után szöveget adsz hozzá:

```markdown
> [!tip] A kiemelt megjegyzéseknek lehet egyedi címük  
> Mint ennek is.
```

> [!tip] A kiemelt megjegyzéseknek lehet egyedi címük  
> Mint ennek is.

Akár a tartalmat is elhagyhatod, hogy csak a címet jelenítsd meg:

```markdown
> [!tip] Csak címből álló kiemelt megjegyzés
```

> [!tip] Csak címből álló kiemelt megjegyzés

### Összecsukható kiemelt megjegyzések

Kiemelt megjegyzést összecsukhatóvá teheted úgy, hogy **plusz (+)** vagy **mínusz (-)** jelet adsz közvetlenül a típus azonosító után.

A **pluszjel** alapértelmezés szerint kibővíti a kiemelt megjegyzést, míg a **mínuszjel** összehajtja azt.

```markdown
> [!faq]- Összecsukhatóak a kiemelt megjegyzések?  
> Igen! Egy összecsukható kiemelt megjegyzés tartalma rejtett marad, amikor össze van hajtva.
```

> [!faq]- Összecsukhatóak a kiemelt megjegyzések?  
> Igen! Egy összecsukható kiemelt megjegyzés tartalma rejtett marad, amikor össze van hajtva.

### Egymásba ágyazott kiemelt megjegyzések

Kiemelt megjegyzéseket több szinten is egymásba ágyazhatsz.

```markdown
> [!question] Be lehet ágyazni kiemelt megjegyzéseket?  
> > [!todo] Igen, be lehet.  
> > > [!example] Akár több rétegű beágyazást is használhatsz.
```

> [!question] Be lehet ágyazni kiemelt megjegyzéseket?  
> > [!todo] Igen, be lehet.  
> > > [!example] Akár több rétegű beágyazást is használhatsz.


### Kiemelt megjegyzések testreszabása

[[CSS snippets|CSS kódrészletek]] és [[Community plugins|közösségi bővítmények]] segítségével egyedi kiemelt megjegyzéseket hozhatsz létre, vagy akár felülírhatod az alapértelmezett konfigurációt.

Egy egyedi kiemelt megjegyzés definiálásához hozz létre az alábbi CSS blokkot:

```css
.callout[data-callout="custom-question-type"] {
    --callout-color: 0, 0, 0;
    --callout-icon: lucide-alert-circle;
}
```

A `data-callout` attribútum értéke az azonosító, amelyet használni szeretnél, például `[!custom-question-type]`.

- `--callout-color` a háttérszínt határozza meg, RGB formátumban (0–255 értékekkel a piros, zöld és kék színhez).
- `--callout-icon` lehet egy ikon azonosító a [lucide.dev](https://lucide.dev) oldalról, vagy egy SVG elem.

> [!warning] Fontos tudnivaló a Lucide ikonok verzióiról  
> Az Obsidian rendszeresen frissíti a Lucide ikonokat. Az aktuálisan támogatott verzió alább látható; használd ezt vagy korábbi ikonokat az egyedi kiemelt megjegyzésekhez.  
> ![[Credits#^lucide]]

> [!tip] SVG ikonok  
> A Lucide ikonok helyett használhatsz **SVG elemet** is kiemelt megjegyzések ikonjának.
>
> ```css
> --callout-icon: '<svg>...custom svg...</svg>';
> ```

### Támogatott típusok

Többféle kiemelt megjegyzés típus és álnév érhető el. Minden típus külön háttérszínnel és ikonnal rendelkezik.

Az alapértelmezett stílusok használatához cseréld ki az `info` típust az egyik támogatott típussal, például `[!tip]` vagy `[!warning]`. A kiemelt megjegyzés típusát jobb kattintással is módosíthatod.

Hacsak nem [[#Customize callouts|testreszabod a kiemelt megjegyzéseket]], minden nem támogatott típus **alapértelmezésként** a `note` típusra vált. A típus azonosító **nem érzékeny a kis- és nagybetűkre**.

> [!note]
> ```md
> > [!note]
> > Lorem ipsum dolor sit amet
> ```

---

> [!abstract]-
> ```md
> > [!abstract]
> > Lorem ipsum dolor sit amet
> ```

Aliases: `summary`, `tldr`

---

> [!info]-
> ```md
> > [!info]
> > Lorem ipsum dolor sit amet
> ```

---

> [!todo]-
> ```md
> > [!todo]
> > Lorem ipsum dolor sit amet
> ```

---

> [!tip]-
> ```md
> > [!tip]
> > Lorem ipsum dolor sit amet
> ```

Aliases: `hint`, `important`

---

> [!success]-
> ```md
> > [!success]
> > Lorem ipsum dolor sit amet
> ```

Aliases: `check`, `done`

---

> [!question]-
> ```md
> > [!question]
> > Lorem ipsum dolor sit amet
> ```

Aliases: `help`, `faq`

---

> [!warning]-
>  ```md
> > [!warning]
> > Lorem ipsum dolor sit amet
> ```

Aliases: `caution`, `attention`

---

> [!failure]-
> ```md
> > [!failure]
> > Lorem ipsum dolor sit amet
> ```

Aliases: `fail`, `missing`

---

> [!danger]-
> ```md
> > [!danger]
> > Lorem ipsum dolor sit amet
> ```

Alias: `error`

---

> [!bug]-
> ```md
> > [!bug]
> > Lorem ipsum dolor sit amet
> ```

---

> [!example]-
> ```md
> > [!example]
> > Lorem ipsum dolor sit amet
> ```

---

> [!quote]-
> ```md
> > [!quote]
> > Lorem ipsum dolor sit amet
> ```

Alias: `cite`


