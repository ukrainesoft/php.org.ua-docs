---
navigation:
  - function.iconv-strlen.md: « iconv\_strlen
  - function.iconv-strrpos.md: iconv\_strrpos »
  - index.md: PHP Manual
  - ref.iconv.md: Функції iconv
title: iconv\_strpos
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# iconv\_strpos

(PHP 5, PHP 7, PHP 8)

iconv\_strpos — Повертає позицію першого входження підрядка

### Опис

```methodsynopsis
iconv_strpos(    string $haystack,    string $needle,    int $offset = 0,    ?string $encoding = null): int|false
```

Повертає позицію першого входження підрядка `needle` в рядку `haystack`

В отличие от[strpos()](function.strpos.md) **iconv\_strpos()** повертає зміщення перед рядком у символах, а не в байтах. Кількість символів трактується залежно від вказаної параметром `encoding` кодування.

### Список параметрів

`haystack`

Рядок, в якому проводиться пошук.

`needle`

Шуканий підрядок.

`offset`

Необов'язковий параметр `offset` дозволяє вказати, з якого символу рядка починати пошук. Якщо вказано негативне значення, зсув буде відлічуватися з кінця рядка.

`encoding`

Якщо параметр `encoding` не вказано, то мається на увазі, що `string` має кодування [iconv.internal\_encoding](iconv.configuration.md)

Якщо `haystack`или`needle` не є рядками, вони будуть перетворені на рядок та застосовані як код символу.

### Значення, що повертаються

Повертає номер позиції першого входження рядка `needle`в`haystack`

Якщо рядок `needle`не найдена,**iconv\_strpos()** повертає **`false`**

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Логічний тип](language.types.boolean.md)Используйте[оператор ===](language.operators.comparison.md) для перевірки значення, яке повертається цією функцією.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `encoding` тепер допускає значення null. |
| 7.1.0 | Підтримка негативних значень `offset` |

### Дивіться також

-   [strpos()](function.strpos.md) \- Повертає позицію першого входження підрядка
-   [iconv\_strrpos()](function.iconv-strrpos.md) \- Повертає позицію останнього входження підрядка
-   [mb\_strpos()](function.mb-strpos.md) \- Шукає позицію першого входження підрядка у рядок
