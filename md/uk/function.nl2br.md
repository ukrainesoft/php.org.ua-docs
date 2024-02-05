---
navigation:
  - function.nl-langinfo.md: « nl\_langinfo
  - function.number-format.md: number\_format »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: nl2br
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# nl2br

(PHP 4, PHP 5, PHP 7, PHP 8)

nl2br — Вставляє HTML код розриву рядка перед кожним перекладом рядка

### Опис

```methodsynopsis
nl2br(string $string, bool $use_xhtml = true): string
```

Повертає рядок `string`, в якій перед кожним перекладом рядка (`\r\n` `\n\r` `\n`и`\r`) вставлен`<br />`или`<br>`

### Список параметрів

`string`

Вхідний рядок.

`use_xhtml`

Чи використовувати сумісні з XHTML переклади рядків чи ні.

### Значення, що повертаються

Повертає змінений рядок.

### Приклади

**Приклад #1 Приклад використання** nl2br()\*\*\*\*

```php
<?php
echo nl2br("foo - это вам не\n bar");
?>
```

Результат виконання наведеного прикладу:

```
foo - это вам не<br />
 bar
```

**Приклад #2 Генерування коректної HTML-верстки за допомогою параметра `use_xhtml`**

```php
<?php
echo nl2br("Привет!\r\nЭтой мой HTML-документ", false);
?>
```

Результат виконання наведеного прикладу:

```
Привет!<br>
Этой мой HTML-документ
```

**Приклад #3 Різні роздільники рядків**

```php
<?php
$string = "This\r\nis\n\ra\nstring\r";
echo nl2br($string);
?>
```

Результат виконання наведеного прикладу:

```
This<br />
is<br />
a<br />
string<br />
```

### Дивіться також

-   [htmlspecialchars()](function.mdspecialchars.md) \- Перетворює спеціальні символи в HTML-сутності
-   [htmlentities()](function.mdentities.md) \- Перетворює всі можливі символи у відповідні HTML-сутності
-   [wordwrap()](function.wordwrap.md) \- Переносить рядок за вказаною кількістю символів
-   [str\_replace()](function.str-replace.md) \- Замінює всі входження рядка пошуку на рядок заміни
