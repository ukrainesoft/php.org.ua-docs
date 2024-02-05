---
navigation:
  - function.iconv-strpos.md: « iconv\_strpos
  - function.iconv-substr.md: iconv\_substr »
  - index.md: PHP Manual
  - ref.iconv.md: Функції iconv
title: iconv\_strrpos
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# iconv\_strrpos

(PHP 5, PHP 7, PHP 8)

iconv\_strrpos — Повертає позицію останнього входження підрядка

### Опис

```methodsynopsis
iconv_strrpos(string $haystack, string $needle, ?string $encoding = null): int|false
```

Находит последнюю позицию подстроки`needle` в рядку `haystack`

В отличие от[strrpos()](function.strrpos.md) **iconv\_strrpos()** повертає зміщення перед рядком у символах, а не в байтах. Кількість символів трактується залежно від вказаної параметром `encoding` кодування.

### Список параметрів

`haystack`

Рядок, в якому проводиться пошук.

`needle`

Шуканий підрядок.

`encoding`

Якщо параметр `encoding` не вказано, то мається на увазі, що `string` має кодування [iconv.internal\_encoding](iconv.configuration.md)

Якщо `haystack`или`needle` не є рядками, вони будуть перетворені на рядок та застосовані як код символу.

### Значення, що повертаються

Повертає номер позиції останнього входження рядка `needle`в`haystack`

Якщо рядок `needle`не найдена,**iconv\_strrpos()** повертає **`false`**

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Логічний тип](language.types.boolean.md)Используйте[оператор ===](language.operators.comparison.md) для перевірки значення, яке повертається цією функцією.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `encoding` тепер допускає значення null. |

### Дивіться також

-   [strrpos()](function.strrpos.md) \- Повертає позицію останнього входження підрядка у рядку
-   [iconv\_strpos()](function.iconv-strpos.md) \- Повертає позицію першого входження підрядка
-   [mb\_strrpos()](function.mb-strrpos.md) \- Шукає позицію останнього входження підрядка у рядок
