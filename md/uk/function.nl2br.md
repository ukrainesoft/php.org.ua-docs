Вставляє HTML код розриву рядка перед кожним перекладом рядка

-   [« nl\_langinfo](function.nl-langinfo.html)
    
-   [number\_format »](function.number-format.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы со строками](ref.strings.html)
    
-   Вставляє HTML код розриву рядка перед кожним перекладом рядка
    

# nl2br

(PHP 4, PHP 5, PHP 7, PHP 8)

nl2br — Вставляє HTML код розриву рядка перед кожним перекладом рядка

### Опис

```methodsynopsis
nl2br(string $string, bool $use_xhtml = true): string
```

Повертає рядок `string`, в якій перед кожним перекладом рядка (`\r\n` `\n\r` `\n` і `\r`) вставлений `<br />` або `<br>`

### Список параметрів

`string`

Вхідний рядок.

`use_xhtml`

Чи використовувати сумісні з XHTML переклади рядків чи ні.

### Значення, що повертаються

Повертає змінений рядок.

### Приклади

**Приклад #1 Приклад використання **nl2br()****

```php
<?php
echo nl2br("foo - это вам не\n bar");
?>
```

Результат виконання цього прикладу:

```
foo - это вам не<br />
 bar
```

**Приклад #2 Генерування коректної HTML-верстки за допомогою параметра `use_xhtml`**

```php
<?php
echo nl2br("Привет!\r\nЭтой мой HTML-документ", false);
?>
```

Результат виконання цього прикладу:

```
Привет!<br>
Этой мой HTML-документ
```

**Приклад #3 Різні роздільники рядків**

```php
<?php
$string = "This\r\nis\n\ra\nstring\r";
echo nl2br($string);
?>
```

Результат виконання цього прикладу:

```
This<br />
is<br />
a<br />
string<br />
```

### Дивіться також

-   [htmlspecialchars()](function.htmlspecialchars.html) - Перетворює спеціальні символи на HTML-сутності
-   [htmlentities()](function.htmlentities.html) - Перетворює всі можливі символи у відповідні HTML-сутності
-   [wordwrap()](function.wordwrap.html) - Переносить рядок за вказаною кількістю символів
-   [str\_replace()](function.str-replace.html) - Замінює всі входження рядка пошуку на рядок заміни