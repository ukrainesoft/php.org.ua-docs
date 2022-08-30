Перевіряє, чи визначено інтерфейс

-   [« getparentclass](function.get-parent-class.html)
    
-   [ісa »](function.is-a.html)
    
-   [PHP Manual](index.html)
    
-   [Функції роботи з класами та об'єктами](ref.classobj.html)
    
-   Перевіряє, чи визначено інтерфейс
    

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

Визначає, чи використовувати за промовчанням [autoload](language.oop5.autoload.html) чи ні

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо інтерфейс c заданим ім'ям `interface` був визначений або **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **interfaceexists()****

```php
<?php
// Проверяем существование интерфейса перед его использованием
if (interface_exists('MyInterface')) {
    class MyClass implements MyInterface
    {
        // Методы
    }
}

?>
```

### Дивіться також

-   [getdeclaredinterfaces()](function.get-declared-interfaces.html) - Повертає масив усіх оголошених інтерфейсів
-   [classimplements()](function.class-implements.html) - Повертає список інтерфейсів, реалізованих у заданому класі чи інтерфейсі
-   [classexists()](function.class-exists.html) - Перевіряє, чи був оголошений клас
-   [enumexists()](function.enum-exists.html) - Перевіряє, чи визначено перерахування