---
navigation:
  - function.autoload.html: autoload
  - function.class-exists.html: classexists »
  - index.html: PHP Manual
  - ref.classobj.html: Функції роботи з класами та об'єктами
title: classalias
---
# classalias

(PHP 5> = 5.3.0, PHP 7, PHP 8)

classalias — Створює псевдонім для вказаного класу

### Опис

```methodsynopsis
class_alias(string $class, string $alias, bool $autoload = true): bool
```

Створює псевдонім `alias` для класу користувача `class`. Новий клас із псевдонімом буде таким самим, як і оригінальний клас.

### Список параметрів

`class`

Оригінальний клас.

`alias`

Ім'я псевдоніму для класу.

`autoload`

Чи потрібно автоматично підвантажувати оригінальний клас, якщо його не було знайдено.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **classalias()****

```php
<?php

class foo { }

class_alias('foo', 'bar');

$a = new foo;
$b = new bar;

// объекты одинаковы
var_dump($a == $b, $a === $b);
var_dump($a instanceof $b);

// классы одинаковы
var_dump($a instanceof foo);
var_dump($a instanceof bar);

var_dump($b instanceof foo);
var_dump($b instanceof bar);

?>
```

Результат виконання цього прикладу:

```
bool(true)
bool(false)
bool(true)
bool(true)
bool(true)
bool(true)
bool(true)
```

### Дивіться також

-   [getparentclass()](function.get-parent-class.html) - Повертає ім'я батьківського класу для об'єкта чи класу
-   [ісsubclassof()](function.is-subclass-of.html) - Перевіряє, чи містить об'єкт у своєму дереві предків зазначений клас чи прямо реалізує його
