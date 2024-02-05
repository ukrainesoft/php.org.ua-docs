---
navigation:
  - function.runkit7-method-copy.md: « runkit7\_method\_copy
  - function.runkit7-method-remove.md: runkit7\_method\_remove »
  - index.md: PHP Manual
  - ref.runkit7.md: Функції runkit7
title: runkit7\_method\_redefine
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# runkit7\_method\_redefine

(PECL runkit7 >= Unknown)

runkit7\_method\_redefine - Динамічно змінює код заданого методу

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

Замикання ([closure](class.closure.md)), Що визначає метод.

`flags`

Перевизначений метод може бути **`RUNKIT7_ACC_PUBLIC`** **`RUNKIT7_ACC_PROTECTED`**или**`RUNKIT7_ACC_PRIVATE`**, і, при необхідності, об'єднаний за допомогою побітового АБО з **`RUNKIT7_ACC_STATIC`**

`doc_comment`

Документальний коментар методу.

`return_type`

Тип значення методу, що повертається.

`is_strict`

Визначає, чи буде метод поводитися так, якби він був оголошений у файлі з `strict_types=1`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**runkit7\_method\_redefine()\*\*\*\*

```php
<?php
class Example {
    function foo() {
        return "foo!\n";
    }
}

// создание объекта Example
$e = new Example();

// вывод Example::foo() (до переопределения)
echo "До: " . $e->foo();

// Переопределение метода 'foo'
runkit7_method_redefine(
    'Example',
    'foo',
    '',
    'return "bar!\n";',
    RUNKIT7_ACC_PUBLIC
);

// вывод Example::foo() (после переопределения)
echo "После: " . $e->foo();
?>
```

Результат виконання наведеного прикладу:

```
До: foo!
После: bar!
```

### Дивіться також

-   [runkit7\_method\_add()](function.runkit7-method-add.md) \- Динамічно додає новий метод у заданий клас
-   [runkit7\_method\_copy()](function.runkit7-method-copy.md) \- Копіює метод з одного класу до іншого
-   [runkit7\_method\_remove()](function.runkit7-method-remove.md) \- динамічно видаляє заданий метод
-   [runkit7\_method\_rename()](function.runkit7-method-rename.md) \- динамічно змінює ім'я заданого методу
-   [runkit7\_function\_redefine()](function.runkit7-function-redefine.md) \- замінює визначення функції новою реалізацією
