---
aliases:
  - Concepts/Insider builds
  - Insider builds
permalink: early-access
---
Szerezz korai hozzáférést a közelgő kiadásokhoz a _korai hozzáférésű verziók_ engedélyezésével.  
A korai hozzáférésű verziók **csak a [[Catalyst license]] licenccel rendelkező felhasználók számára elérhetők**.

> [!warning]  
> A korai hozzáférésű verziók **béta kiadások**. Új funkciókat tartalmaznak, de **kevésbé stabilak lehetnek**.  
> **Ne engedélyezd a korai hozzáférésű verziókat**, ha **megbízhatóbb élményt** szeretnél.  
>  
> A közösségi bővítmény- és témafejlesztők **ugyanakkor kapják meg** a korai hozzáférésű verziókat, mint mindenki más.  
> **Légy türelmes** azokkal a fejlesztőkkel, akiknek **frissítéseket kell készíteniük az új funkciók támogatásához**.

## Korai hozzáférésű verziók engedélyezése asztali gépen

A korai hozzáférésű verziók fogadásához kövesd az alábbi lépéseket:

1. Nyisd meg a **Beállítások** menüt.
2. Az oldalsávban válaszd az **Általános** lehetőséget.
3. Az **Fiók → Saját fiók** alatt válaszd a **Bejelentkezés** lehetőséget.
4. Az **Email** mezőbe írd be az email címedet.
5. A **Jelszó** mezőbe írd be a jelszavadat.
6. Bejelentkezés után térj vissza a **Beállítások** menübe.
7. Az oldalsávban válaszd az **Általános** lehetőséget.
8. Az **Alkalmazás** szekció alatt engedélyezd a **Korai hozzáférésű verziók fogadását**.

## Korai hozzáférésű verziók telepítése mobil eszközön

A korai hozzáférésű verziók telepítéséhez mobil eszközön kövesd az alábbi lépéseket:

1. Csatlakozz az [Obsidian Discord szerverhez](https://discord.gg/veuWUTm).
2. [[Catalyst license#Get your Discord badge|Szerezd meg a Discord jelvényedet]], hogy hozzáférj az insider csatornákhoz.
3. Nyisd meg a Discordot.
4. Az `#insider-mobile-release` csatornában nyisd meg a **Rögzített üzeneteket**.
   - **Asztali verzión**: válaszd a **rajzszög ikont** a jobb felső sarokban.
   - **Mobilon**: húzd balra és válaszd a **Rögzített üzenetek** lehetőséget.
5. A **Rögzített üzenetek** alatt válaszd ki az **eszközödre vonatkozó telepítési linket**:
   - **iOS esetén**: Nyisd meg a TestFlight linket iPhone-on vagy iPaden.
   - **Android esetén**: Töltsd le és telepítsd az APK fájlt.

## Probléma bejelentése és visszajelzés

Ha hibát találsz egy korai hozzáférésű verzióban, érdemes **bejelenteni** az Obsidian csapatnak.  
A bejelentés előtt keresd meg a [fórumban](https://forum.obsidian.md/) vagy Discordon, hogy más **már jelentette-e** ugyanazt a problémát.

A hiba bejelentésére az alábbi csatornák állnak rendelkezésre:

- **Discordon**: Jelentsd a problémát a megfelelő `#insider-release` csatornában.
- **Fórumon**: Hozz létre új témát a [Hibajelentések](https://forum.obsidian.md/c/bug-reports/7) részben.

A hiba bejelentésekor **add meg a build verziót és az operációs rendszert**, amelyen futtatod az Obsidian-t.  
A build verziót megtalálod a **Beállítások → Névjegy → Alkalmazás → Jelenlegi verzió** alatt.

## Visszaállás nyilvános verzióra asztali gépen

A nyilvános (nem korai hozzáférésű) verzióra való visszaálláshoz asztali gépen:

1. **Tiltsd le** a korai hozzáférésű verziókat:
   1. Nyisd meg a **Beállítások** menüt.
   2. Az oldalsávban válaszd az **Általános** lehetőséget.
   3. Az **Alkalmazás** alatt **kapcsold ki** a **Korai hozzáférésű verziók fogadását**.
2. Zárd be az Obsidian-t.
3. Töröld az `obsidian-VERSION.asar` fájlt, ahol a `VERSION` az Obsidian verziója.
   - **Windows**: `%APPDATA%\obsidian\obsidian-VERSION.asar`
   - **Mac**: `~/Library/Application Support/obsidian/obsidian-VERSION.asar`
   - **Linux**: `~/.config/obsidian/obsidian-VERSION.asar`
4. Indítsd újra az Obsidian-t.

## Visszaállás nyilvános verzióra mobilon

A nyilvános (nem korai hozzáférésű) verzióra való visszaálláshoz mobilon:

1. **Készíts biztonsági mentést** a tároló adataidról.
2. **Távolítsd el** az Obsidian alkalmazást.
3. **Telepítsd újra** az Obsidian-t a Play Store-ból vagy az Apple App Store-ból.
4. **Állítsd vissza** a tároló adataidat a mentésekből.
5. **Nyisd meg** az Obsidian-t.
