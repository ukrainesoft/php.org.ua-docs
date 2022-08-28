Перевіряє, чи визначено інтерфейс

-   [« get\_parent\_class](function.get-parent-class.html)
    
-   [is\_a »](function.is-a.html)
    
-   [PHP Manual](index.html)
    
-   [Функции работы с классами и объектами](ref.classobj.html)
    
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

Визначає, чи використовувати за промовчанням [\_\_autoload](language.oop5.autoload.html) чи ні

### Значення, що повертаються

Повертає **`true`**якщо інтерфейс c заданим ім'ям `interface` був визначений або **`false`** в іншому випадку.

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

-   [get\_declared\_interfaces()](function.get-declared-interfaces.html) - Повертає масив усіх оголошених інтерфейсів
-   [class\_implements()](function.class-implements.html) - Повертає список інтерфейсів, реалізованих у заданому класі чи інтерфейсі
-   [class\_exists()](function.class-exists.html) - Перевіряє, чи був оголошений клас
-   [enum\_exists()](function.enum-exists.html) - Перевіряє, чи визначено перерахування