---
navigation:
  - function.serialize.md: « serialize
  - function.strval.md: strval »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: settype
---
# settype

(PHP 4, PHP 5, PHP 7, PHP 8)

settype — Задає тип змінної

### Опис

```methodsynopsis
settype(mixed &$var, string $type): bool
```

Задає тип `type` змінної `var`

### Список параметрів

`var`

Перетворювальна змінна.

`type`

Допустимими значеннями параметра `type` є:

-   "boolean" або "bool"
-   "integer" або "int"
-   "float" або "double"
-   "string"
-   "array"
-   "object"
-   "null"

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **settype()****

```php
<?php
$foo = "5bar"; // строка
$bar = true;   // булевое значение

settype($foo, "integer"); // $foo теперь 5   (целое)
settype($bar, "string");  // $bar теперь "1" (строка)
?>
```

### Примітки

> **Зауваження**
> 
> Максимальне значення для "int" одно **`PHP_INT_MAX`**

### Дивіться також

-   [gettype()](function.gettype.md) - Повертає тип змінної
-   [Приведение типов](language.types.type-juggling.md#language.types.typecasting)
-   [Маніпуляції з типами](language.types.type-juggling.md)
