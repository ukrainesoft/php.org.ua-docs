---
navigation:
  - function.is-resource.md: « is\_resource
  - function.is-string.md: is\_string »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: is\_scalar
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# is\_scalar

(PHP 4 >= 4.0.5, PHP 5, PHP 7, PHP 8)

is\_scalar — Перевіряє, чи є змінна скаляр.

### Опис

```methodsynopsis
is_scalar(mixed $value): bool
```

Перевіряє, чи є змінна скаляр.

Скалярні змінні - це змінні, що містять int, float, string та bool. Типи array, object, resource і null - не скалярні.

> **Зауваження** :
> 
> Функция**is\_scalar()** не вважає ресурси (resource) скалярними значеннями, оскільки ресурси - це абстрактні типи даних, які поки що засновані на цілих числах (int). Покладатися на цю деталь не потрібно, оскільки не виключено, що в майбутньому функція розглядатиме ресурси по-іншому.

> **Зауваження** :
> 
> Функция**is\_scalar()** не вважає NULL скаляром.

### Список параметрів

`value`

Перевірена змінна.

### Значення, що повертаються

Повертає **`true`**, если значение`value`— скаляр, иначе\*\*`false`\*\*

### Приклади

**Приклад #1 Приклад использования функции**is\_scalar()\*\*\*\*

```php
<?php

function show_var($var)
{
    if (is_scalar($var)) {
        echo $var;
    } else {
        var_dump($var);
    }
}
$pi = 3.1416;
$proteins = array("hemoglobin", "cytochrome c oxidase", "ferredoxin");

show_var($pi);
show_var($proteins)

?>
```

Результат виконання наведеного прикладу:

```
3.1416
array(3) {
  [0]=>
  string(10) "hemoglobin"
  [1]=>
  string(20) "cytochrome c oxidase"
  [2]=>
  string(10) "ferredoxin"
}
```

### Дивіться також

-   [is\_float()](function.is-float.md) \- Перевіряє, чи є змінна число з плаваючою точкою
-   [is\_int()](function.is-int.md) \- Перевіряє, чи є змінна ціла кількість
-   [is\_numeric()](function.is-numeric.md) \- Перевіряє, чи містить змінне число чи числове рядок
-   [is\_real()](function.is-real.md) \- Псевдонім is\_float
-   [is\_string()](function.is-string.md) \- Перевіряє, чи є тип змінної рядок
-   [is\_bool()](function.is-bool.md) \- Перевіряє, чи є змінна логічне значення
-   [is\_object()](function.is-object.md) \- Перевіряє, чи є змінна об'єкт
-   [is\_array()](function.is-array.md) \- Визначає, чи є змінна масив
