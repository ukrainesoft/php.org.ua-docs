Перевіряє, чи був оголошений клас

-   [« class\_alias](function.class-alias.html)
    
-   [enum\_exists »](function.enum-exists.html)
    
-   [PHP Manual](index.html)
    
-   [Функции работы с классами и объектами](ref.classobj.html)
    
-   Перевіряє, чи був оголошений клас
    

# classexists

(PHP 4, PHP 5, PHP 7, PHP 8)

classexists — Перевіряє, чи був оголошений клас

### Опис

```methodsynopsis
class_exists(string $class, bool $autoload = true): bool
```

Ця функція перевіряє, чи був оголошений зазначений клас чи ні.

### Список параметрів

`class`

Назва класу. Сприймається без урахування регістру.

`autoload`

Чи викликати за замовчуванням [\_\_autoload](language.oop5.autoload.html)

### Значення, що повертаються

Повертає **`true`**, якщо клас `class` оголошено, інакше **`false`**

### Приклади

**Приклад #1 Приклад використання **classexists()****

```php
<?php
// Проверяем существование класса перед его использованием
if (class_exists('MyClass')) {
    $myclass = new MyClass();
}

?>
```

**Приклад #2 Приклад використання з параметром `autoload`**

```php
<?php
spl_autoload_register(function ($class_name) {
    include $class_name . '.php';

    // Проверяем необходимость подключения указанного класса
    if (!class_exists($class_name, false)) {
        throw new LogicException("Unable to load class: $class_name");
    }
});

if (class_exists(MyClass::class)) {
    $myclass = new MyClass();
}

?>
```

### Дивіться також

-   [function\_exists()](function.function-exists.html) - Повертає true, якщо вказана функція визначена
-   [enum\_exists()](function.enum-exists.html) - Перевіряє, чи визначено перерахування
-   [interface\_exists()](function.interface-exists.html) - Перевіряє, чи визначено інтерфейс
-   [get\_declared\_classes()](function.get-declared-classes.html) - Повертає масив із іменами оголошених класів