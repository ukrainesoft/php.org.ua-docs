---
navigation:
  - function.runkit7-method-remove.md: « runkit7\_method\_remove
  - function.runkit7-object-id.md: runkit7\_object\_id »
  - index.md: PHP Manual
  - ref.runkit7.md: Функції runkit7
title: runkit7\_method\_rename
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# runkit7\_method\_rename

(PECL runkit7 >= Unknown)

runkit7\_method\_rename - Динамічно змінює ім'я заданого методу

### Опис

```methodsynopsis
runkit7_method_rename(string $class_name, string $source_method_name, string $target_method_name): bool
```

> **Зауваження**: Цю функцію не можна використовувати для впливу на працюючі в цей момент (або ланцюгові) методи.

### Список параметрів

`class_name`

Клас, у якому необхідно перейменувати спосіб.

`source_method_name`

Метод, який слід перейменувати.

`target_method_name`

Нове ім'я методу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**runkit7\_method\_rename()\*\*\*\*

```php
<?php
class Example {
    function foo() {
        return "foo!\n";
    }
}

// Переименование метода 'foo' в 'bar'
runkit7_method_rename(
    'Example',
    'foo',
    'bar'
);

// Вывод переименованной функции
echo (new Example)->bar();
?>
```

Результат виконання наведеного прикладу:

```
foo!
```

### Дивіться також

-   [runkit7\_method\_add()](function.runkit7-method-add.md) \- Динамічно додає новий метод у заданий клас
-   [runkit7\_method\_copy()](function.runkit7-method-copy.md) \- Копіює метод з одного класу до іншого
-   [runkit7\_method\_redefine()](function.runkit7-method-redefine.md) \- динамічно змінює код заданого методу
-   [runkit7\_method\_remove()](function.runkit7-method-remove.md) \- динамічно видаляє заданий метод
-   [runkit7\_function\_rename()](function.runkit7-function-rename.md) \- Змінює ім'я функції
