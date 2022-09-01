---
navigation:
  - function.similar-text.html: « similartext
  - function.sprintf.html: sprintf »
  - index.html: PHP Manual
  - ref.strings.html: Функції для роботи з рядками
title: soundex
---
# soundex

(PHP 4, PHP 5, PHP 7, PHP 8)

soundex — Повертає ключ soundex для рядка

### Опис

```methodsynopsis
soundex(string $string): string
```

Повертає ключ soundex для рядка `string`

Двом словам, що мають схожу вимову, відповідає той самий ключ soundex. Ця властивість може бути використана, наприклад, при пошуку бази даних, коли відома вимова слова і невідомо його написання.

Ця реалізація функції soundex описана Дональдом Кнутом (Donald Knuth) у книзі "The Art Of Computer Programming, vol. 3: Sorting And Searching", Addison-Wesley (1973), стор 391-392.

### Список параметрів

`string`

Вхідний рядок.

### Значення, що повертаються

Повертає ключ soundex у вигляді рядка (string). Повертає ключ soundex у вигляді рядка (string) із чотирма символами. Якщо в `string` міститься хоча б одна літера, рядок, що повертається починається з літери. В іншому випадку повертається `"0000"`

### список змін

| Версия | Описание |
| --- | --- |
|  | До цієї версії при виклику функції з порожнім рядком поверталося **`false`** без особливих причин. |

### Приклади

**Приклад #1 Приклад використання soundex**

```php
<?php
soundex("Euler")       == soundex("Ellery");    // E460
soundex("Gauss")       == soundex("Ghosh");     // G200
soundex("Hilbert")     == soundex("Heilbronn"); // H416
soundex("Knuth")       == soundex("Kant");      // K530
soundex("Lloyd")       == soundex("Ladd");      // L300
soundex("Lukasiewicz") == soundex("Lissajous"); // L222
?>
```

### Дивіться також

-   [levenshtein()](function.levenshtein.html) - обчислює відстань Левенштейна між двома рядками
-   [metaphone()](function.metaphone.html) - Повертає ключ metaphone для рядка
-   [similartext()](function.similar-text.html) - обчислює ступінь схожості двох рядків
