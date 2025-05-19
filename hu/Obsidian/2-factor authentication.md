---
aliases:
  - 2FA
  - Recovery codes
permalink: 2fa
---
Ha rendelkezel [Obsidian fiókkal](https://obsidian.md/account), engedélyezheted a kétlépcsős hitelesítést (2FA), hogy egy második ellenőrzési lépéssel védd a fiókodat.

## 2FA engedélyezése

- Jelentkezz be [Obsidian fiókodba](https://obsidian.md/account/profile) a böngésződből.
- A **Profil** szekcióban menj a **Kétlépcsős hitelesítés** menüpontra, majd válaszd az **Engedélyezés** lehetőséget.
- Egy felugró ablak jelenik meg, amely arra kér, hogy csatlakoztasd egy hitelesítő alkalmazást **QR-kód** vagy **beállítási kulcs** segítségével.

> [!hint]- Népszerű hitelesítő alkalmazások
> - [Authy](https://authy.com)
> - [Google Authenticator](https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2)
> - [Microsoft Authenticator](https://www.microsoft.com/en-us/security/mobile-authenticator-app)
> - [iCloud Keychain](https://support.apple.com/en-gb/guide/iphone/ipha6173c19f/ios)

- Miután csatlakoztattad a hitelesítő alkalmazást, az generál egy hatjegyű kódot. Írd be ezt a kódot a **QR-kód/beállítási kulcs** rész alá, a 3. lépésben.
- Végül add meg a jelenlegi jelszavadat.
- Válaszd a **Beállítás befejezése** lehetőséget.
- A felugró ablak egy megerősítő ablakra vált, amely megmutatja a helyreállítási kódjaidat. **Mentésre ajánlott**, mivel ezekre szükséged lesz a fiók visszaállításához.

Most már be van állítva a 2FA.

> [!warning]- QR-kód/beállítási kulcs biztonsági mentése  
> Ha úgy döntesz, hogy **mentést készítesz** a **QR-kódról** vagy **beállítási kulcsról** a helyreállítási kódok mellett, **erősen ajánlott**, hogy egy **jelszóval titkosított rendszerben tárold**.

## Helyreállítási kódok generálása

Ha korábban engedélyezted a 2FA-t, amikor még nem volt helyreállítási kód elérhető, vagy ha frissíteni szeretnéd a helyreállítási kódjaidat, kövesd az alábbi lépéseket:

- Jelentkezz be [Obsidian fiókodba](https://obsidian.md/account/profile) a böngészőből.
- A **Kétlépcsős hitelesítés** mellett válaszd a **Helyreállítási kódok frissítése** lehetőséget.
- A felugró ablakban add meg a **jelszavadat** és a **6 jegyű hitelesítő kódodat**.
- Egy megerősítő ablak megjeleníti a helyreállítási kódjaidat. Két lehetőség közül választhatsz:
    - **Másolás**: A kódokat másolhatod és beillesztheted máshová.
    - **Letöltés**: Letölthetsz egy `obsidian-recovery-codes.txt` fájlt, amely tartalmazza a kódjaidat.
- Válaszd a **Rendben** gombot a felugró ablak bezárásához.

A helyreállítási kódokat **egyszer** használhatod **a 6 jegyű hitelesítő kód helyett**, és bármikor **frissítheted** őket.

## 2FA letiltása

- Jelentkezz be [Obsidian fiókodba](https://obsidian.md/account/profile) a böngésződből.
- A **Profil** szekcióban menj a **Kétlépcsős hitelesítés** menüpontra, majd válaszd a **Letiltás** lehetőséget.
- Add meg az Obsidian jelszavadat.
- Írd be a jelenlegi hatjegyű kódot a hitelesítő alkalmazásodból.
- Válaszd a **2FA letiltása** lehetőséget.
- Visszakerülsz a fiókkezelési képernyőre.

A **Kétlépcsős hitelesítés** beállítás ismét egy **Engedélyezés** gombot fog mutatni, ami jelzi, hogy a 2FA le lett tiltva.

## Gyakran Ismételt Kérdések

**Engedélyeztem a 2FA-t. Ki fogok jelentkezni az Obsidian eszközeimen?**  
Nem. A 2FA engedélyezése nem jelentkeztet ki automatikusan minden eszközödről. Ha szükséges, manuálisan kijelentkezhetsz a fiókoldaladon, majd újra bejelentkezhetsz minden eszközön.

**Engedélyeztem, majd letiltottam a 2FA-t. Újra szeretném beállítani. Használhatom az eredeti QR-kódot vagy beállítási kulcsot?**  
Nem. Minden alkalommal **új QR-kódot** és **új beállítási kulcsot** kapsz, amikor újra beállítod a 2FA-t.

**Engedélyeztem a 2FA-t, de többszöri kijelentkezés/belépés után sem kérte tőlem. Ez működik?**  
A böngésző gyorsítótára miatt úgy tűnhet, mintha változtatásokat végeznél az oldalon (például bejelentkezés/kijelentkezés), miközben valójában a tárolt adatokhoz férsz hozzá.  
Próbáld meg egy privát böngészőablakban bejelentkezni, hogy megerősítsd a 2FA működését.

Ha a probléma továbbra is fennáll, kérlek [jelentsd be egy hibajelentésben](https://forum.obsidian.md/c/bug-reports/7).

**Elvesztettem a helyreállítási kódjaimat, a hitelesítőmet, és minden mást, ami szükséges lenne a fiókomhoz. Mit tegyek?**  

Ha elvesztetted a helyreállítási kódjaidat és a hitelesítődet, kérlek írj emailt a [support@obsidian.md](mailto:support@obsidian.md?subject=I%20lost%20my%202FA) címre segítségért a fiókodhoz való hozzáférés visszaállításához.

