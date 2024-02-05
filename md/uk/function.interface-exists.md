---
navigation:
  - function.get-parent-class.md: « get\_parent\_class
  - function.is-a.md: is\_a »
  - index.md: PHP Manual
  - ref.classobj.md: Функції роботи з класами та об'єктами
title: interface\_exists
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# interface\_exists

(PHP 5 >= 5.0.2, PHP 7, PHP 8)

interface\_exists — Перевіряє, чи визначено інтерфейс.

### Опис

```methodsynopsis
interface_exists(string $interface, bool $autoload = true): bool
```

Перевіряє, чи вказаний інтерфейс.

### Список параметрів

`interface`

Ім'я інтерфейсу

`autoload`

Чи потрібно [автоматично підвантажувати](language.oop5.autoload.md) інтерфейс, якщо він ще не завантажено.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо інтерфейс c заданим ім'ям `interface` був визначений або **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання** interface\_exists()\*\*\*\*

```php
<?php
// Проверяем существование интерфейса перед его использованием
if (interface_exists('MyInterface')) {
    class MyClass implements MyInterface
    {
        // Методы
    }
}

?>
```

### Дивіться також

-   [get\_declared\_interfaces()](function.get-declared-interfaces.md) \- Повертає масив усіх оголошених інтерфейсів
-   [class\_implements()](function.class-implements.md) \- Повертає список інтерфейсів, реалізованих у заданому класі чи інтерфейсі
-   [class\_exists()](function.class-exists.md) \- Перевіряє, чи був оголошений клас
-   [enum\_exists()](function.enum-exists.md) \- Перевіряє, чи визначено перерахування
