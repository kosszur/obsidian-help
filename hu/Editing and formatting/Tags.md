---
aliases:
  - How to/Working with tags
permalink: tags
---
A címkék olyan **kulcsszavak vagy témák**, amelyek segítenek gyorsan megtalálni a kívánt jegyzeteket.

## Címke hozzáadása egy jegyzethez

Címke létrehozásához **írj egy `#` karaktert** a szerkesztőben, majd **adj hozzá egy kulcsszót**. Például: `#meeting`.

Címkéket a `tags` [[Properties|tulajdonság]] segítségével is hozzáadhatsz. YAML formátumban a címkéknek **mindig listaként** kell szerepelniük:

```yaml
---
tags:
  - recipe
  - cooking
---
```

## Jegyzetek keresése címkék alapján

A jegyzeteket címkék alapján megtalálhatod a [[Search|Keresés]] bővítménnyel, ha a **`tag`** [[Search#Search operators|keresési operátort]] használod, például `tag:#meeting`.

Kereshetsz címkék alapján **közvetlenül a jegyzetekben** is, ha rájuk kattintasz.

A [[Tags view|Címkenézet]] bővítmény segítségével válaszd a **Tags: Show tags** parancsot a [[Command palette|Parancspalettában]], majd válaszd ki a keresni kívánt címkét.

## Egymásba ágyazott címkék

Az **egymásba ágyazott címkék** címke-hierarchiákat határoznak meg, amelyek **megkönnyítik a kapcsolódó címkék keresését és szűrését**.

Egymásba ágyazott címkéket hozhatsz létre **perjelek (`/`) használatával** a címke nevében, például `#inbox/to-read` és `#inbox/processing`.

A **[[Search|Keresés]] és [[Tags view|Címkenézet]]** bővítmények **támogatják az egymásba ágyazott címkéket**.

## Címke formátuma

Címkék létrehozásához az alábbi karaktereket használhatod:

- Betűk (A–Z)
- Számok (0–9)
- Aláhúzás (`_`)
- Kötőjel (`-`)
- Perjel (`/`) az [[#Nested tags|egymásba ágyazott címkékhez]]

A címkéknek **legalább egy nem számjegy karaktert** kell tartalmazniuk. Például `#1984` **nem** érvényes címke, de `#y1984` **igen**.

A címkék **nem érzékenyek a kis- és nagybetűkre**. Például `#tag` és `#TAG` **ugyanolyanként** lesz kezelve.

> [!note]  
> A címkék azzal a **kis- és nagybetűs formázással jelennek meg**, amellyel **először létrehoztad őket** a [[Tags view|Címkenézetben]].  
> Például ha először `#Tag`-et hozol létre, majd később `#TAG`-et, **mindkettő `#Tag`-ként jelenik meg**.

A címkék **nem tartalmazhatnak szóközt**. Két vagy több szó elválasztására az alábbi formátumokat használhatod:

- `#camelCase`
- `#PascalCase`
- `#snake_case`
- `#kebab-case`
