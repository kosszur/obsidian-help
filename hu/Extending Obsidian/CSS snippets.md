---
aliases: 
description: Ismerd meg, hogyan módosíthatod az Obsidian alkalmazás megjelenését teljes téma létrehozása nélkül.
mobile: true
permalink: snippets
publish: true
---
Tanuld meg, hogyan módosíthatod az Obsidian alkalmazás megjelenésének bizonyos aspektusait anélkül, hogy [teljes témát kellene építened](https://docs.obsidian.md/Themes/App+themes/Build+a+theme). 

> [!tip]  
> Ha az [[Introduction to Obsidian Publish|Obsidian Publish]] CSS kezelésével kapcsolatban keresel útmutatást, feltétlenül tekintsd meg a [[Customize your site|Webhely testreszabása]] részt.

A **CSS** egy olyan nyelv, amely **meghatározza**, hogyan néz ki a **HTML**. CSS kódrészletek hozzáadásával megváltoztathatod az Obsidian **felhasználói felületének** egyes részeit, például a **címsorok méretét és színét**. Az Obsidian rendelkezik **[CSS változókkal](https://docs.obsidian.md/Reference/CSS+variables/CSS+variables)**, amelyek megkönnyítik az interfész testreszabását.

Az Obsidian a CSS kódrészleteket a tároló **[[Configuration folder|konfigurációs mappájában]]** keresi.

## Kódrészlet hozzáadása

Ha **asztali számítógépen** szeretnél **CSS kódrészletet** hozzáadni ![[lucide-monitor-check.svg#icon]], kövesd az alábbi lépéseket:

1. Nyisd meg a **Beállítások** menüt.
2. A **Megjelenés → CSS kódrészletek** alatt válaszd a **Kódrészlet mappa megnyitása** lehetőséget ( ![[lucide-folder-plus.svg#icon]] ).
3. A **kódrészlet mappában** hozz létre egy **CSS fájlt**, amely tartalmazza a módosításaidat.
4. Az Obsidianban, a **Megjelenés → CSS kódrészletek** alatt válaszd a **Kódrészletek újratöltése** ( ![[lucide-refresh-cw.svg#icon]] ) lehetőséget a kódrészletek listában való megjelenítéséhez.
5. Engedélyezd a kódrészletet a kapcsolóval.

Ha **mobilon vagy tableten** szeretnél **CSS kódrészletet** hozzáadni ![[obsidian-smartphone.svg#icon]], kövesd az alábbi lépéseket:

1. Nyiss meg egy fájlkezelőt, és keresd meg a tárolót. A tároló helyét az _Tároló kezelése…_ menüben ellenőrizheted azáltal, hogy rákkattintasz, és megnézed az elérési utat.
2. Nyisd meg a **[[Configuration folder|konfigurációs mappát]]**, és hozz létre egy `snippets` nevű mappát, ha az **nem létezik**.
3. **Helyezd el** a CSS kódrészletedet ebben a mappában.
4. Nyisd meg az Obsidian **Beállítások** menüt (![[lucide-cog.svg#icon]]).
5. **Válaszd ki** a bal oldalon a **Megjelenés** opciót.
6. Görgess le a **CSS kódrészletek** szekcióhoz.
7. **Érintsd meg** az **Újratöltés** (![[lucide-refresh-cw.svg#icon]]) lehetőséget a frissítéshez.
8. **Kapcsold be** a kódrészletet.

Alternatív megoldásként:
- [[Sync your notes across devices|Szinkronizálhatod]] a módosításokat a szinkronizálási szolgáltatásoddal.
- Használhatsz egy közösségi bővítményt, amely lehetővé teszi **kódrészletek létrehozását** közvetlenül az Obsidianban.

Miután **engedélyezted**, az Obsidian **automatikusan érzékeli a CSS módosításokat**, és alkalmazza őket, amikor **elmented a fájlt**.

> [!tip]  
> **Nem kell újraindítanod** az Obsidian alkalmazást a módosítások életbe léptetéséhez. **Előfordulhat azonban**, hogy a [[Command palette|Parancspaletta]] **Obsidian újratöltése mentés nélkül** parancsát kell használnod, hogy az aktuális témában vagy jegyzetben láthatóvá váljanak a változások.

## CSS írása az Obsidianhoz

Az Obsidian számos módszert kínál, amelyek megkönnyítik és hatékonyabbá teszik a CSS használatát.

Az Obsidian rendelkezik **[CSS változókkal](https://docs.obsidian.md/Reference/CSS+variables/CSS+variables)**, amelyekkel **egyszerűen módosíthatod** az alkalmazás különböző részeit, valamint egy beépített [[properties#Property types|tulajdonság típussal]], amely **megváltoztatja** egy vagy több jegyzet megjelenését.

> [!example] Változók  
> Hozz létre egy **`headers.css`** nevű fájlt az alábbi tartalommal, hogy a [[Basic formatting syntax#Headings|címsorok]] színei **szivárvánnyá** változzanak:
> 
> ```css
> body {
>   --h1-color: red;
>   --h2-color: orange;
>   --h3-color: yellow;
>   --h4-color: green;
>   --h5-color: blue;
>   --h6-color: pink;
> }
> ```

> [!example] CSSclasses
> Hozz létre egy [[Properties|tulajdonságot]] `cssclasses` névvel és egy **tetszőleges értékkel**, hogy **egy vagy több jegyzet eltérő megjelenésű** legyen.
> 
> **CSS**:
> ```css
> .no-inline .inline-title {
>    display: none;
> }
> ```
> 
> **YAML/Properties**:
> ```yaml
> cssclasses: no-inline
> ```
> 
> Ez elrejti **az inline címet** minden olyan jegyzetből, amely tartalmazza ezt a tulajdonságot és értéket.

A **helyes és érvényes CSS fájl létrehozásához** javasoljuk, hogy **Visual Studio Code** ([Visual Studio Code](https://visualstudio.microsoft.com/)) vagy **Sublime Text** ([Sublime Text](https://www.sublimetext.com/)) szerkesztőt használj, mivel **a hibás CSS nem fog működni**.

## További információk

- Ha **új vagy a CSS-ben**, nézd meg a **Mozilla** által készített útmutatót: [HTML stílusozás CSS segítségével](https://developer.mozilla.org/en-US/docs/Learn/CSS).
- További információk az Obsidian megjelenésének formázásáról:
  - [Stílusokról](https://docs.obsidian.md/Reference/CSS+variables/About+styling)
  - [Téma készítése](https://docs.obsidian.md/Themes/App+themes/Build+a+theme)
  - [Obsidian Publish téma készítése](https://docs.obsidian.md/Themes/Obsidian+Publish+themes/Build+a+Publish+theme)
  - [Obsidian CSS Inspector munkafolyamat](https://forum.obsidian.md/t/obsidian-css-inspector-workflow/58178)
