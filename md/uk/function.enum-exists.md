- [«class_exists](function.class-exists.md)
- [get_called_class »](function.get-called-class.md)

- [PHP Manual](index.md)
- [Функції роботи з класами та об'єктами](ref.classobj.md)
- Перевіряє, чи визначено перерахування

#enum_exists

(PHP 8 \>= 8.1.0)

enum_exists — Перевіряє, чи визначено перерахування

### Опис

**enum_exists**(string `$enum`, bool `$autoload` = **`true`**): bool

Функція перевіряє, чи визначено цей перелік.

### Список параметрів

`enum`
Ім'я переліку. Ім'я зіставляється без урахування регістру.

`autoload`
Чи слід викликати [\_\_autoload](language.oop5.autoload.md)
замовчуванням.

### Значення, що повертаються

Повертає **`true`**, якщо перерахування `enum` визначено або
**`false`** інакше.

### Приклади

**Приклад #1 Приклад використання **enum_exists()****

`<?php// Переконайтеся, що перерахування існує, перш чем намагатися його використовуватиif (enum_exists(Suit::class)) {    $myclass = Suit::Hearts;}>

### Дивіться також

- [function_exists()](function.function-exists.md) - Повертає
true, якщо зазначена функція визначена
- [class_exists()](function.class-exists.md) - Перевіряє, чи був він
оголошено клас
- [interface_exists()](function.interface-exists.md) - Перевіряє,
чи визначено інтерфейс
- [get_declared_classes()](function.get-declared-classes.md) -
Повертає масив із іменами оголошених класів
