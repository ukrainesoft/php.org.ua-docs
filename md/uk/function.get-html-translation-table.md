---
navigation:
  - function.fprintf.md: « fprintf
  - function.hebrev.md: hebrev »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: get\_html\_translation\_table
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# get\_html\_translation\_table

(PHP 4, PHP 5, PHP 7, PHP 8)

get\_html\_translation\_table — Повертає таблицю перетворень, що використовується функціями [htmlspecialchars()](function.mdspecialchars.md) і [htmlentities()](function.mdentities.md)

### Опис

```methodsynopsis
get_html_translation_table(int $table = HTML_SPECIALCHARS, int $flags = ENT_QUOTES | ENT_SUBSTITUTE | ENT_HTML401, string $encoding = "UTF-8"): array
```

**get\_html\_translation\_table()** повертає таблицю перетворень, що використовується функціями [htmlspecialchars()](function.mdspecialchars.md) і [htmlentities()](function.mdentities.md)

> **Зауваження** :
> 
> Спеціальні символи можуть бути закодовані різними способами. Наприклад, `"` може бути закодований як `&quot;` `&#34;`или`&#x22`. . **get\_html\_translation\_table()** повертає лише форми, що використовуються функціями [htmlspecialchars()](function.mdspecialchars.md) і [htmlentities()](function.mdentities.md)

### Список параметрів

`table`

Вказує, яку таблицю використовуватиме перетворення. Або **`HTML_ENTITIES`**, либо\*\*`HTML_SPECIALCHARS`\*\*

`flags`

Бітова маска, що складається з одного або декількох наведених нижче прапорів, які вказують, які лапки міститиме таблиця, а також для якого документа таблиця призначена. Значення за замовчуванням `ENT_QUOTES | ENT_SUBSTITUTE | ENT_HTML401`

**Доступні константи у параметрі `flags`**

| Имя константы | Опис |
| --- | --- |
| **`ENT_COMPAT`** | Таблиця міститиме сутності для подвійних лапок, але не буде для одинарних. |
| **`ENT_QUOTES`** | Таблиця міститиме сутності як для подвійних лапок, так і для одинарних. |
| **`ENT_NOQUOTES`** | Таблиця не міститиме сутності ні для подвійних лапок, ні для одинарних. |
| **`ENT_SUBSTITUTE`** | Замінює некоректні кодові послідовності символом заміни Юнікоду U+FFFD у разі використання UTF-8 та &#FFFD; при використанні іншого кодування замість повернення порожнього рядка. |
| **`ENT_HTML401`** | Таблиця для HTML 4.01 |
| **`ENT_XML1`** | Таблиця для XML 1. |
| **`ENT_XHTML`** | Таблиця XHTML. |
| **`ENT_HTML5`** | Таблиця для HTML 5 |

`encoding`

Кодування, що використовується. Якщо не вказано, значенням за промовчанням для цього аргументу є UTF-8.

Підтримуються такі кодування:

**Підтримувані кодування**

| Кодировка | Псевдонимы | Опис |
| --- | --- | --- |
| ISO-8859-1 | ISO8859-1 | Західноєвропейська Latin-1. |
| ISO-8859-5 | ISO8859-5 | Рідко використовуване кириличне кодування (Latin/Cyrillic). |
| ISO-8859-15 | ISO8859-15 | Західноєвропейська Latin-9. Додає символ євро, французькі та фінські літери до кодування Latin-1 (ISO-8859-1). |
| UTF-8 |  | 8-бітна Unicode, сумісна з ASCII. |
| cp866 | ibm866, 866 | Кирилічна кодування, що застосовується в DOS. |
| cp1251 | Windows-1251, win-1251, 1251 | Кирилічна кодування, що використовується у Windows. |
| cp1252 | Windows-1252, 1252 | Західно-європейське кодування, що використовується у Windows. |
| KOI8-R | koi8-ru, koi8r | Російське кодування. |
| BIG5 | 950 | Традиційний китайський, застосовується переважно на Тайвані. |
| GB2312 | 936 | Спрощена китайська, стандартне національне кодування. |
| BIG5-HKSCS |  | Розширена Big5, що застосовується в Гонконгу. |
| Shift\_JIS | SJIS, SJIS-win, cp932, 932 | Японське кодування. |
| EUC-JP | EUCJP, eucJP-win | Японське кодування. |
| MacRoman |  | Кодування, яке використовується в Mac OS. |
| `''` |  | Порожній рядок активує режим визначення кодування із файлу скрипта (Zend multibyte), [default\_charset](ini.core.md#ini.default-charset) та поточної локалі (дивіться [nl\_langinfo()](function.nl-langinfo.md) і [setlocale()](function.setlocale.md)) у зазначеному порядку. Не рекомендується використовувати. |

> **Зауваження**: Інші кодування не підтримуються, замість них буде застосовано кодування за замовчуванням та згенеровано попередження.

### Значення, що повертаються

Повертає таблицю перетворень у вигляді масиву з оригінальними символами як ключі та сутності як значення.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Значення за промовчанням `flags` змінено з **`ENT_COMPAT`**на**`ENT_QUOTES`** |

### Приклади

**Приклад #1 Приклад таблиці перетворень**

```php
<?php
var_dump(get_html_translation_table(HTML_ENTITIES, ENT_QUOTES | ENT_HTML5));
?>
```

Висновок наведеного прикладу буде схожим на:

```
array(1510) {
  ["
"]=>
  string(9) "&NewLine;"
  ["!"]=>
  string(6) "&excl;"
  ["""]=>
  string(6) "&quot;"
  ["#"]=>
  string(5) "&num;"
  ["$"]=>
  string(8) "&dollar;"
  ["%"]=>
  string(8) "&percnt;"
  ["&"]=>
  string(5) "&amp;"
  ["'"]=>
  string(6) "&apos;"
  // ...
}
```

### Дивіться також

-   [htmlspecialchars()](function.mdspecialchars.md) \- Перетворює спеціальні символи в HTML-сутності
-   [htmlentities()](function.mdentities.md) \- Перетворює всі можливі символи у відповідні HTML-сутності
-   [html\_entity\_decode()](function.md-entity-decode.md) \- Перетворює HTML-сутності на символи
