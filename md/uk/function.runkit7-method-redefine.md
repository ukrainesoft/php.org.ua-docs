---
navigation:
  - function.runkit7-method-copy.html: « runkit7methodcopy
  - function.runkit7-method-remove.html: runkit7methodremove »
  - index.html: PHP Manual
  - ref.runkit7.html: Функції runkit7
title: runkit7методredefine
---
# runkit7методredefine

(PECL runkit7> = Unknown)

runkit7методredefine - Динамічно змінює код заданого методу

### Опис

```methodsynopsis
runkit7_method_redefine(    string $class_name,    string $method_name,    string $argument_list,    string $code,    int $flags = RUNKIT7_ACC_PUBLIC,    string $doc_comment = null,    string $return_type = ?,    bool $is_strict = ?): bool
```

```methodsynopsis
runkit7_method_redefine(    string $class_name,    string $method_name,    Closure $closure,    int $flags = RUNKIT7_ACC_PUBLIC,    string $doc_comment = null,    string $return_type = ?,    bool $is_strict = ?): bool
```

### Список параметрів

`class_name`

Клас, у якому необхідно перевизначити спосіб.

`method_name`

Ім'я методу, який необхідно перевизначити.

`argument_list`

Розділений комами список аргументів для перевизначеного методу.

`code`

Новий код, який буде виконуватись під час виклику `method_name`

`closure`

Замикання ([closure](class.closure.html)), Що визначає метод.

`flags`

Перевизначений метод може бути **`RUNKIT7_ACC_PUBLIC`** **`RUNKIT7_ACC_PROTECTED`** або **`RUNKIT7_ACC_PRIVATE`**, і, при необхідності, об'єднаний за допомогою побітового АБО з **`RUNKIT7_ACC_STATIC`**

`doc_comment`

Документальний коментар методу.

`return_type`

Тип значення методу, що повертається.

`is_strict`

Визначає, чи буде метод поводитися так, якби він був оголошений у файлі з `strict_types=1`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **runkit7методredefine()****

```php
<?php
class Example {
    function foo() {
        return "foo!\n";
    }
}

// создание объекта Example
$e = new Example();

// вывод Example::foo() (до переопределения)
echo "До: " . $e->foo();

// Переопределение метода 'foo'
runkit7_method_redefine(
    'Example',
    'foo',
    '',
    'return "bar!\n";',
    RUNKIT7_ACC_PUBLIC
);

// вывод Example::foo() (после переопределения)
echo "После: " . $e->foo();
?>
```

Результат виконання цього прикладу:

```
До: foo!
После: bar!
```

### Дивіться також

-   [runkit7methodadd()](function.runkit7-method-add.html) - Динамічно додає новий метод у заданий клас
-   [runkit7methodcopy()](function.runkit7-method-copy.html) - Копіює метод з одного класу до іншого
-   [runkit7methodremove()](function.runkit7-method-remove.html) - динамічно видаляє заданий метод
-   [runkit7methodrename()](function.runkit7-method-rename.html) - динамічно змінює ім'я заданого методу
-   [runkit7functionredefine()](function.runkit7-function-redefine.html) - замінює визначення функції новою реалізацією
