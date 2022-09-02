---
navigation:
  - function.iconv-strlen.md: « iconvstrlen
  - function.iconv-strrpos.md: iconvstrrpos »
  - index.md: PHP Manual
  - ref.iconv.md: Функции iconv
title: iconvstrpos
---
# iconvstrpos

(PHP 5, PHP 7, PHP 8)

iconvstrpos — Повертає позицію першого входження підрядка

### Опис

```methodsynopsis
iconv_strpos(    string $haystack,    string $needle,    int $offset = 0,    ?string $encoding = null): int|false
```

Повертає позицію першого входження підрядка `needle` у рядку `haystack`

На відміну від [strpos()](function.strpos.md) **iconvstrpos()** повертає зміщення перед рядком у символах, а не в байтах. Кількість символів трактується залежно від вказаної параметром `encoding` кодування.

### Список параметрів

`haystack`

Рядок, в якому проводиться пошук.

`needle`

Шуканий підрядок.

`offset`

Необов'язковий параметр `offset` дозволяє вказати, з якого символу рядка починати пошук. Якщо вказано негативне значення, зсув буде відлічуватися з кінця рядка.

`encoding`

Якщо параметр `encoding` не вказано, то мається на увазі, що `string` має кодування [iconv.internalencoding](iconv.configuration.md)

Якщо `haystack` або `needle` не є рядками, вони будуть перетворені на рядок та застосовані як код символу.

### Значення, що повертаються

Повертає номер позиції першого входження рядка `needle` в `haystack`

Якщо рядок `needle` не знайдена, **iconvstrpos()** повертає **`false`**

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Булев тип](language.types.boolean.md). Використовуйте [оператор ===](language.operators.comparison.md) для перевірки значення, яке повертається цією функцією.

### список змін

| Версия | Описание |
| --- | --- |
|  | `encoding` тепер допускає значення null. |
|  | Підтримка негативних значень `offset` |

### Дивіться також

-   [strpos()](function.strpos.md) - Повертає позицію першого входження підрядка
-   [iconvstrrpos()](function.iconv-strrpos.md) - Повертає позицію останнього входження підрядка
-   [мбstrpos()](function.mb-strpos.md) - Пошук позиції першого входження одного рядка до іншого
