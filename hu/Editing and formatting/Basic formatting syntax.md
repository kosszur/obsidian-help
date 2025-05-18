---
aliases:
  - Hogyan formázd a jegyzeteidet
  - Markdown
description: Tanuld meg az alapvető formázási lehetőségeket az Obsidianban Markdown használatával.
mobile: true
permalink: syntax
publish: true
---

Tanuld meg, hogyan alkalmazhatsz alapvető formázást jegyzeteidben a [Markdown](https://daringfireball.net/projects/markdown/) segítségével. Haladó formázási szintaxisért lásd: [[Advanced formatting syntax|Haladó formázási szintaxis]].

## Bekezdések

Markdownban bekezdések létrehozásához használj egy **üres sort**, amely elválasztja a szövegblokkokat. Minden üres sorral elválasztott szövegblokk különálló bekezdésként kerül értelmezésre.

```md
Ez egy bekezdés.

Ez egy másik bekezdés.
```

Ez egy bekezdés.

Ez egy másik bekezdés.

Az üres sorok használata a sorok között külön bekezdéseket hoz létre. Ez az alapértelmezett viselkedés Markdownban.

> [!tip] Több üres hely  
> A bekezdéseken belüli és közötti **több egymás melletti üres hely** egyetlen szóközzé zsugorodik, amikor megjelenik a [[Edit and preview Markdown#Editor views|Olvasási nézetben]] vagy az [[Introduction to Obsidian Publish|Obsidian Publish]] oldalakon.
> 
> ```md
> Több          egymás melletti          szóköz
> 
> 
> 
> és több új sor a bekezdések között.
> ```
> 
> 
> > Több          egymás melletti          szóköz
> > 
> > 
> > 
> > és több új sor a bekezdések között.
> 
> Ha meg szeretnéd akadályozni a szóközök összeomlását, vagy több üres helyet szeretnél beszúrni, használhatod az `&nbsp;` (nem törhető szóköz) vagy `<br>` (sorelválasztó) HTML-címkéket.

### Sorelválasztás

Az Obsidianban alapértelmezés szerint egyetlen `Enter` lenyomása új sort hoz létre a jegyzetben, de ez a *folytatásaként* kezelődik ugyanannak a bekezdésnek a megjelenítéskor, követve a Markdown szokásos viselkedését. Ha egy bekezdésen *belül* szeretnél új sort beszúrni anélkül, hogy új bekezdést kezdenél, két módon teheted meg:

- Adj hozzá **két szóközt** a sor végéhez, mielőtt megnyomod az `Enter`-t, vagy  
- Használd a **`Shift + Enter`** gyorsbillentyűt a közvetlen sorelválasztás beszúrásához.

> [!question] - Miért nem hoz létre több `Enter` lenyomás több sorelválasztást olvasási nézetben?  
> Markdownban egyetlen `Enter` lenyomása **figyelmen kívül marad**, és több egymás utáni `Enter` lenyomás csak egy új bekezdést eredményez. Ez összhangban van a Markdown **puha törésszabályával**, ahol az extra üres sorok nem generálnak további sorelválasztásokat vagy bekezdéseket – egyetlen bekezdésszétválasztásra zsugorodnak. Ez az alapértelmezett Markdown viselkedés, amely biztosítja, hogy a bekezdések természetesen folyjanak, váratlan törések nélkül.

Az Obsidian tartalmaz egy **Szabályos sorelválasztások** beállítást, amely biztosítja, hogy az alkalmazás kövesse a Markdown szabványos sorelválasztási előírásait.

A funkció engedélyezéséhez:

1. Nyisd meg a **Beállítások** menüt.
2. Lépj az **Editor** fülre.
3. Engedélyezd a **Szabályos sorelválasztások** opciót.

Ha az **Szabályos sorelválasztások** be van kapcsolva az Obsidianban, a sorelválasztás háromféle módon viselkedhet attól függően, hogyan van elválasztva a sorok:

**Egyetlen `Enter` szóköz nélkül**: Egyetlen `Enter` szóköz nélkül a két külön sor egyetlen sort képez a megjelenítés során.

```md
line one
line two
```

Megjelenítés:

sor egy sor kettő

**Egyetlen `Enter` két vagy több szóközzel**: Ha a sor végén hozzáadsz **két vagy több szóközt** az `Enter` megnyomása előtt, a két sor ugyanannak a bekezdésnek a része marad, de egy sorelválasztás (HTML `<br>` elem) megszakítja őket. Ebben a példában két aláhúzás jelet használunk a szóközök helyettesítésére.

```md
sor három__  
sor négy
```

Renders as:

sor három<br>
sor négy

**Kettős `Enter` (szóközzel vagy anélkül)**: Ha **kétszer vagy többször megnyomod az `Enter`-t**, a sorok különálló bekezdésekké válnak (HTML `<p>` elemek), függetlenül attól, hogy a sor végén hozzáadtál-e szóközt.

```md
sor öt

sor hat
```

Megjelenítés:

<p>sor öt</p>
<p>sor hat</p>

## Címsorok

Címsor létrehozásához adj hozzá legfeljebb hat `#` jelet a címsor szövege elé. A `#` jelek száma határozza meg a címsor méretét.

```md
# Ez egy 1-es szintű címsor
## Ez egy 2-es szintű címsor
### Ez egy 3-as szintű címsor
#### Ez egy 4-es szintű címsor
##### Ez egy 5-ös szintű címsor
###### Ez egy 6-os szintű címsor
```

%% Ezek a címsorok HTML-t használnak, hogy elkerüljék a Vázlat/Tartalomjegyzék zsúfoltságát %%
<h1>Ez egy 1-es szintű címsor</h1>
<h2>Ez egy 2-es szintű címsor</h2>
<h3>Ez egy 3-as szintű címsor</h3>
<h4>Ez egy 4-es szintű címsor</h4>
<h5>Ez egy 5-ös szintű címsor</h5>
<h6>Ez egy 6-os szintű címsor</h6>

## Félkövér, dőlt, kiemelt szöveg

Szövegformázást alkalmazhatsz a [[Editing shortcuts|szerkesztési gyorsbillentyűkkel]] is.

| Stílus | Szintaxis | Példa | Kimenet |
|-|-|-|-|
| Félkövér | `** **` vagy `__ __` | `**Félkövér szöveg**` | **Félkövér szöveg** |
| Dőlt | `* *` vagy `_ _`  | `*Dőlt szöveg*` | *Dőlt szöveg* |
| Áthúzott | `~~ ~~` |  `~~Áthúzott szöveg~~` | ~~Áthúzott szöveg~~ |
| Kiemelt | `== ==` |  `==Kiemelt szöveg==` | ==Kiemelt szöveg== |
| Félkövér és beágyazott dőlt | `** **` és `_ _`  | `**Félkövér szöveg és _beágyazott dőlt_ szöveg**` | **Félkövér szöveg és _beágyazott dőlt_ szöveg** |
| Félkövér és dőlt | `*** ***` vagy `___ ___` |  `***Félkövér és dőlt szöveg***` | ***Félkövér és dőlt szöveg*** |

Formázást kényszeríthetsz sima szövegként való megjelenítésre egy fordított perjel (`\`) hozzáadásával előtte.

\*\*Ez a sor nem lesz félkövér\*\*

```markdown
\*\*Ez a sor nem lesz félkövér\*\*
```

\**Ez a sor dőlt lesz, és mutatni fogja a csillagokat*\*

```markdown
\**Ez a sor dőlt lesz, és mutatni fogja a csillagokat*\*
```


## Belső hivatkozások

Az Obsidian két formátumot támogat a [[internal links|belső hivatkozásokhoz]] jegyzetek között:

- Wikihivatkozás: `[[Három mozgástörvény]]`
- Markdown: `[Három mozgástörvény](Három%20mozgástörvény.md)`

## Külső hivatkozások

Ha egy külső URL-re szeretnél hivatkozni, létrehozhatsz egy inline hivatkozást a hivatkozás szövegét szögletes zárójelek (`[ ]`) közé helyezve, majd az URL-t kerek zárójelek (`( )`) közé téve.

```md
[Obsidian Súgó](https://help.obsidian.md)
```

[Obsidian Súgó](https://help.obsidian.md)

Külső hivatkozásokat más tárolókban lévő fájlokra is létrehozhatsz az [[Obsidian URI|Obsidian URI]] segítségével.

```md
[Note](obsidian://open?vault=MainVault&file=Note.md)
```

### Üres helyek kezelése hivatkozásokban

Ha az URL-ed üres helyeket tartalmaz, **ki kell cserélned őket** `%20` karakterekre.

```md
[My Note](obsidian://open?vault=MainVault&file=My%20Note.md)
```

Az URL-t szögletes zárójelek (`< >`) közé is helyezheted az elkerülés érdekében.

```md
[My Note](<obsidian://open?vault=MainVault&file=My Note.md>)
```

## Külső képek

Külső URL-ekkel rendelkező képeket adhatsz hozzá úgy, hogy egy `!` jelet helyezel a [[#External links|külső hivatkozás]] elé.

```md
![Engelbart](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)
```

![Engelbart](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)

A képek méretét megváltoztathatod úgy, hogy a link végéhez hozzáadod a `|640x480` formátumot, ahol **640** a szélesség, **480** pedig a magasság.

```md
![Engelbart|100x145](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)
```

Ha csak a szélességet adod meg, a kép az eredeti képarány szerint méreteződik. Például:

```md
![Engelbart|100](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)
```

> [!tip]  
> Ha egy tárolón belüli képet szeretnél hozzáadni, akkor [[Embed files#Embed an image in a note|beágyazhatod a képet egy jegyzetbe]].

## Idézetek

Szöveget idézhetsz úgy, hogy egy `>` jelet teszel a szöveg elé.

```md
> Human beings face ever more complex and urgent problems, and their effectiveness in dealing with these problems is a matter that is critical to the stability and continued progress of society.

\- Doug Engelbart, 1961
```

> Human beings face ever more complex and urgent problems, and their effectiveness in dealing with these problems is a matter that is critical to the stability and continued progress of society.

\- Doug Engelbart, 1961

> [!tip]  
> Az idézetet [[Callouts|kiemelt megjegyzéssé]] alakíthatod úgy, hogy az első sorba `[!info]` jelölést helyezel.

## Listák

Felsorolásos listát hozhatsz létre úgy, hogy egy `-`, `*` vagy `+` jelet írsz a szöveg elé.

```md
- Első listaelem
- Második listaelem
- Harmadik listaelem
```

- Első listaelem
- Második listaelem
- Harmadik listaelem

Számozott lista létrehozásához minden sor elején számot kell megadnod, amelyet egy `.` vagy `)` jel követ.

```md
1. Első listaelem
2. Második listaelem
3. Harmadik listaelem
```

1. Első listaelem
2. Második listaelem
3. Harmadik listaelem

```md
1) Első listaelem
2) Második listaelem
3) Harmadik listaelem
```

1) Első listaelem
2) Második listaelem
3) Harmadik listaelem

Használhatod a `Shift + Enter` kombinációt egy [[#Line breaks|sorelválasztás]] beszúrásához egy számozott listán belül anélkül, hogy a számozást megváltoztatnád.

```md
1. First list item
   
2. Second list item
3. Third list item
   
4. Fourth list item
5. Fifth list item
6. Sixth list item
```

### Feladatlisták

Feladatlista létrehozásához kezdd minden listaelemet kötőjellel és szóközzel, amelyet `[ ]` követ.

```md
- [x] Ez egy befejezett feladat.
- [ ] Ez egy befejezetlen feladat.
```

- [x] Ez egy befejezett feladat.
- [ ] Ez egy befejezetlen feladat.

Az Olvasási nézetben a jelölőnégyzet kiválasztásával válthatsz a feladat állapotán.

> [!tip]  
> Bármilyen karaktert használhatsz a négyzetben, hogy megjelöld a feladatot teljesítettként.
>
> ```md
> - [x] Tej
> - [?] Tojás
> - [-] Tojás
> ```
>
> - [x] Tej
> - [?] Tojás
> - [-] Tojás

### Listák egymásba ágyazása

Bármilyen listát—számozott, felsorolásos vagy feladatlistát—beágyazhatsz másik lista alá.

Egymásba ágyazott lista létrehozásához behúzhatsz egy vagy több listaelemet. A listatípusokat keverheted az egymásba ágyazott szerkezetben:

```md
1. Első listaelem
   1. Számozott allistaelem
2. Második listaelem
   - Felsorolásos allistaelem
```

1. Első listaelem
   1. Számozott allistaelem
2. Második listaelem
   - Felsorolásos allistaelem

Hasonlóképpen, feladatlistát is ágyazhatsz be úgy, hogy behúzol egy vagy több listaelemet:

```md
- [ ] Feladat 1
	- [ ] Alfeladat 1
- [ ] Feladat 2
	- [ ] Alfeladat 1
```

- [ ] Feladat 1
	- [ ] Alfeladat 1
- [ ] Feladat 2
	- [ ] Alfeladat 1

Használd a `Tab` vagy `Shift + Tab` billentyűkombinációt a kijelölt listaelemek behúzásához vagy visszahúzásához, hogy könnyen rendszerezd őket.


## Vízszintes vonal

Három vagy több csillag `***`, kötőjel `---` vagy aláhúzás `___` egy külön sorban vízszintes vonalat hoz létre. A szimbólumokat szóközökkel is elválaszthatod.

```md
***
****
* * *
---
----
- - -
___
____
_ _ _
```

***

## Kód

A kódot formázhatod mondaton belül inline módban, vagy különálló blokkban.

### Inline kód

A kódot egy mondaton belül egyetlen backtick jel használatával formázhatod.

```md
Text inside `backticks` on a line will be formatted like code.
```

A `backtickek` között lévő szöveg kódként lesz formázva.

Ha backtick jelet szeretnél elhelyezni egy inline kódblokkon belül, dupla backtickekkel vesd körül, például: inline ``kód egy backtick ` karakterrel belül``.


### Kódrészletek

Kódszöveg formázásához blokk formában helyezd három backtick vagy három hullámvonal (`~~~`) közé.

~~~
```
cd ~/Desktop
```
~~~

```
~~~
cd ~/Desktop
~~~
```

```md
cd ~/Desktop
```

Kódrészletet úgy is létrehozhatsz, hogy a szöveget `Tab` vagy **4 üres hely** segítségével behúzod.

```md
    cd ~/Desktop
```

Szintaxis kiemelést adhatsz a kódrészlethez, ha az első backtick sor után megadod a programozási nyelv kódját.

~~~md
```js
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```
~~~

```js
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```

Az Obsidian a Prism-et használja szintaxis kiemeléshez. További információért lásd: [Támogatott nyelvek](https://prismjs.com/#supported-languages).

> [!note]  
> A [[Edit and preview Markdown#Source mode|Forrás mód]] és a [[Edit and preview Markdown#Live Preview|Élő előnézet]] nem támogatja a PrismJS-t, ezért eltérően jelenítheti meg a szintaxis kiemelést.


## Lábjegyzetek

Lábjegyzeteket[^footnote] adhatsz hozzá jegyzeteidhez az alábbi szintaxis használatával:

[^footnote]: Ez egy lábjegyzet.

```md
Ez egy egyszerű lábjegyzet[^1].

[^1]: Ez a hivatkozott szöveg.
[^2]: Adj hozzá 2 szóközt minden új sor elejéhez.  
  Ez lehetővé teszi, hogy több soron átívelő lábjegyzeteket írj.
[^note]: A megnevezett lábjegyzetek számként jelennek meg, de megkönnyítik a hivatkozások azonosítását.
```

Lábjegyzetet beszúrhatsz inline módon is egy mondatba. Fontos, hogy a `^` jel **a szögletes zárójelek** kívül legyen.

```md
Inline lábjegyzeteket is használhatsz. ^[Ez egy inline lábjegyzet.]
```

> [!note]  
> Az inline lábjegyzetek **csak olvasási nézetben működnek**, élő előnézetben nem.

## Megjegyzések

Megjegyzéseket adhatsz hozzá úgy, hogy a szöveget `%%` jelek közé zárod. A megjegyzések **csak szerkesztési nézetben** láthatók.

```md
Ez egy %%inline%% megjegyzés.

%%
Ez egy blokk megjegyzés.

A blokk megjegyzések több soron átívelhetnek.
%%
```

## Markdown szintaxis elkerülése

Bizonyos esetekben előfordulhat, hogy **speciális karaktereket** szeretnél megjeleníteni Markdownban, például `*`, `_` vagy `#`, anélkül, hogy azok formázást aktiválnának. Ezeket a karaktereket **szó szerint** jelenítheted meg, ha egy fordított perjelet (`\`) írsz eléjük.

> [!example] Gyakori karakterek, amelyeket el kell kerülni  
> 
> - Csillag: `\*`
> - Aláhúzás: `\_`
> - Hashtag: `\#`
> - Backtick: `` \` ``
> - Függőleges vonal (táblázatokban használva): `\|`
> - Tilde: `\~`

```md
\*Ez a szöveg nem lesz dőlt\*.
```

\*Ez a szöveg nem lesz dőlt\*.

Számozott listák használata közben előfordulhat, hogy **el kell kerülni a pontot** a szám után, hogy megakadályozd az automatikus listaformázást. Ebben az esetben a **pont elé**, **nem a szám elé** kell helyezned a fordított perjelet (`\`).

```md
1\. Ez nem lesz listaelem.
```

1\. Ez nem lesz listaelem.

## További tudnivalók

Ha többet szeretnél megtudni a haladó formázási szintaxisokról, például táblázatokról, diagramokról vagy matematikai kifejezésekről, lásd: [[Advanced formatting syntax|Haladó formázási szintaxis]].

Ha többet szeretnél megtudni arról, hogyan dolgozza fel az Obsidian a Markdown-t, lásd: [[Obsidian Flavored Markdown|Obsidian által támogatott Markdown]].
