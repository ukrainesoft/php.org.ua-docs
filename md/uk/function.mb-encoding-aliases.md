---
navigation:
  - function.mb-encode-numericentity.html: « mbencodenumericentity
  - function.mb-ereg-match.html: мбeregmatch »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: мбencodingaliases
---
# мбencodingaliases

(PHP 5> = 5.3.0, PHP 7, PHP 8)

мбencodingaliases — Отримує псевдоніми відомого типу кодування

### Опис

```methodsynopsis
mb_encoding_aliases(string $encoding): array
```

Повертає масив псевдонімів для відомого типу кодування `encoding`

### Список параметрів

`encoding`

Кодування, для якого шукаються псевдоніми.

### Значення, що повертаються

У разі успішного виконання повертає індексний масив із псевдонімами кодування або **`false`** у разі виникнення помилки

### Помилки

Викликає помилку рівня **`E_WARNING`**, якщо кодування `encoding` невідома.

### Приклади

**Приклад #1 Приклад використання **мбencodingaliases()****

```php
<?php
$encoding        = 'ASCII';
$known_encodings = mb_list_encodings();

if (in_array($encoding, $known_encodings)) {

    $aliases = mb_encoding_aliases($encoding);
    print_r($aliases);

} else {

    echo "Неизвестная кодировка ($encoding).\n";

}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [0] => ANSI_X3.4-1968
    [1] => iso-ir-6
    [2] => ANSI_X3.4-1986
    [3] => ISO_646.irv:1991
    [4] => US-ASCII
    [5] => ISO646-US
    [6] => us
    [7] => IBM367
    [8] => cp367
    [9] => csASCII
)
```

### Дивіться також

-   [мбlistencodings()](function.mb-list-encodings.md) - Повертає масив усіх кодувань, що підтримуються.
