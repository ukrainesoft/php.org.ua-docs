Додає нову функцію, функція аналогічна createfunction

-   [« runkit7\_constant\_remove](function.runkit7-constant-remove.html)
    
-   [runkit7\_function\_copy »](function.runkit7-function-copy.html)
    
-   [PHP Manual](index.html)
    
-   [Функции runkit7](ref.runkit7.html)
    
-   Додає нову функцію, функція аналогічна createfunction
    

# runkit7functionadd

(PECL runkit7> = Unknown)

runkit7functionadd - Додає нову функцію, функція аналогічна [create\_function()](function.create-function.html)

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

Замикання ([closure](class.closure.html)), Що визначає функцію.

`return_by_reference`

Визначає, чи функція повинна повертатися за посиланням.

`doc_comment`

Документальний коментар функції.

`return_type`

Тип значення функції, що повертається.

`is_strict`

Визначає, чи повинна функція поводитися так, якби вона була оголошена у файлі з `strict_types=1`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **runkit7functionadd()****

```php
<?php
runkit7_function_add('testme','$a,$b','echo "Значение A - $a\n"; echo "Значение B - $b\n";');
testme(1,2);
?>
```

Результат виконання цього прикладу:

```
Значение A - 1
Значение B - 2
```

### Дивіться також

-   [create\_function()](function.create-function.html) - Створює функцію динамічно, оцінюючи рядок коду
-   [runkit7\_function\_redefine()](function.runkit7-function-redefine.html) - замінює визначення функції новою реалізацією
-   [runkit7\_function\_copy()](function.runkit7-function-copy.html) - Копіює функцію в нове ім'я функції
-   [runkit7\_function\_rename()](function.runkit7-function-rename.html) - Змінює ім'я функції
-   [runkit7\_function\_remove()](function.runkit7-function-remove.html) - Видаляє визначення функції
-   [runkit7\_method\_add()](function.runkit7-method-add.html) - Динамічно додає новий метод у заданий клас