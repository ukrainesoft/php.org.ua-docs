Перевіряє, чи існує метод у даному класі

-   [« issubclassоф](function.is-subclass-of.html)
    
-   [propertyexists »](function.property-exists.html)
    
-   [PHP Manual](index.md)
    
-   [Функції роботи з класами та об'єктами](ref.classobj.md)
    
-   Перевіряє, чи існує метод у даному класі
    

# методexists

(PHP 4, PHP 5, PHP 7, PHP 8)

методexists — Перевіряє, чи існує метод у цьому класі

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

**Приклад #1 Приклад використання **методexists()****

```php
<?php
$directory = new Directory('.');
var_dump(method_exists($directory,'read'));
?>
```

Результат виконання цього прикладу:

```
bool(true)
```

**Приклад #2 Приклад статичного використання **методexists()****

```php
<?php
var_dump(method_exists('Directory','read'));
?>
```

Результат виконання цього прикладу:

```
bool(true)
```

### Примітки

> **Зауваження**
> 
> Виклик цієї функції буде використовувати всі зареєстровані [функции автозагрузки](language.oop5.autoload.md)якщо клас ще не відомий.

### Дивіться також

-   [functionexists()](function.function-exists.html) - Повертає true, якщо вказана функція визначена
-   [ісcallable()](function.is-callable.html) - Перевіряє, що значення може бути викликане як функція у поточній області видимості
-   [classexists()](function.class-exists.html) - Перевіряє, чи був оголошений клас