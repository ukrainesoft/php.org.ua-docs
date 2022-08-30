Перевіряє, чи є змінна скалярним значенням

-   [« isresource](function.is-resource.html)
    
-   [ісstring »](function.is-string.html)
    
-   [PHP Manual](index.md)
    
-   [Функції для роботи зі змінними](ref.var.md)
    
-   Перевіряє, чи є змінна скалярним значенням
    

# ісscalar

(PHP 4> = 4.0.5, PHP 5, PHP 7, PHP 8)

ісscalar — Перевіряє, чи є змінна скалярним значенням

### Опис

```methodsynopsis
is_scalar(mixed $value): bool
```

Перевіряє, чи є змінна скалярним значенням.

Скалярні змінні – це змінні з типами int, float, string та bool. Типи array, object, resource і null є скалярними.

> **Зауваження**
> 
> **ісscalar()** не вважає змінні типу resource скалярними, оскільки ресурси є абстрактними типами даних, що у час засновані цілому типі. Не варто покладатися на цю деталь реалізації, оскільки вона може змінитися.

> **Зауваження**
> 
> **ісscalar()** не вважає NULL скаляром.

### Список параметрів

`value`

Перевірена змінна.

### Значення, що повертаються

Повертає **`true`**, якщо `value` є скалярним значенням, або **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **ісscalar()****

```php
<?php
function show_var($var)
{
    if (is_scalar($var)) {
        echo $var;
    } else {
        var_dump($var);
    }
}
$pi = 3.1416;
$proteins = array("hemoglobin", "cytochrome c oxidase", "ferredoxin");

show_var($pi);
show_var($proteins)

?>
```

Результат виконання цього прикладу:

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

-   [ісfloat()](function.is-float.html) - Перевіряє, чи є змінна числом із плаваючою точкою
-   [ісint()](function.is-int.html) - Перевіряє, чи є змінна цілим числом
-   [ісnumeric()](function.is-numeric.html) - Перевіряє, чи є змінна числом або рядком, що містить число
-   [ісreal()](function.is-real.html) - Псевдонім isfloat
-   [ісstring()](function.is-string.html) - Перевіряє, чи є змінним рядком
-   [ісbool()](function.is-bool.html) - Перевіряє, чи є змінна булевою
-   [ісobject()](function.is-object.html) - Перевіряє, чи є змінна об'єктом
-   [ісarray()](function.is-array.html) - Визначає, чи є змінна масивом