Копіює метод з одного класу до іншого

-   [« runkit7methodadd](function.runkit7-method-add.html)
    
-   [runkit7methodredefine »](function.runkit7-method-redefine.html)
    
-   [PHP Manual](index.html)
    
-   [Функції runkit7](ref.runkit7.html)
    
-   Копіює метод з одного класу до іншого
    

# runkit7методcopy

(PECL runkit7> = Unknown)

runkit7методcopy — Копіює метод з одного класу до іншого

### Опис

```methodsynopsis
runkit7_method_copy(    string $destination_class,    string $destination_method_name,    string $source_class,    string $source_method_name = ?): bool
```

### Список параметрів

`destination_class`

Цільовий клас для скопійованого методу.

`destination_method_name`

Назва методу призначення.

`source_class`

Початковий клас скопійованого методу.

`source_method_name`

Ім'я методу копіювання з вихідного класу. Якщо цей параметр опущено, передбачається значення `destination_method_name`

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **runkit7методcopy()****

```php
<?php
class Foo {
    function example() {
        return "foo!\n";
    }
}

class Bar {
    // изначально никаких методов
}

// копирование метода example() из класса Foo в класс Bar как baz()
runkit7_method_copy('Bar', 'baz', 'Foo', 'example');

// функция вывода скопирована
echo Bar::baz();
?>
```

Результат виконання цього прикладу:

```
foo!
```

### Дивіться також

-   [runkit7methodadd()](function.runkit7-method-add.html) - Динамічно додає новий метод у заданий клас
-   [runkit7methodredefine()](function.runkit7-method-redefine.html) - динамічно змінює код заданого методу
-   [runkit7methodremove()](function.runkit7-method-remove.html) - динамічно видаляє заданий метод
-   [runkit7methodrename()](function.runkit7-method-rename.html) - динамічно змінює ім'я заданого методу
-   [runkit7functioncopy()](function.runkit7-function-copy.html) - Копіює функцію в нове ім'я функції