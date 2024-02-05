---
navigation:
  - function.intval.md: « intval
  - function.is-bool.md: is\_bool »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: is\_array
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# is\_array

(PHP 4, PHP 5, PHP 7, PHP 8)

is\_array — Визначає, чи є змінна масив

### Опис

```methodsynopsis
is_array(mixed $value): bool
```

Визначає, чи є змінна масив.

### Список параметрів

`value`

Перевірена змінна.

### Значення, що повертаються

Повертає **`true`**, если переменная`value` - масив (array), інакше **`false`**

### Приклади

**Приклад #1 Приклад перевірки того, що змінна масив**

```php
<?php

$yes = array('это', 'массив');

echo is_array($yes) ? 'Массив' : 'Не массив';
echo "\n";

$no = 'это строка';

echo is_array($no) ? 'Массив' : 'Не массив';

?>
```

Результат виконання наведеного прикладу:

```
Массив
Не массив
```

### Дивіться також

-   [array\_is\_list()](function.array-is-list.md) \- Перевіряє, чи є даний array списком
-   [is\_float()](function.is-float.md) \- Перевіряє, чи є змінна число з плаваючою точкою
-   [is\_int()](function.is-int.md) \- Перевіряє, чи є змінна ціла кількість
-   [is\_string()](function.is-string.md) \- Перевіряє, чи є тип змінної рядок
-   [is\_object()](function.is-object.md) \- Перевіряє, чи є змінна об'єкт
