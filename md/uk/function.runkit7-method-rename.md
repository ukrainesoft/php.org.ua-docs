---
navigation:
  - function.runkit7-method-remove.md: « runkit7methodremove
  - function.runkit7-object-id.md: runkit7objectid »
  - index.md: PHP Manual
  - ref.runkit7.md: Функції runkit7
title: runkit7методrename
---
# runkit7методrename

(PECL runkit7> = Unknown)

runkit7методrename - Динамічно змінює ім'я заданого методу

### Опис

```methodsynopsis
runkit7_method_rename(string $class_name, string $source_method_name, string $target_method_name): bool
```

> **Зауваження**: Ця функція не може бути використана для впливу на працюючі в даний момент (або ланцюгові) методи.

### Список параметрів

`class_name`

Клас, у якому необхідно перейменувати спосіб.

`source_method_name`

Метод, який слід перейменувати.

`target_method_name`

Нове ім'я методу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **runkit7методrename()****

```php
<?php
class Example {
    function foo() {
        return "foo!\n";
    }
}

// Переименование метода 'foo' в 'bar'
runkit7_method_rename(
    'Example',
    'foo',
    'bar'
);

// Вывод переименованной функции
echo (new Example)->bar();
?>
```

Результат виконання цього прикладу:

```
foo!
```

### Дивіться також

-   [runkit7methodadd()](function.runkit7-method-add.md) - Динамічно додає новий метод у заданий клас
-   [runkit7methodcopy()](function.runkit7-method-copy.md) - Копіює метод з одного класу до іншого
-   [runkit7methodredefine()](function.runkit7-method-redefine.md) - динамічно змінює код заданого методу
-   [runkit7methodremove()](function.runkit7-method-remove.md) - динамічно видаляє заданий метод
-   [runkit7functionrename()](function.runkit7-function-rename.md) - Змінює ім'я функції
