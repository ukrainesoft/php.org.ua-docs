---
navigation:
  - function.fprintf.html: « fprintf
  - function.hebrev.html: hebrev »
  - index.html: PHP Manual
  - ref.strings.html: Функції для роботи з рядками
title: gethtmltranslationtable
---
# gethtmltranslationtable

(PHP 4, PHP 5, PHP 7, PHP 8)

gethtmltranslationtable — Повертає таблицю перетворень, що використовується функціями [htmlspecialchars()](function.htmlspecialchars.html) і [htmlentities()](function.htmlentities.html)

### Опис

```methodsynopsis
get_html_translation_table(int $table = HTML_SPECIALCHARS, int $flags = ENT_QUOTES | ENT_SUBSTITUTE | ENT_HTML401, string $encoding = "UTF-8"): array
```

**gethtmltranslationtable()** повертає таблицю перетворень, що використовується функціями [htmlspecialchars()](function.htmlspecialchars.html) і [htmlentities()](function.htmlentities.html)

> **Зауваження**
> 
> Спеціальні символи можуть бути закодовані різними способами. Наприклад, `"` може бути закодований як `&quot;` `&#34;` або `&#x22`. . **gethtmltranslationtable()** повертає лише форми, що використовуються функціями [htmlspecialchars()](function.htmlspecialchars.html) і [htmlentities()](function.htmlentities.html)

### Список параметрів

`table`

Вказує, яку таблицю використовуватиме перетворення. Або **`HTML_ENTITIES`**, або **`HTML_SPECIALCHARS`**

`flags`

Бітова маска, що складається з одного або декількох наведених нижче прапорів, які вказують, які лапки міститиме таблиця, а також для якого документа таблиця призначена. Значення за замовчуванням `ENT_QUOTES | ENT_SUBSTITUTE | ENT_HTML401`

**Доступні константи у параметрі `flags`**

| Имя константы | Описание |
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

| Кодировка | Псевдонимы | Описание |
| --- | --- | --- |
| ISO-8859-1 | ISO8859-1 | Західноєвропейська Latin-1. |
| ISO-8859-5 | ISO8859-5 | Рідко використовуване кириличне кодування (Latin/Cyrillic). |
| ISO-8859-15 | ISO8859-15 | Західноєвропейська Latin-9. Додає символ євро, французькі та фінські літери до кодування Latin-1 (ISO-8859-1). |
| UTF-8 |  | 8-бітна Unicode, сумісна з ASCII. |
| CP866 | ibm866, 866 | Кирилічна кодування, що застосовується в DOS. |
| CP1251 | Windows-1251, win-1251, 1251 | Кирилічна кодування, що використовується у Windows. |
| CP1252 | Windows-1252, 1252 | Західно-європейське кодування, що використовується у Windows. |
| KOI8-R | koi8-ru, koi8r | Російське кодування. |
| BIG5 |  | Традиційний китайський, застосовується переважно на Тайвані. |
| GB2312 |  | Спрощена китайська, стандартне національне кодування. |
| BIG5-HKSCS |  | Розширена Big5, що застосовується в Гонконгу. |
| ShiftJIS | SJIS, SJIS-win, CP932, 932 | Японське кодування. |
| EUC-JP | EUCJP, eucJP-win | Японське кодування. |
| MacRoman |  | Кодування, яке використовується в Mac OS. |
| `''` |  | Порожній рядок активує режим визначення кодування із файлу скрипта (Zend multibyte), [defaultcharset](ini.core.html#ini.default-charset) та поточної локалі (дивіться [нлlanginfo()](function.nl-langinfo.html) і [setlocale()](function.setlocale.html)) у зазначеному порядку. Не рекомендується використовувати. |

> **Зауваження**: Інші кодування не підтримуються, замість них буде застосовано кодування за замовчуванням та згенеровано попередження.

### Значення, що повертаються

Повертає таблицю перетворень у вигляді масиву з оригінальними символами як ключі та сутності як значення.

### список змін

| Версия | Описание |
| --- | --- |
|  | Значення за промовчанням `flags` змінено з **`ENT_COMPAT`** на **`ENT_QUOTES`** |

### Приклади

**Приклад #1 Приклад таблиці перетворень**

```php
<?php
var_dump(get_html_translation_table(HTML_ENTITIES, ENT_QUOTES | ENT_HTML5));
?>
```

Результатом виконання цього прикладу буде щось подібне:

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

-   [htmlspecialchars()](function.htmlspecialchars.html) - Перетворює спеціальні символи на HTML-сутності
-   [htmlentities()](function.htmlentities.html) - Перетворює всі можливі символи у відповідні HTML-сутності
-   [htmlentitydecode()](function.html-entity-decode.html) - Перетворює HTML-сутності у відповідні їм символи
