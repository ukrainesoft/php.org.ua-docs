---
navigation:
  - function.runkit7-method-redefine.md: « runkit7methodredefine
  - function.runkit7-method-rename.md: runkit7methodrename »
  - index.md: PHP Manual
  - ref.runkit7.md: Функції runkit7
title: runkit7методremove
---
# runkit7методremove

(PECL runkit7> = Unknown)

runkit7методremove - Динамічно видаляє заданий метод

### Опис

```methodsynopsis
runkit7_method_remove(string $class_name, string $method_name): bool
```

> **Зауваження**: Ця функція не може бути використана для впливу на працюючі в даний момент (або ланцюгові) методи.

### Список параметрів

`class_name`

Клас, де потрібно видалити метод.

`method_name`

Ім'я методу, що видаляється.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **runkit7методremove()****

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

Результат виконання цього прикладу:

```
bar
```

### Дивіться також

-   [runkit7methodadd()](function.runkit7-method-add.md) - Динамічно додає новий метод у заданий клас
-   [runkit7methodcopy()](function.runkit7-method-copy.md) - Копіює метод з одного класу до іншого
-   [runkit7methodredefine()](function.runkit7-method-redefine.md) - динамічно змінює код заданого методу
-   [runkit7methodrename()](function.runkit7-method-rename.md) - динамічно змінює ім'я заданого методу
-   [runkit7functionremove()](function.runkit7-function-remove.md) - Видаляє визначення функції
