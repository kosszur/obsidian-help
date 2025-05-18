---
aliases:
  - front matter
  - Advanced topics/YAML front matter
  - metadata
  - property
cssclasses:
  - soft-embed
permalink: properties
---
A tulajdonságok lehetővé teszik, hogy rendszerezd a jegyzetekkel kapcsolatos információkat. A tulajdonságok **strukturált adatokat** tartalmaznak, például szöveget, hivatkozásokat, dátumokat, jelölőnégyzeteket és számokat. A tulajdonságokat [[Community plugins|közösségi bővítményekkel]] is kombinálhatod, amelyek különböző funkciókat kínálnak a strukturált adatokkal.

## Tulajdonság hozzáadása egy jegyzethez

Többféleképpen adhatsz hozzá tulajdonságot egy jegyzethez:

- Használhatod a **Fájltulajdonság hozzáadása** [[Command palette|parancsot]].
- Használhatod a **`Cmd/Ctrl+;`** [[Hotkeys|gyorsbillentyűt]].
- Válaszd a **Fájltulajdonság hozzáadása** lehetőséget a **További műveletek** menüben (hárompontos ikon vagy jobb kattintás a lapon).
- Írd be a `---` karaktereket **a fájl legelső sorába**.

Miután hozzáadtál egy tulajdonságot, a fájl tetején megjelenik egy **sor**, amely két mezőt tartalmaz: a tulajdonság _nevét_ és _értékét_.

A név bármi lehet, amit választasz. Az Obsidian **néhány alapértelmezett tulajdonságot** biztosít: `tags`, `cssclasses` és `aliases`.

Miután megadtad a tulajdonság nevét, hozzárendelhetsz egy értéket.

### Tulajdonságtípusok

A **név és érték** mellett a tulajdonságoknak van egy *típusa* is. A tulajdonság típusa meghatározza, milyen értékeket tárolhat. A tulajdonság típusát **módosíthatod**, ha rákattintasz az ikonra, vagy használod az **Fájltulajdonság szerkesztése** parancsot.

Az Obsidian a következő tulajdonságtípusokat támogatja:

- **[[#^text-list|Szöveg]]**
- **[[#^text-list|Lista]]**
- **[[#^numbers|Szám]]**
- **[[#^checkbox|Jelölőnégyzet]]**
- **[[#^date-time|Dátum]]**
- **[[#^date-time|Dátum és idő]]**

Miután egy **tulajdonságtípus** hozzá lett rendelve egy tulajdonsághoz, az összes **azonos névvel rendelkező tulajdonság** ugyanezt a típust fogja használni.

## Haladó használat

### Hivatkozások

A **Szöveg** és **Lista** típusú tulajdonságok tartalmazhatnak URL-eket és [[Internal links|belső hivatkozásokat]] a `[[Hivatkozás]]` szintaxis használatával.

### Tulajdonságok keresése

A tulajdonságoknak saját [[Search|keresési szintaxisa]] van, amelyet más keresési kifejezésekkel és operátorokkal együtt használhatsz. [[Search#Search properties|Lásd a tulajdonságok keresési szintaxisát]].

### Sablonok

Tulajdonságokat adhatsz hozzá [[Plugins/Templates|sablonokhoz]]. Amikor **egy sablont beszúrsz** az aktív jegyzetbe, az összes **tulajdonság a sablonból** hozzáadódik a jegyzethez. Az Obsidian összevonja a **jegyzetben lévő meglévő tulajdonságokat** a sablon tulajdonságaival.

### Tulajdonságok átnevezése

Egy tulajdonságot átnevezhetsz, ha jobb kattintással kiválasztod a [[Properties view|Minden tulajdonság nézetben]].

### Megjelenítési módok

Módosíthatod, hogyan jelenjenek meg a tulajdonságok a jegyzetedben a **Beállítások → Szerkesztő → Tulajdonságok a dokumentumban** menüben. A lehetőségek:

- **Látható** (alapértelmezett) — megjeleníti a tulajdonságokat a jegyzet tetején, ha vannak.
- **Rejtett** — elrejti a tulajdonságokat, de továbbra is megjeleníthető a **oldalsávban** a [[Properties view|Tulajdonságok nézetben]].
- **Forrás** — megjeleníti a tulajdonságokat egyszerű szöveges YAML formátumban.

### CSS kódrészletek

Használhatsz [[CSS snippets|CSS kódrészleteket]] a jegyzetek **megjelenésének módosítására**.

### Nem támogatott funkciók

Az Obsidian **nem támogatja** az alábbi funkciókat:

- **Egymásba ágyazott tulajdonságok** — megtekintésükhöz ajánlott a **Forrás mód** használata.
- **Tömeges tulajdonság szerkesztés** — ez megoldható tömeges szerkesztő eszközökkel, például **VSCode, szkriptek és közösségi bővítmények** segítségével.
- **Markdown tulajdonságokban** — ez egy **szándékos korlátozás**, mivel a tulajdonságok **kis, önálló információdarabok**, amelyek **ember és gép** számára is olvashatóak.

## Gyorsbillentyűk

### Tulajdonság hozzáadása

| Művelet | Gyorsbillentyű |
|---|---|
|Új tulajdonság hozzáadása|`Cmd + ;`|

### Tulajdonságok közti navigáció

Amikor egy tulajdonság van fókuszban

| Művelet | Gyorsbillentyű |
|---|---|
|Fókusz áthelyezése a következő tulajdonságra|`Le nyíl` vagy `Tab`|
|Fókusz áthelyezése az előző tulajdonságra|`Fel nyíl` vagy `Shift+Tab`|
|Ugrás a szerkesztőbe|`Alt+Le nyíl`|

### Tulajdonságok kijelölése

| Művelet | Gyorsbillentyű |
|---|---|
|Kijelölés kiterjesztése felfelé|`Shift+Fel nyíl`|
|Kijelölés kiterjesztése lefelé|`Shift+Le nyíl`|
|Összes kijelölése|`Cmd+A`|

### Tulajdonságok szerkesztése

| Művelet | Gyorsbillentyű |
|---|---|
|Tulajdonság név szerkesztése|`Balra nyíl`|
|Tulajdonság érték szerkesztése|`Jobbra nyíl`|
|Tulajdonság fókuszálása|`Escape`|
|Tulajdonság törlése|`Cmd+Backspace`<br><br>Ha több tulajdonság van kijelölve, akkor az egész kijelölés törlődik.|
|Visszavonás|`Cmd+Z`|
|Újra végrehajtás|`Cmd+Shift+Z`|

### Vim (haladó)

| Művelet | Gyorsbillentyű |
|---|---|
|Lejjebb lépés|`j`|
|Feljebb lépés|`k`|
|Fókusz kulcsra|`h`|
|Fókusz értékre|`l`|
|Fókusz értékre (kurzor a végén)|`A`|
|Fókusz értékre (kurzor az elején)|`i`|
|Új tulajdonság létrehozása|`o`|

## Tulajdonságformátum

A tulajdonságok a fájl tetején **[YAML](https://yaml.org/) formátumban** vannak tárolva. A YAML egy népszerű formátum, amelyet **emberek és gépek** számára is könnyű olvasni.

A tulajdonságok **nevei** és **értékei** kettősponttal és egy szóközzel vannak elválasztva:

```yaml
---
name: value
---
```

Bár **az egyes név-érték párok sorrendje nem számít**, minden név **egyedi** kell legyen egy jegyzeten belül. Például nem lehet **több `tags` tulajdonság** egy jegyzetben.

Az értékek lehetnek szövegek, számok, **true** vagy **false**, illetve **több értéket tartalmazó gyűjtemények** (tömbök).
^text-list

```yaml
---
title: A New Hope # This is a text property
year: 1977
favorite: true
cast: # This is a list property
  - Mark Hamill
  - Harrison Ford
  - Carrie Fisher
---
```

A **Szöveg** és **Lista** típusú tulajdonságokban lévő **belső hivatkozások** idézőjelek között kell legyenek. Az Obsidian **automatikusan hozzáadja ezeket**, ha **kézzel írsz** be belső hivatkozásokat tulajdonságként, de **figyelj rájuk**, ha sablon bővítményeket használsz.

```yaml
---
link: "[[Link]]" 
linklist: 
  - "[[Link]]" 
  - "[[Link2]]"
---
```

A **Szám** típusú tulajdonságoknak mindig **konkrét számnak** kell lenniük, **nem matematikai kifejezésnek** operátorokkal. Egész számok és tizedes törtek **egaránt megengedettek**.
^numbers

```yaml
---
year: 1977
pie: 3.14
---
```

A **Jelölőnégyzet** típusú tulajdonságok értékei `true` vagy `false` lehetnek. **Ha egy tulajdonság üres**, az **automatikusan `false` értékű** lesz. Az **Élő előnézetben** ez egy **jelölőnégyzetként jelenik meg**.
^checkbox

```yaml
---
favorite: true
reply: false
last: # this will default to false
```


A **Dátum** és **Dátum & Idő** típusú tulajdonságok **az alábbi formátumban** vannak tárolva:
^date-time

```yaml
---
date: 2020-08-21
time: 2020-08-21T10:30:00
---
```

A dátumválasztó **követi az operációs rendszered alapértelmezett dátum és idő formátumát**. **Rendszerbeállításokban** módosíthatod:

> [!info]- Windows
> **Settings → Time & Language → Language & Region → Regional Format → Change Formats**
> **Beállítások → Idő és nyelv → Nyelv és régió → Regionális formátum → Formátumok módosítása**  
> 
> ![[Windows-OS-DateTime.png#interface]]

> [!info]- Mac OS
> **System Preferences → Language and Region → Date format**
> **Rendszerbeállítások → Nyelv és régió → Dátumformátum**  
> 
> ![[Mac-OS-DateTime.png|450]]

Ha a **[[Daily notes]]** bővítmény **be van kapcsolva**, a **dátum tulajdonság** automatikusan belső hivatkozásként fog **működni** az adott napi jegyzethez.

![[Daily notes#^daily-notes-date]]

### JSON tulajdonságok

Bár **ajánlott a YAML használata** a tulajdonságok meghatározására, [JSON](https://www.json.org/) formátumot is használhatsz:  

```json
---
{
  "tags": "journal",
  "publish": false
}
---
```

A JSON blokkot az Obsidian **beolvassa, értelmezi és YAML formátumban** menti.
## Alapértelmezett tulajdonságok

Az Obsidian alapértelmezés szerint az alábbi tulajdonságokat biztosítja:

| Tulajdonság | Leírás |
|-|-|
| `tags` | Lásd: [[Editing and formatting/Tags\|Címkék]]. |
| `aliases` | Lásd: [[Aliases\|Álnévek]]. |
| `cssclasses` | Lehetővé teszi az egyedi jegyzetek stílusát [[CSS snippets\|CSS kódrészletekkel]]. |

### Tulajdonságok az Obsidian Publishhez

Az alábbi tulajdonságok használhatók [[Introduction to Obsidian Publish\|Obsidian Publish]] szolgáltatással:

| Tulajdonság      | Leírás                                                                                                       |
| ------------- | ----------------------------------------------------------------------------------------------------------------- |
| `publish`     | Lásd: [[Publish your content#Automatically select notes to publish\|Automatikusan publikálandó jegyzetek kiválasztása]]. |
| `permalink`   | Lásd: [[Permalinks\|Permalinkek]].                                                                                   |
| `description` | Lásd: [[Social media link previews#Description\|Leírás]].                                                      |
| `image`       | Lásd: [[Social media link previews#Image\|Kép]].                                                                  |
| `cover`       | Lásd: [[Social media link previews#Image\|Borítókép]].                                                                  |

### Elavult tulajdonságok

Ezek a tulajdonságok elavultak az Obsidian 1.4 verziójától kezdve. **Ne használd őket többé**:

| Tulajdonság | Leírás |
|-|-|
| `tag` | Elavult alias a `tags` tulajdonság helyett. |
| `alias` | Elavult alias az `aliases` tulajdonság helyett. |
| `cssclass` | Elavult alias a `cssclasses` tulajdonság helyett. |
