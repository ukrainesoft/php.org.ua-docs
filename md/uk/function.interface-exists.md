---
navigation:
  - function.get-parent-class.md: « getparentclass
  - function.is-a.md: ісa »
  - index.md: PHP Manual
  - ref.classobj.md: Функції роботи з класами та об'єктами
title: interfaceexists
---
# interfaceexists

(PHP 5> = 5.0.2, PHP 7, PHP 8)

interfaceexists — Перевіряє, чи визначено інтерфейс.

### Опис

```methodsynopsis
interface_exists(string $interface, bool $autoload = true): bool
```

Перевіряє, чи вказаний інтерфейс.

### Список параметрів

`interface`

Ім'я інтерфейсу

`autoload`

Визначає, чи використовувати за промовчанням [autoload](language.oop5.autoload.md) чи ні

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо інтерфейс c заданим ім'ям `interface` був визначений або **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **interfaceexists()****

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

-   [getdeclaredinterfaces()](function.get-declared-interfaces.md) - Повертає масив усіх оголошених інтерфейсів
-   [classimplements()](function.class-implements.md) - Повертає список інтерфейсів, реалізованих у заданому класі чи інтерфейсі
-   [classexists()](function.class-exists.md) - Перевіряє, чи був оголошений клас
-   [enumexists()](function.enum-exists.md) - Перевіряє, чи визначено перерахування
