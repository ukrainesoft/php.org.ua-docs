---
navigation:
  - function.func-get-arg.md: « funcgetarg
  - function.func-num-args.md: funcnumargs »
  - index.md: PHP Manual
  - ref.funchand.md: Функции управления функциями
title: funcgetargs
---
# funcgetargs

(PHP 4, PHP 5, PHP 7, PHP 8)

funcgetargs - Повертає масив, що містить аргументи функції

### Опис

```methodsynopsis
func_get_args(): array
```

Отримує масив, що містить аргументи функції.

Ця функція може бути використана спільно з [funcnumargs()](function.func-num-args.md) і [funcgetarg()](function.func-get-arg.md) для створення функцій із змінною кількістю аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив, в якому кожен елемент є копією відповідного члена списку аргументів функції користувача.

### Помилки

Генерує попередження під час виклику поза визначенням функції.

### Приклади

**Приклад #1 Приклад використання **funcgetargs()****

```php
<?php
function foo()
{
    $numargs = func_num_args();
    echo "Количество аргументов: $numargs\n";
    if ($numargs >= 2) {
        echo "Второй аргумент: " . func_get_arg(1) . "\n";
    }
    $arg_list = func_get_args();
    for ($i = 0; $i < $numargs; $i++) {
        echo "Аргумент №$i: " . $arg_list[$i] . "\n";
    }
}

foo(1, 2, 3);
?>
```

Результат виконання цього прикладу:

```
Количество аргументов: 3
Второй аргумент: 2
Аргумент №0: 1
Аргумент №1: 2
Аргумент №2: 3
```

**Приклад #2 Приклад передачі аргументів за посиланням та за значенням з **funcgetargs()****

```php
<?php
function byVal($arg) {
    echo 'Передан          : ', var_export(func_get_args()), PHP_EOL;
    $arg = 'baz';
    echo 'После изменения  : ', var_export(func_get_args()), PHP_EOL;
}

function byRef(&$arg) {
    echo 'Передан          : ', var_export(func_get_args()), PHP_EOL;
    $arg = 'baz';
    echo 'После изменения  : ', var_export(func_get_args()), PHP_EOL;
}

$arg = 'bar';
byVal($arg);
byRef($arg);
?>
```

Результат виконання цього прикладу:

Передано : array (  
0 => 'bar',

Після зміни: array (  
0 => ьбазь,

Передано : array (  
0 => 'bar',

Після зміни: array (  
0 => ьбазь,

### Примітки

> **Зауваження**
> 
> Починаючи з PHP 8.0.0, сімейство функцій func() призначено для більшої прозорості щодо іменованих аргументів, обробляючи аргументи так, ніби всі вони були передані позиційно, а відсутні аргументи замінюються їх значеннями за умовчанням. Функція ігнорує набір невідомих варіативних аргументів. До зібраних невідомих іменованих аргументів можна отримати доступ лише через варіативний параметр.

> **Зауваження**
> 
> Якщо аргументи були передані за посиланням, то всі зміни аргументів будуть відображені на значеннях, що повертаються функцією. У PHP 7 також буде повернуто поточні значення, якщо аргументи передані за значенням

> **Зауваження**: Ця функція повертає копії переданих аргументів і не повертає значення за промовчанням (непереданих) аргументів.

### Дивіться також

-   [Синтаксис](functions.arguments.md#functions.variable-arg-list)
-   [funcgetarg()](function.func-get-arg.md)
-   [funcnumargs()](function.func-num-args.md)
-   [ReflectionFunctionAbstract::getParameters()](reflectionfunctionabstract.getparameters.md)
