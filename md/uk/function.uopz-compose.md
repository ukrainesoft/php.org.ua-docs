---
navigation:
  - function.uopz-backup.md: « uopz\_backup
  - function.uopz-copy.md: uopz\_copy »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopz\_compose
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uopz\_compose

(PECL uopz 1, PECL uopz 2)

uopz\_compose — Скласти клас

**Увага**

Ця функція була *ВИДАЛЕНО*в PECL uopz 5.0.0.

### Опис

```methodsynopsis
uopz_compose(    string $name,    array $classes,    array $methods = ?,    array $properties = ?,    int $flags = ?): void
```

Створює клас заданого імені, який реалізує, успадковує чи використовує всі надані класи

### Список параметрів

`name`

Коректне ім'я класу

`classes`

Масив імен класів, інтерфейсів та трейтів

`methods`

Асоціативний масив методів, де значення або замикання, або представлені структурою \[модифікатори => замикання\]

`properties`

Асоціативний масив властивостей, де ключі – імена, а значення – модифікатори

`flags`

Тип запису за замовчуванням ZEND\_ACC\_CLASS

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання** uopz\_compose()\*\*\*\*

```php
<?php
class myClass {}
trait myTrait {}
interface myInterface {}

uopz_compose(
    Composed::class, [
        myClass::class,
        myTrait::class,
        myInterface::class
    ], [
    "__construct" => function() {
        /* ... */
    }
]);

var_dump(
 class_uses(Composed::class),
 class_parents(Composed::class),
 class_implements(Composed::class));
?>
```

Результат виконання наведеного прикладу:

```
array(1) {
  ["myTrait"]=>
  string(7) "myTrait"
}
array(1) {
  ["myClass"]=>
  string(7) "myClass"
}
array(1) {
  ["myInterface"]=>
  string(11) "myInterface"
}
```
