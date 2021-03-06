- [«func_get_arg](function.func-get-arg.md)
- [func_num_args »](function.func-num-args.md)

- [PHP Manual](index.md)
- [Функції керування функціями](ref.funchand.md)
- Повертає масив, що містить аргументи функції

# func_get_args

(PHP 4, PHP 5, PHP 7, PHP 8)

func_get_args - Повертає масив, що містить аргументи функції

### Опис

**func_get_args**(): array

Отримує масив, який містить аргументи функції.

Ця функція може бути використана спільно з
[func_num_args()](function.func-num-args.md) та
[func_get_arg()](function.func-get-arg.md) для створення функцій з
змінною кількістю аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив, у якому кожен елемент є копією
відповідного члена списку аргументів функції користувача.

### Помилки

Генерує попередження під час виклику поза визначенням функції.

### Приклади

**Приклад #1 Приклад використання **func_get_args()****

` <?phpfunction foo(){    $numargs = func_num_args(); echo "Кількість аргументів: $numargs
";    if ($numargs >= 2) {        echo "Другий аргумент: " . func_get_arg(1) . "
";    }    $arg_list = func_get_args();    for ($i = 0; $i < $numargs; $i++) {        echo "Аргумент №$i: " . $arg_list[$i] . "
";    }}foo(1, 2, 3);?> `

Результат виконання цього прикладу:

Кількість аргументів: 3
Другий аргумент: 2
Аргумент №0: 1
Аргумент №1: 2
Аргумент №2: 3

**Приклад #2 Приклад передачі аргументів за посиланням та за значенням з
**func_get_args()****

` <?phpfunction byVal($arg) {    echo 'Передано           ::'', var_export(func_get_args()), PHP_EOL; $arg=='baz'; echo 'Після зміни  : ', var_export(func_get_args()), PHP_EOL;}function byRef(&$arg) {   echo 'Передано  _| $arg=='baz'; echo 'Після зміни  : ', var_export(func_get_args()), PHP_EOL;}$arg = 'bar';byVal($arg);byRef($arg);?> `

Результат виконання цього прикладу:


Передано : array (
0 =\> 'bar',
)
Після зміни : array (
0 =\> 'baz',
)
Передано : array (
0 =\> 'bar',
)
Після зміни : array (
0 =\> 'baz',
)

### Примітки

> **Примітка**:
>
> Починаючи з PHP 8.0.0, сімейство функцій func\_\*() призначене для
> більшої прозорості щодо іменованих аргументів, обробляючи
> аргументи так, якби всі вони були передані позиційно, а
> відсутні аргументи замінюються їх значеннями за замовчуванням. Функція
> ігнорує набір невідомих іменованих варіативних аргументів. До
> зібраним невідомим іменованим аргументам можна отримати доступ
> лише через варіативний параметр.

> **Примітка**:
>
> Якщо аргументи були передані за посиланням, всі зміни аргументів
> будуть відображені на значеннях, що повертаються функцією. У PHP 7 також будуть
> Повернені поточні значення, якщо аргументи передані за значенням

> **Примітка**: Ця функція повертає лише копії переданих
> аргументів і не повертає значення за замовчуванням (непереданих)
> аргументів.

### Дивіться також

- [Синтаксис `...`](functions.arguments.md#functions.variable-arg-list)
- [func_get_arg()](function.func-get-arg.md)
- [func_num_args()](function.func-num-args.md)
- [ReflectionFunctionAbstract::getParameters()](reflectionfunctionabstract.getparameters.md)
