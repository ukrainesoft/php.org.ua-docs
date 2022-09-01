---
navigation:
  - function.runkit7-import.html: « runkit7import
  - function.runkit7-method-copy.html: runkit7methodcopy »
  - index.md: PHP Manual
  - ref.runkit7.md: Функції runkit7
title: runkit7методadd
---
# runkit7методadd

(PECL runkit7> = Unknown)

runkit7методadd — Динамічно додає новий метод у заданий клас

### Опис

```methodsynopsis
runkit7_method_add(    string $class_name,    string $method_name,    string $argument_list,    string $code,    int $flags = RUNKIT7_ACC_PUBLIC,    string $doc_comment = null,    string $return_type = ?,    bool $is_strict = ?): bool
```

```methodsynopsis
runkit7_method_add(    string $class_name,    string $method_name,    Closure $closure,    int $flags = RUNKIT7_ACC_PUBLIC,    string $doc_comment = null,    string $return_type = ?,    bool $is_strict = ?): bool
```

### Список параметрів

`class_name`

Клас, у якому потрібно додати метод.

`method_name`

Ім'я методу, який потрібно додати.

`argument_list`

Розділений комами список аргументів для нового методу.

`code`

Код, який буде виконуватись під час виклику `method_name`

`closure`

Замикання ([closure](class.closure.md)), Що визначає метод.

`flags`

Метод може бути **`RUNKIT7_ACC_PUBLIC`** **`RUNKIT7_ACC_PROTECTED`** або **`RUNKIT7_ACC_PRIVATE`**, і, при необхідності, об'єднаний за допомогою побітового АБО з **`RUNKIT7_ACC_STATIC`**

`doc_comment`

Документальний коментар методу.

`return_type`

Тип значення методу, що повертається.

`is_strict`

Визначає, чи буде метод поводитися так, якби він був оголошений у файлі з `strict_types=1`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **runkit7методadd()****

```php
<?php
class Example {
    function foo() {
        echo "foo!\n";
    }
}

// создание объекта Example
$e = new Example();

// добавление нового общедоступного метода
runkit7_method_add(
    'Example',
    'add',
    '$num1, $num2',
    'return $num1 + $num2;',
    RUNKIT7_ACC_PUBLIC
);

// добавление 12 + 4
echo $e->add(12, 4);
?>
```

Результат виконання цього прикладу:

```
16
```

### Дивіться також

-   [runkit7methodcopy()](function.runkit7-method-copy.md) - Копіює метод з одного класу до іншого
-   [runkit7methodredefine()](function.runkit7-method-redefine.md) - динамічно змінює код заданого методу
-   [runkit7methodremove()](function.runkit7-method-remove.md) - динамічно видаляє заданий метод
-   [runkit7methodrename()](function.runkit7-method-rename.md) - динамічно змінює ім'я заданого методу
-   [runkit7functionadd()](function.runkit7-function-add.md) - Додає нову функцію, функція аналогічна createfunction
