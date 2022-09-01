---
navigation:
  - splfixedarray.construct.md: '« SplFixedArray::construct'
  - splfixedarray.current.md: 'SplFixedArray::current »'
  - index.md: PHP Manual
  - class.splfixedarray.md: SplFixedArray
title: 'SplFixedArray::count'
---
# SplFixedArray::count

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SplFixedArray::count — Повертає розмір масиву

### Опис

```methodsynopsis
public SplFixedArray::count(): int
```

Повертає розмір масиву.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає розмір масиву.

### Приклади

**Приклад #1 Приклад **SplFixedArray::count()****

```php
<?php
$array = new SplFixedArray(5);
echo $array->count() . "\n";
echo count($array) . "\n";
?>
```

Результат виконання цього прикладу:

```
5
5
```

### Примітки

> **Зауваження**
> 
> Цей метод еквівалентний [SplFixedArray::getSize()](splfixedarray.getsize.md)

> **Зауваження**
> 
> Число елементів завжди дорівнює заданому розміру, т.к. всі значення спочатку ініціалізуються як **`null`**

### Дивіться також

-   [SplFixedArray::getSize()](splfixedarray.getsize.md) - Отримує розмір масиву
