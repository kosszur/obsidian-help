---
aliases:
  - Using Obsidian URI
  - Advanced topics/Using obsidian URI
  - Concepts/Obsidian URI
---
Obsidian URI egy egyedi URI protokoll, amelyet az Obsidian támogat, és lehetővé teszi különböző műveletek végrehajtását, például jegyzetek megnyitását vagy létrehozását. Az Obsidian URI lehetőséget nyújt az automatizálásra és az alkalmazások közötti munkafolyamatokra.

## URI formátuma

Az Obsidian URI-k a következő formátumot használják:

```
obsidian://action?param1=value&param2=value
```

Az `action` paraméter a végrehajtani kívánt műveletet határozza meg. Az elérhető műveletek:

- `open` — jegyzet megnyitása.
- `new` — új jegyzet létrehozása vagy meglévő bővítése.
- `daily` — napi jegyzet létrehozása vagy megnyitása.
- `search` — keresés megnyitása.

> [!warning] Kódolás  
> Győződj meg róla, hogy az értékeid megfelelően URI-kódoltak. Például **a `/` karaktert `%2F`-ként kell kódolni**, és **a szóközt `%20`-ként**.
> 
> Ez különösen fontos, mert **egy nem megfelelően kódolt "fenntartott" karakter** megtörheti az URI értelmezését. [További részletek itt](https://en.wikipedia.org/wiki/Percent-encoding).

## Jegyzet megnyitása

Az `open` művelet egy **Obsidian tárolót** nyit meg, vagy egy **fájlt** annak a tárolónak belsejében.

### Példák

- `obsidian://open?vault=my%20vault`  
  Megnyitja a `my vault` nevű tárolót. Ha a tároló már nyitva van, az ablak fókuszba kerül.
- `obsidian://open?vault=ef6ca3e3b524d22f`  
  Megnyitja az `ef6ca3e3b524d22f` azonosítóval ellátott tárolót.
- `obsidian://open?vault=my%20vault&file=my%20note`  
  Megnyitja a `my vault` tárolóban lévő `my note.md` fájlt, **ha az létezik**.
- `obsidian://open?path=%2Fhome%2Fuser%2Fmy%20vault%2Fpath%2Fto%2Fmy%20note`  
  Az Obsidian ellenőrzi, **hogy létezik-e egy olyan tároló**, amely tartalmazza ezt az **elérési utat**: `/home/user/my vault/path/to/my note`. Ezután **az elérési út hátralévő részét** az `file` paraméterként kezeli. Például ha van egy tároló a `/home/user/my vault` helyen, akkor ez ekvivalens lenne azzal, hogy **az `file` paraméter `path/to/my note` értéket kap**.

> [!tip] Ugrás címsorra vagy blokkra  
> Megfelelő URI kódolással **ugorhatsz egy címsorra vagy blokkra** a jegyzeten belül.  
> `Note%23Heading` egy **"Heading" nevű címsorra** navigál, míg  
> `Note%23%5EBlock` egy **"Block" nevű blokkra**.

### Paraméterek

- `vault` lehet a tároló neve vagy annak azonosítója[^1].
- `file` lehet fájlnév vagy a tároló gyökérkönyvtárától számított elérési út. Ha a fájl kiterjesztése `md`, akkor a kiterjesztés elhagyható.
- `path` egy abszolút fájlrendszer útvonal egy fájlhoz.
  - Ennek a paraméternek a használata **felülírja** a `vault` és `file` paramétereket.
  - Az alkalmazás megkeresi a **legpontosabb tárolót**, amely tartalmazza az adott fájlútvonalat.
  - Ezután az útvonal hátralévő része **a `file` paraméter lesz**.
- `prepend` a fájl tetejére adja hozzá a tartalmat, és megpróbálja összevonni a tulajdonságokat.
- `append` a fájl végéhez adja hozzá a tartalmat, és szintén megpróbálja összevonni a tulajdonságokat.

## Jegyzet létrehozása

A `new` művelet egy **új jegyzetet** hoz létre a tárolóban, opcionálisan bizonyos tartalommal.

### Példák

- `obsidian://new?vault=my%20vault&name=my%20note`  
  Megnyitja a `my vault` tárolót, és létrehozza a `my note` nevű jegyzetet.
- `obsidian://new?vault=my%20vault&path=path%2Fto%2Fmy%20note`  
  Megnyitja a `my vault` tárolót, és létrehozza a jegyzetet ezen az útvonalon: `path/to/my note`.

### Paraméterek

- `vault` lehet a tároló neve vagy annak azonosítója[^1]. Ugyanaz, mint az `open` műveletnél.
- `name` a létrehozandó fájl neve. Ha meg van adva, a fájl helyét a **"Új jegyzetek alapértelmezett helye"** beállítás határozza meg.
- `file` a tárolón belüli abszolút fájlútvonal, beleértve a nevet. Ha meg van adva, **felülírja** a `name` paramétert.
- `path` egy globális abszolút fájlútvonal. **Ugyanúgy működik**, mint az `open` művelet `path` paramétere, és **felülírja** a `vault` és `file` paramétereket.
- `content` (opcionális) a jegyzet tartalma.
- `clipboard` (opcionális) a vágólap tartalmának használata a `content` helyett.
- `silent` (opcionális) ha ezt a paramétert beállítod, az **új jegyzet nem nyílik meg** automatikusan.
- `append` (opcionális) ha a fájl létezik, hozzáfűzi az új tartalmat.
- `overwrite` (opcionális) **felülírja a meglévő fájlt**, de csak **ha az `append` nincs beállítva**.
- `x-success` (opcionális) lásd: [[#Use x-callback-url parameters]].

## Napi jegyzet létrehozása vagy megnyitása

A `daily` művelet létrehozza vagy megnyitja a napi jegyzetedet. Ehhez a [[Daily notes|Napi jegyzetek]] bővítményt engedélyezni kell.

### Példák

- `obsidian://daily?vault=my%20vault`  
  Megnyitja a `my vault` tárolót, és létrehozza vagy megnyitja a napi jegyzetet.

### Paraméterek

A `daily` művelet **ugyanazokat a paramétereket** fogadja el, mint a `new` művelet.

## Keresés megnyitása

A `search` művelet megnyitja a [[Search|Keresés]] funkciót az adott tárolóban, és opcionálisan végrehajtja a keresési kifejezést.

### Példák

- `obsidian://search?vault=my%20vault`  
  Megnyitja a `my vault` tárolót, és **elindítja** a [[Search|Keresést]].
- `obsidian://search?vault=my%20vault&query=Obsidian`  
  Megnyitja a `my vault` tárolót, elindítja a [[Search|Keresést]], és végrehajtja a `Obsidian` keresést.

### Paraméterek

- `vault` lehet a tároló neve vagy azonosítója[^1]. Ugyanaz, mint az `open` műveletnél.
- `query` (opcionális) A végrehajtandó keresési kifejezés.

## Integráció a Hookkal

Ez az Obsidian URI művelet a [Hook](https://hookproductivity.com/) szolgáltatáshoz készült.

### Példa

`obsidian://hook-get-address`

### Paraméterek

- `vault` (opcionális) lehet a tároló neve vagy azonosítója[^1]. Ha nincs megadva, az aktuális vagy utoljára fókuszált tárolót használja.
- `x-success` (opcionális) lásd: [[#Use x-callback-url parameters]].
- `x-error` (opcionális) lásd: [[#Use x-callback-url parameters]].

Ha `x-success` paramétert adsz meg, az API **ezt fogja használni** x-callback-url-ként. **Ellenkező esetben** az aktuális fókuszált jegyzet **Markdown hivatkozását** másolja a vágólapra **obsidian://open** URL-ként.

## x-callback-url paraméterek használata

Bizonyos végpontok elfogadják az **x-callback-url** paramétereket: `x-success` és `x-error`.  
Ha ezeket megadod, az Obsidian az alábbi adatokat küldi vissza az `x-success` callbackhez:

- `name` — a fájl neve **kiterjesztés nélkül**.
- `url` — az `obsidian://` URI a fájlhoz.
- `file` (csak asztali verzió) — a `file://` URL a fájlhoz.

Példa:  
Ha az Obsidian ezt kapja:  
`obsidian://.....x-success=myapp://x-callback-url`,  
akkor a válasz:  
`myapp://x-callback-url?name=...&url=obsidian%3A%2F%2Fopen...&file=file%3A%2F%2F...`

## Rövidített formátumok

Az előző formátumokon kívül két további **"rövidített"** formátum is használható tárolók és fájlok megnyitásához:

1. `obsidian://vault/my vault/my note` ekvivalens az alábbi URI-val:  
   `obsidian://open?vault=my%20vault&file=my%20note`
2. `obsidian:///absolute/path/to/my note` ekvivalens az alábbi URI-val:  
   `obsidian://open?path=%2Fabsolute%2Fpath%2Fto%2Fmy%20note`

## Hibaelhárítás

### Obsidian URI regisztrálása

Windows és macOS rendszereken **az alkalmazás egyszeri futtatása elegendő**, hogy regisztrálja az Obsidian URI protokollt a gépen.

Linuxon viszont **összetettebb folyamat** szükséges:

1. **Hozz létre egy** `obsidian.desktop` **fájlt**. [Részletek itt](https://developer.gnome.org/documentation/guidelines/maintainer/integrating.html#desktop-files).
2. Győződj meg arról, hogy a **desktop fájlban az `Exec` mező így van megadva**:  
   `Exec=executable %u`  
   A `%u` szükséges az **`obsidian://` URI-k továbbításához** az alkalmazásnak.
3. Ha **AppImage telepítőt** használsz, előfordulhat, hogy ki kell **csomagolnod**:  
   `Obsidian-x.y.z.AppImage --appimage-extract`  
   Ezután az `Exec` mezőnek a **kicsomagolt futtatható fájlra kell mutatnia**.

[^1]: A tároló azonosítója egy **véletlenszerű 16 karakteres kód**, például `ef6ca3e3b524d22f`.  
Minden számítógépen lévő tárolóhoz **egyedi** azonosító tartozik.  
Az azonosítót a **tárolóváltó megnyitásával** találhatod meg, és **a kívánt tárolónál válaszd a "Tároló azonosító másolása" lehetőséget**.

