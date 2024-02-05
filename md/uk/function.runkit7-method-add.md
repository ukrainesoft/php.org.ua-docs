---
navigation:
  - function.runkit7-import.md: « runkit7\_import
  - function.runkit7-method-copy.md: runkit7\_method\_copy »
  - index.md: PHP Manual
  - ref.runkit7.md: Функції runkit7
title: runkit7\_method\_add
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# runkit7\_method\_add

(PECL runkit7 >= Unknown)

runkit7\_method\_add — Динамічно додає новий метод у заданий клас

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

Метод може бути **`RUNKIT7_ACC_PUBLIC`** **`RUNKIT7_ACC_PROTECTED`**или**`RUNKIT7_ACC_PRIVATE`**, і, при необхідності, об'єднаний за допомогою побітового АБО з **`RUNKIT7_ACC_STATIC`**

`doc_comment`

Документальний коментар методу.

`return_type`

Тип значення методу, що повертається.

`is_strict`

Визначає, чи буде метод поводитися так, якби він був оголошений у файлі з `strict_types=1`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**runkit7\_method\_add()\*\*\*\*

```php
<?php
class Example {
    function foo() {
        echo "foo!\n";
    }
}

// создание объекта Example
$e = new Example();

// добавление нового общедоступного метода
runkit7_method_add(
    'Example',
    'add',
    '$num1, $num2',
    'return $num1 + $num2;',
    RUNKIT7_ACC_PUBLIC
);

// добавление 12 + 4
echo $e->add(12, 4);
?>
```

Результат виконання наведеного прикладу:

```
16
```

### Дивіться також

-   [runkit7\_method\_copy()](function.runkit7-method-copy.md) \- Копіює метод з одного класу до іншого
-   [runkit7\_method\_redefine()](function.runkit7-method-redefine.md) \- динамічно змінює код заданого методу
-   [runkit7\_method\_remove()](function.runkit7-method-remove.md) \- динамічно видаляє заданий метод
-   [runkit7\_method\_rename()](function.runkit7-method-rename.md) \- динамічно змінює ім'я заданого методу
-   [runkit7\_function\_add()](function.runkit7-function-add.md) \- Додає нову функцію, функція аналогічна create\_function
