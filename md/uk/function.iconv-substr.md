---
navigation:
  - function.iconv-strrpos.md: « iconv\_strrpos
  - function.iconv.md: iconv »
  - index.md: PHP Manual
  - ref.iconv.md: Функції iconv
title: iconv\_substr
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# iconv\_substr

(PHP 5, PHP 7, PHP 8)

iconv\_substr — Отримання частини рядка

### Опис

```methodsynopsis
iconv_substr(    string $string,    int $offset,    ?int $length = null,    ?string $encoding = null): string|false
```

Отримує частину рядка `string`, визначену параметрами `offset`и`length`

### Список параметрів

`string`

Початковий рядок.

`offset`

Якщо `offset`неотрицателен,**iconv\_substr()** отримує частину рядка `string` починаючи із символу з порядковим номером `offset` (Нумерація починається з нуля).

Якщо `offset`отрицателен,**iconv\_substr()** отримує частину рядка починаючи з позиції, що віддаляється від кінця рядка `string`на`offset` символів.

`length`

Якщо `length` заданий і позитивний, значення, що повертається містить не більше `length` символів, починаючи з `offset` (залежить від довжини рядка `string`

Якщо вказано негативний `length` **iconv\_substr()** отримує частину рядка `string`, починаючи з `offset` символу і до символу, віддаленого від кінця рядка на `length` символів. У разі якщо `offset` також негативний, стартова позиція обчислюється заздалегідь відповідно до вищеописаного правила.

`encoding`

Якщо параметр `encoding` не вказано, передбачається, що рядок `string` має кодування [iconv.internal\_encoding](iconv.configuration.md)

Обратите внимание, что и`offset`, и`length` ґрунтуються на розмірі символу, розрахованого виходячи з кодування тексту (`encoding`), у той час як схожа функція [substr()](function.substr.md) завжди розглядає їх побайтове усунення.

### Значення, що повертаються

Повертає частину рядка `string`, визначену параметрами `offset`и`length`

Якщо рядок `string`имеет меньшую длину, чем параметр`offset`, буде повернуто **`false`**. Якщо `string` має довжину рівну `offset`, буде повернуто порожній рядок.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `length`и`encoding` тепер допускають значення null. |
| 7.0.11 | Якщо `string` має довжину рівну `offset`, буде повернено порожній рядок. Раніше у таких випадках поверталося **`false`** |

### Дивіться також

-   [substr()](function.substr.md) \- Повертає підрядок
-   [mb\_substr()](function.mb-substr.md) \- Повертає частину рядка
-   [mb\_strcut()](function.mb-strcut.md) \- Отримує частину рядка
