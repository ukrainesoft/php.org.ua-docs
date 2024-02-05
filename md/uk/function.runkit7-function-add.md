---
navigation:
  - function.runkit7-constant-remove.md: « runkit7\_constant\_remove
  - function.runkit7-function-copy.md: runkit7\_function\_copy »
  - index.md: PHP Manual
  - ref.runkit7.md: Функції runkit7
title: runkit7\_function\_add
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# runkit7\_function\_add

(PECL runkit7 >= Unknown)

runkit7\_function\_add - Додає нову функцію, функція аналогічна [create\_function()](function.create-function.md)

### Опис

```methodsynopsis
runkit7_function_add(    string $function_name,    string $argument_list,    string $code,    bool $return_by_reference = null,    string $doc_comment = null,    string $return_type = ?,    bool $is_strict = ?): bool
```

```methodsynopsis
runkit7_function_add(    string $function_name,    Closure $closure,    string $doc_comment = null,    string $return_type = ?,    bool $is_strict = ?): bool
```

### Список параметрів

`function_name`

Ім'я функції, що створюється.

`argument_list`

Список аргументів, розділених комами.

`code`

Код, що становить функцію.

`closure`

Замикання ([closure](class.closure.md)), Що визначає функцію.

`return_by_reference`

Визначає, чи функція повинна повертатися за посиланням.

`doc_comment`

Документальний коментар функції.

`return_type`

Тип значення функції, що повертається.

`is_strict`

Визначає, чи повинна функція поводитися так, якби вона була оголошена у файлі з `strict_types=1`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** runkit7\_function\_add()\*\*\*\*

```php
<?php
runkit7_function_add('testme','$a,$b','echo "Значение A - $a\n"; echo "Значение B - $b\n";');
testme(1,2);
?>
```

Результат виконання наведеного прикладу:

```
Значение A - 1
Значение B - 2
```

### Дивіться також

-   [create\_function()](function.create-function.md) \- Створює функцію динамічно, оцінюючи рядок коду
-   [runkit7\_function\_redefine()](function.runkit7-function-redefine.md) \- замінює визначення функції новою реалізацією
-   [runkit7\_function\_copy()](function.runkit7-function-copy.md) \- Копіює функцію в нове ім'я функції
-   [runkit7\_function\_rename()](function.runkit7-function-rename.md) \- Змінює ім'я функції
-   [runkit7\_function\_remove()](function.runkit7-function-remove.md) \- Видаляє визначення функції
-   [runkit7\_method\_add()](function.runkit7-method-add.md) \- Динамічно додає новий метод у заданий клас
