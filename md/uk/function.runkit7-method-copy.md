---
navigation:
  - function.runkit7-method-add.md: « runkit7\_method\_add
  - function.runkit7-method-redefine.md: runkit7\_method\_redefine »
  - index.md: PHP Manual
  - ref.runkit7.md: Функції runkit7
title: runkit7\_method\_copy
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# runkit7\_method\_copy

(PECL runkit7 >= Unknown)

runkit7\_method\_copy — Копіює метод з одного класу до іншого

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

**Пример #1 Пример использования**runkit7\_method\_copy()\*\*\*\*

```php
<?php
class Foo {
    function example() {
        return "foo!\n";
    }
}

class Bar {
    // изначально никаких методов
}

// копирование метода example() из класса Foo в класс Bar как baz()
runkit7_method_copy('Bar', 'baz', 'Foo', 'example');

// функция вывода скопирована
echo Bar::baz();
?>
```

Результат виконання наведеного прикладу:

```
foo!
```

### Дивіться також

-   [runkit7\_method\_add()](function.runkit7-method-add.md) \- Динамічно додає новий метод у заданий клас
-   [runkit7\_method\_redefine()](function.runkit7-method-redefine.md) \- динамічно змінює код заданого методу
-   [runkit7\_method\_remove()](function.runkit7-method-remove.md) \- динамічно видаляє заданий метод
-   [runkit7\_method\_rename()](function.runkit7-method-rename.md) \- динамічно змінює ім'я заданого методу
-   [runkit7\_function\_copy()](function.runkit7-function-copy.md) \- Копіює функцію в нове ім'я функції
