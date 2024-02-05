---
navigation:
  - function.is-subclass-of.md: « is\_subclass\_of
  - function.property-exists.md: property\_exists »
  - index.md: PHP Manual
  - ref.classobj.md: Функції роботи з класами та об'єктами
title: method\_exists
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# method\_exists

(PHP 4, PHP 5, PHP 7, PHP 8)

method\_exists — Перевіряє, чи існує метод у цьому класі

### Опис

```methodsynopsis
method_exists(object|string $object_or_class, string $method): bool
```

Перевіряє, чи існує метод класу у вказаному об'єкті `object_or_class`

### Список параметрів

`object_or_class`

Примірник об'єкта або ім'я класу

`method`

Ім'я методу

### Значення, що повертаються

Повертає **`true`**, якщо метод `method` визначено для зазначеного об'єкта `object_or_class`, інакше повертає **`false`**

### Приклади

**Приклад #1 Приклад використання** method\_exists()\*\*\*\*

```php
<?php
$directory = new Directory('.');
var_dump(method_exists($directory,'read'));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
```

**Приклад #2 Приклад статичного використання **method\_exists()****

```php
<?php
var_dump(method_exists('Directory','read'));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
```

### Примітки

> **Зауваження** :
> 
> Виклик цієї функції буде використовувати всі зареєстровані [функції автозавантаження](language.oop5.autoload.md)якщо клас ще не відомий.

### Дивіться також

-   [function\_exists()](function.function-exists.md) \- Повертає true, якщо вказана функція визначена
-   [is\_callable()](function.is-callable.md) \- Перевіряє, що значення може бути викликане як функція у поточній області видимості
-   [class\_exists()](function.class-exists.md) \- Перевіряє, чи був оголошений клас
