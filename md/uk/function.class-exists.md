---
navigation:
  - function.class-alias.md: « class\_alias
  - function.enum-exists.md: enum\_exists »
  - index.md: PHP Manual
  - ref.classobj.md: Функції роботи з класами та об'єктами
title: class\_exists
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# class\_exists

(PHP 4, PHP 5, PHP 7, PHP 8)

class\_exists — Перевіряє, чи було оголошено клас

### Опис

```methodsynopsis
class_exists(string $class, bool $autoload = true): bool
```

Ця функція перевіряє, чи був оголошений зазначений клас чи ні.

### Список параметрів

`class`

Назва класу. Сприймається без урахування регістру.

`autoload`

Чи потрібно [автоматично підвантажувати](language.oop5.autoload.md) клас, якщо він ще не завантажений.

### Значення, що повертаються

Повертає **`true`**, якщо клас `class` оголошено, інакше **`false`**

### Приклади

**Пример #1 Пример использования**class\_exists()\*\*\*\*

```php
<?php
// Проверяем существование класса перед его использованием
if (class_exists('MyClass')) {
    $myclass = new MyClass();
}

?>
```

**Пример #2 Пример использования c параметром`autoload`**

```php
<?php
spl_autoload_register(function ($class_name) {
    include $class_name . '.php';

    // Проверяем необходимость подключения указанного класса
    if (!class_exists($class_name, false)) {
        throw new LogicException("Unable to load class: $class_name");
    }
});

if (class_exists(MyClass::class)) {
    $myclass = new MyClass();
}

?>
```

### Дивіться також

-   [function\_exists()](function.function-exists.md) \- Повертає true, якщо вказана функція визначена
-   [enum\_exists()](function.enum-exists.md) \- Перевіряє, чи визначено перерахування
-   [interface\_exists()](function.interface-exists.md) \- Перевіряє, чи визначено інтерфейс
-   [get\_declared\_classes()](function.get-declared-classes.md) \- Повертає масив із іменами оголошених класів
