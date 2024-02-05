---
navigation:
  - function.autoload.md: « \_\_autoload
  - function.class-exists.md: class\_exists »
  - index.md: PHP Manual
  - ref.classobj.md: Функції роботи з класами та об'єктами
title: class\_alias
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# class\_alias

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

class\_alias — Створює псевдонім для вказаного класу

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

Чи потрібно [автоматично підвантажувати](language.oop5.autoload.md) клас, якщо він ще не завантажений.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**class\_alias()\*\*\*\*

```php
<?php

class Foo { }

class_alias('Foo', 'Bar');

$a = new Foo;
$b = new Bar;

// объекты одинаковы
var_dump($a == $b, $a === $b);
var_dump($a instanceof $b);

// классы одинаковы
var_dump($a instanceof Foo);
var_dump($a instanceof Bar);

var_dump($b instanceof Foo);
var_dump($b instanceof Bar);

?>
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(false)
bool(true)
bool(true)
bool(true)
bool(true)
bool(true)
```

### Примітки

> **Зауваження** :
> 
> Імена класів у PHP не залежать від регістру, що і відображено у цій функції. Псевдоніми, що створюються функцією **class\_alias()**, оголошуються у нижньому регістрі. Це означає, що для класу `MyClass` виклик `class_alias('MyClass', 'MyClassAlias')` оголосить новий псевдонім класу з ім'ям `myclassalias`

### Дивіться також

-   [get\_parent\_class()](function.get-parent-class.md) \- Повертає ім'я батьківського класу для об'єкта чи класу
-   [is\_subclass\_of()](function.is-subclass-of.md) \- Перевіряє, чи містить об'єкт у своєму дереві предків зазначений клас чи прямо реалізує його
