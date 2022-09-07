---
navigation:
  - arrayobject.uasort.md: '« ArrayObject::uasort'
  - arrayobject.unserialize.md: 'ArrayObject::unserialize »'
  - index.md: PHP Manual
  - class.arrayobject.md: ArrayObject
title: 'ArrayObject::uksort'
---
# ArrayObject::uksort

(PHP 5> = 5.2.0, PHP 7, PHP 8)

ArrayObject::uksort — Сортувати масив за ключами, використовуючи функцію користувача для порівняння

### Опис

```methodsynopsis
public ArrayObject::uksort(callable $callback): bool
```

Ця функція сортує ключі записів за допомогою наданої користувачем функції. Відносини між ключами та елементами зберігаються.

> **Зауваження**
> 
> Якщо обидва порівнювані значення еквівалентні, вони зберігають свій початковий порядок. До PHP 8.0.0 їх відносний порядок у відсортованому масиві не було визначено.

### Список параметрів

`callback`

Функція порівняння повинна повертати ціле, яке менше, дорівнює чи більше нуля, якщо перший аргумент є відповідно меншим, рівним чи більшим, ніж другий.

```methodsynopsis
callback(mixed $a, mixed $b): int
```

### Значення, що повертаються

Функція завжди повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **ArrayObject::uksort()****

```php
<?php
function cmp($a, $b) {
    $a = preg_replace('@^(a|an|the) @', '', $a);
    $b = preg_replace('@^(a|an|the) @', '', $b);
    return strcasecmp($a, $b);
}

$array = array("John" => 1, "the Earth" => 2, "an apple" => 3, "a banana" => 4);
$arrayObject = new ArrayObject($array);
$arrayObject->uksort('cmp');

foreach ($arrayObject as $key => $value) {
    echo "$key: $value\n";
}
?>
```

Результат виконання цього прикладу:

```
an apple: 3
a banana: 4
the Earth: 2
John: 1
```

### Дивіться також

-   [ArrayObject::asort()](arrayobject.asort.md) - Сортувати записи за значенням
-   [ArrayObject::ksort()](arrayobject.ksort.md) - Сортувати записи за ключами
-   [ArrayObject::natsort()](arrayobject.natsort.md) - Сортувати масив, використовуючи алгоритм "natural order"
-   [ArrayObject::natcasesort()](arrayobject.natcasesort.md) - Сортувати масив, використовуючи реєстронезалежний алгоритм "natural order"
-   [ArrayObject::uasort()](arrayobject.uasort.md) - Сортувати записи, використовуючи функцію користувача для порівняння елементів і зберігаючи при цьому зв'язок ключ/значення
-   [uksort()](function.uksort.md) - Сортує масив за ключами, використовуючи функцію користувача для порівняння ключів
