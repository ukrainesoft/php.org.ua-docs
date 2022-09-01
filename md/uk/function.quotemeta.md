---
navigation:
  - function.quoted-printable-encode.html: « quotedprintableencode
  - function.rtrim.html: rtrim »
  - index.html: PHP Manual
  - ref.strings.html: Функції для роботи з рядками
title: quotemeta
---
# quotemeta

(PHP 4, PHP 5, PHP 7, PHP 8)

quotemeta - Екранує спеціальні символи

### Опис

```methodsynopsis
quotemeta(string $string): string
```

Повертає модифікований рядок, у якому перед кожним символом із наступного списку:

. .

вставлений зворотний сліш (`\`

### Список параметрів

`string`

Вхідний рядок.

### Значення, що повертаються

Повертає екранований рядок або **`false`**, якщо як параметр `string` було вказано порожній рядок.

### Приклади

**Приклад #1 Приклад використання **quotemeta()****

```php
<?php

var_dump(quotemeta('PHP is a popular scripting language. Fast, flexible, and pragmatic.'));
?>
```

Результат виконання цього прикладу:

```
string(69) "PHP is a popular scripting language\. Fast, flexible, and pragmatic\."
```

### Примітки

> **Зауваження**: Ця функція безпечна для обробки даних у двійковій формі.

### Дивіться також

-   [addslashes()](function.addslashes.html) - Екранує рядок за допомогою слішів
-   [addcslashes()](function.addcslashes.html) - Екранує рядок слішами у стилі мови C
-   [htmlentities()](function.htmlentities.html) - Перетворює всі можливі символи у відповідні HTML-сутності
-   [htmlspecialchars()](function.htmlspecialchars.html) - Перетворює спеціальні символи на HTML-сутності
-   [nl2br()](function.nl2br.html) - Вставляє HTML код розриву рядка перед кожним перекладом рядка
-   [stripslashes()](function.stripslashes.html) - Видаляє екранування символів
-   [stripcslashes()](function.stripcslashes.html) - Видаляє екранування символів, зроблене функцією addcslashes
-   [pregquote()](function.preg-quote.html) - Екранує символи у регулярних виразах
