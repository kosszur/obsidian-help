---
aliases:
  - How to/Embedding web pages
  - Iframe
  - Editing and formatting/Embedding web pages
permalink: embed-web-pages
---
Tanuld meg, hogyan használhatod az [iframe](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe) HTML elemet weboldalak beágyazására jegyzeteidben.

Weboldal beágyazásához add hozzá az alábbi kódot a jegyzetedhez, és cseréld ki a helyőrző szöveget az beágyazni kívánt weboldal URL-jével:

```html
<iframe src="INSERT YOUR URL HERE"></iframe>
```

> [!note]  
> Néhány weboldal **nem engedélyezi** a beágyazást. Ehelyett olyan URL-eket kínálhatnak, amelyek **külön erre a célra** készültek. Ha egy weboldal **nem támogatja a beágyazást**, próbáld meg **keresni** a weboldal nevét az "embed iframe" kifejezéssel. Például: "youtube embed iframe".

> [!tip]  
> Ha a [[Canvas]] szolgáltatást használod, egy weboldalt beágyazhatsz egy kártyába is. További információért lásd: [[Canvas#Add cards from web pages]].

## YouTube videó beágyazása

YouTube videó beágyazásához használhatod **ugyanazt a Markdown szintaxist**, mint a [[Basic formatting syntax#External images|külső képeknél]]:

```md
![](https://www.youtube.com/watch?v=NnTvZWp5Q7o)
```

![](https://www.youtube.com/watch?v=NnTvZWp5Q7o)

## Tweet beágyazása

Tweet beágyazásához használd ugyanazt a Markdown szintaxist, mint a [[Basic formatting syntax#External images|külső képeknél]]:

```md
![](https://twitter.com/obsdmd/status/1580548874246443010)
```

![](https://twitter.com/obsdmd/status/1580548874246443010)
