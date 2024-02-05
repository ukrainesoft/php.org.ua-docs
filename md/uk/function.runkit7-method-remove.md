---
navigation:
  - function.runkit7-method-redefine.md: « runkit7\_method\_redefine
  - function.runkit7-method-rename.md: runkit7\_method\_rename »
  - index.md: PHP Manual
  - ref.runkit7.md: Функції runkit7
title: runkit7\_method\_remove
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# runkit7\_method\_remove

(PECL runkit7 >= Unknown)

runkit7\_method\_remove - Динамічно видаляє заданий метод

### Опис

```methodsynopsis
runkit7_method_remove(string $class_name, string $method_name): bool
```

> **Зауваження**: Цю функцію не можна використовувати для впливу на працюючі в цей момент (або ланцюгові) методи.

### Список параметрів

`class_name`

Клас, де потрібно видалити метод.

`method_name`

Ім'я методу, що видаляється.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**runkit7\_method\_remove()\*\*\*\*

```php
<?php
class Example {
    function foo() {
        return "foo!\n";
    }

    function bar() {
        return "bar!\n";
    }
}

// Remove the 'foo' method
runkit7_method_remove(
    'Example',
    'foo'
);

echo implode(' ', get_class_methods('Example'));

?>
```

Результат виконання наведеного прикладу:

```
bar
```

### Дивіться також

-   [runkit7\_method\_add()](function.runkit7-method-add.md) \- Динамічно додає новий метод у заданий клас
-   [runkit7\_method\_copy()](function.runkit7-method-copy.md) \- Копіює метод з одного класу до іншого
-   [runkit7\_method\_redefine()](function.runkit7-method-redefine.md) \- динамічно змінює код заданого методу
-   [runkit7\_method\_rename()](function.runkit7-method-rename.md) \- динамічно змінює ім'я заданого методу
-   [runkit7\_function\_remove()](function.runkit7-function-remove.md) \- Видаляє визначення функції
