---
navigation:
  - function.mb-encode-numericentity.md: « mb\_encode\_numericentity
  - function.mb-ereg-match.md: mb\_ereg\_match »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_encoding\_aliases
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_encoding\_aliases

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

mb\_encoding\_aliases — Отримує псевдоніми відомого типу кодування

### Опис

```methodsynopsis
mb_encoding_aliases(string $encoding): array
```

Повертає масив псевдонімів для відомого типу кодування `encoding`

### Список параметрів

`encoding`

Кодування, для якого будуть перевірені псевдоніми.

### Значення, що повертаються

Повертає індексований масив, що містить псевдоніми кодування.

### Помилки

Викидає виняток [ValueError](class.valueerror.md), якщо кодування `encoding` невідома.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Якщо параметр `encoding` невідомий, тепер викидається виняток [ValueError](class.valueerror.md); раніше видавалася помилка рівня **`E_WARNING`** та функція повертала **`false`** |

### Приклади

**Приклад #1 Приклад использования функции**mb\_encoding\_aliases()\*\*\*\*

```php
<?php
$encoding        = 'ASCII';
$known_encodings = mb_list_encodings();

if (in_array($encoding, $known_encodings)) {

    $aliases = mb_encoding_aliases($encoding);
    print_r($aliases);

} else {

    echo "Неизвестная кодировка ($encoding).\n";

}
?>
```

Висновок наведеного прикладу буде схожим на:

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

-   [mb\_list\_encodings()](function.mb-list-encodings.md) \- Повертає масив усіх кодувань, що підтримуються.
