---
navigation:
  - function.quoted-printable-encode.md: « quoted\_printable\_encode
  - function.rtrim.md: rtrim »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: quotemeta
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# quotemeta

(PHP 4, PHP 5, PHP 7, PHP 8)

quotemeta - Екранує спеціальні символи

### Опис

```methodsynopsis
quotemeta(string $string): string
```

Повертає модифікований рядок, у якому перед кожним символом із наступного списку:

. . \\ \* \[ \]

вставлений зворотний сліш (`\`

### Список параметрів

`string`

Вхідний рядок.

### Значення, що повертаються

Повертає екранований рядок або **`false`**, якщо як параметр `string` було вказано порожній рядок.

### Приклади

**Приклад #1 Приклад використання** quotemeta()\*\*\*\*

```php
<?php

var_dump(quotemeta('PHP is a popular scripting language. Fast, flexible, and pragmatic.'));
?>
```

Результат виконання наведеного прикладу:

```
string(69) "PHP is a popular scripting language\. Fast, flexible, and pragmatic\."
```

### Примітки

> **Зауваження**: Ця функція безпечна для обробки даних у двійковій формі.

### Дивіться також

-   [addslashes()](function.addslashes.md) \- Екранує рядок за допомогою слішів
-   [addcslashes()](function.addcslashes.md) \- Екранує рядок слішами у стилі мови C
-   [htmlentities()](function.mdentities.md) \- Перетворює всі можливі символи у відповідні HTML-сутності
-   [htmlspecialchars()](function.mdspecialchars.md) \- Перетворює спеціальні символи в HTML-сутності
-   [nl2br()](function.nl2br.md) \- Вставляє HTML код розриву рядка перед кожним перекладом рядка
-   [stripslashes()](function.stripslashes.md) \- Видаляє екранування символів
-   [stripcslashes()](function.stripcslashes.md) \- Видаляє екранування символів, зроблене функцією addcslashes
-   [preg\_quote()](function.preg-quote.md) \- Екранує символи у регулярних виразах
