Замінює визначення функції новою реалізацією

-   [« runkit7\_function\_copy](function.runkit7-function-copy.html)
    
-   [runkit7\_function\_remove »](function.runkit7-function-remove.html)
    
-   [PHP Manual](index.html)
    
-   [Функции runkit7](ref.runkit7.html)
    
-   Замінює визначення функції новою реалізацією
    

# runkit7functionredefine

(PECL runkit7> = Unknown)

runkit7functionredefine - Замінює визначення функції новою реалізацією

### Опис

```methodsynopsis
runkit7_function_redefine(    string $function_name,    string $argument_list,    string $code,    bool $return_by_reference = null,    string $doc_comment = null,    string $return_type = ?,    bool $is_strict = ?): bool
```

```methodsynopsis
runkit7_function_redefine(    string $function_name,    Closure $closure,    string $doc_comment = null,    string $return_type = ?,    bool $is_strict = ?): bool
```

> **Зауваження**: За замовчуванням, лише функції користувача можуть бути видалені, перейменовані або змінені. Для перекриття внутрішніх функцій, необхідно включити до php.ini опцію `runkit.internal_override`

### Список параметрів

`function_name`

Ім'я функції для перевизначення.

`argument_list`

Новий список аргументів, які приймає функція.

`code`

Реалізація нового коду.

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

**Приклад #1 Приклад використання **runkit7functionredefine()****

```php
<?php
function testme() {
  echo "Оригинальная реализация Testme\n";
}
testme();
runkit7_function_redefine('testme','','echo "Новая реализация Testme\n";');
testme();
?>
```

Результат виконання цього прикладу:

```
Оригинальная реализация Testme
Новая реализация Testme
```

### Дивіться також

-   [runkit7\_function\_add()](function.runkit7-function-add.html) - Додає нову функцію, функція аналогічна createfunction
-   [runkit7\_function\_copy()](function.runkit7-function-copy.html) - Копіює функцію в нове ім'я функції
-   [runkit7\_function\_rename()](function.runkit7-function-rename.html) - Змінює ім'я функції
-   [runkit7\_function\_remove()](function.runkit7-function-remove.html) - Видаляє визначення функції
-   [runkit7\_method\_redefine()](function.runkit7-method-redefine.html) - динамічно змінює код заданого методу