---
navigation:
  - function.call-user-func.md: « call\_user\_func
  - function.forward-static-call-array.md: forward\_static\_call\_array »
  - index.md: PHP Manual
  - ref.funchand.md: Функції керування функціями
title: create\_function
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# create\_function

(PHP 4 >= 4.0.1, PHP 5, PHP 7)

create\_function — Створює функцію динамічно, оцінюючи рядок коду

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.2.0 і була *ВИДАЛЕНО* у версії PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
create_function(string $args, string $code): string
```

Створює функцію динамічно з переданих параметрів та повертає її унікальне ім'я.

**Застереження**

Функція всередині себе робить виклик функції [eval()](function.eval.md), а значить має такі ж проблеми з безпекою, як і [eval()](function.eval.md). Також у неї погані характеристики продуктивності та використання пам'яті, оскільки створені функції є глобальними і не можуть бути звільнені.

Используйте[анонімні функції](functions.anonymous.md)

### Список параметрів

Зазвичай рекомендується передавати параметри у вигляді рядків [з одинарною лапкою](language.types.string.md#language.types.string.syntax.single)При использовании строк[з подвійною лапкою](language.types.string.md#language.types.string.syntax.double) імена змінних у коді повинні бути ретельно екрановані, наприклад, ось так: `\$somevar`

`args`

Аргументи функції у вигляді рядка, розділеного комами.

`code`

Код функції.

### Значення, що повертаються

Повертає унікальне ім'я функції у вигляді рядка або **`false`** у разі виникнення помилки. Зверніть увагу, що ім'я містить недрукований символ (`"\0"`), тому слід бути обережним під час друку імені або включення його в будь-який інший рядок.

### Приклади

**Приклад #1 Створення функції динамічно за допомогою **create\_function()** або анонімних функцій**

Ви можете використовувати динамічно створену функцію, щоб створити функцію на основі інформації, зібраної під час виконання. По-перше, використовуючи функцію **create\_function()** :

```php
<?php
$newfunc = create_function('$a,$b', 'return "ln($a) + ln($b) = " . log($a * $b);');
echo $newfunc(2, M_E) . "\n";
?>
```

Тепер той же код, використовуючи [анонімну функцію](functions.anonymous.md); Зверніть увагу, що код та аргументи більше не містяться в рядках:

```php
<?php
$newfunc = function($a,$b) { return "ln($a) + ln($b) = " . log($a * $b); };
echo $newfunc(2, M_E) . "\n";
?>
```

Результат виконання наведеного прикладу:

```
ln(2) + ln(2.718281828459) = 1.6931471805599
```

**Приклад #2 Создание общей функции-обработчика с помощью**create\_function()\*\* або анонімних функцій\*\*

Іншим варіантом використання може бути загальна функція-обробник, яка може застосовувати набір операцій до списку параметрів:

```php
<?php
function process($var1, $var2, $farr)
{
    foreach ($farr as $f) {
        echo $f($var1, $var2) . "\n";
    }
}

// создаём кучу математических функций
$farr = array(
    create_function('$x,$y', 'return "тригонометрия: ".(sin($x) + $x*cos($y));'),
    create_function('$x,$y', 'return "гипотенуза: ".sqrt($x*$x + $y*$y);'),
    create_function('$a,$b', 'if ($a >=0) {return "b*a^2 = ".$b*sqrt($a);} else {return false;}'),
    create_function('$a,$b', "return \"min(b^2+a, a^2,b) = \".min(\$a*\$a+\$b,\$b*\$b+\$a);"),
    create_function('$a,$b', 'if ($a > 0 && $b != 0) {return "ln(a)/b = ".log($a)/$b; } else { return false; }')
);

echo "\nИспользование первого массива динамических функций\n";
echo "Параметры: 2.3445, M_PI\n";
process(2.3445, M_PI, $farr);

// теперь создаём кучу функций обработки строк
$garr = array(
    create_function('$b,$a', 'if (strncmp($a, $b, 3) == 0) return "** \"$a\" '.
        'и \"$b\"\n** для меня одинаковы! (смотря по первым 3 символам)";'),
    create_function('$a,$b', 'return "CRCs: " . crc32($a) . ", ".crc32($b);'),
    create_function('$a,$b', 'return "similar(a,b) = " . similar_text($a, $b, $p) . "($p%)";')
);
echo "\nИспользование второго массива динамических функций\n";
process("Варкалось. Хливкие шорьки пырялись по наве", "Варан ползёт", $garr);
?>
```

І знову, той же код з використанням [анонімних функцій](functions.anonymous.md). Зверніть увагу, що імена змінних у коді більше не потрібно екранувати, оскільки вони не укладені в рядок.

```php
<?php
function process($var1, $var2, $farr)
{
    foreach ($farr as $f) {
        echo $f($var1, $var2) . "\n";
    }
}

// создаём кучу математических функций
$farr = array(
    function($x,$y) { return "тригонометрия: ".(sin($x) + $x*cos($y)); },
    function($x,$y) { return "гипотенуза: ".sqrt($x*$x + $y*$y); },
    function($a,$b) { if ($a >=0) {return "b*a^2 = ".$b*sqrt($a);} else {return false;} },
    function($a,$b) { return "min(b^2+a, a^2,b) = " . min($a*$a+$b, $b*$b+$a); },
    function($a,$b) { if ($a > 0 && $b != 0) {return "ln(a)/b = ".log($a)/$b; } else { return false; } }
);

echo "\nИспользование первого массива динамических функций\n";
echo "Параметры: 2.3445, M_PI\n";
process(2.3445, M_PI, $farr);

// теперь создаём кучу функций обработки строк
$garr = array(
    function($b,$a) { if (strncmp($a, $b, 3) == 0) return "** \"$a\" " .
        "и \"$b\"\n** для меня одинаковы! (смотря по первым 3 символам)"; },
    function($a,$b) { return "CRCs: " . crc32($a) . ", ".crc32($b); },
    function($a,$b) { return "similar(a,b) = " . similar_text($a, $b, $p) . "($p%)"; }
);
echo "\nИспользование второго массива динамических функций\n";
process("Варкалось. Хливкие шорьки пырялись по наве", "Варан ползёт", $garr);
?>
```

Результат виконання наведеного прикладу:

```
Использование первого массива динамических функций
Параметры: 2.3445, M_PI
тригонометрия: -1.6291725057799
гипотенуза: 3.9199852871011
b*a^2 = 4.8103313314525
min(b^2+a, a^2,b) = 8.6382729035898
ln(a)/b = 0.27122299212594

Использование второго массива динамических функций
** "Варан ползёт" и "Варкалось. Хливкие шорьки пырялись по наве"
** для меня одинаковы! (смотря по первым 3 символам)
CRCs: 2672527412, 2269828269
similar(a,b) = 16(31.683168316832%)
```

**Приклад #3 Використання динамічних функцій як callback-функцій**

Можливо, найпоширенішим використанням динамічних функцій є передача їх як callback-функцій, наприклад, при використанні [array\_walk()](function.array-walk.md) або [usort()](function.usort.md)

```php
<?php
$av = array("the ", "a ", "that ", "this ");
array_walk($av, create_function('&$v,$k', '$v = $v . "mango";'));
print_r($av);
?>
```

Перетворення наведеного вище коду в [анонімну функцію](functions.anonymous.md) :

```php
<?php
$av = array("о, ", "эх, ", "то ", "это ");
array_walk($av, create_function('&$v,$k', '$v = $v . "манго";'));
print_r($av);
?>
```

Результат виконання наведеного прикладу:

```
Array
(
  [0] => о, манго
  [1] => эх, манго
  [2] => то манго
  [3] => это манго
)
```

Сортування рядків від найдовшого до найкоротшого за допомогою **create\_function()** :

```php
<?php
$sv = array("мало", "много", "большая строка", "строка строка строка");
echo "Оригинальный массив:\n";
print_r($sv);
echo "Отсортированный:\n";
usort($sv, create_function('$a,$b','return strlen($b) - strlen($a);'));
print_r($sv);
?>
```

Перетворення наведеного вище коду в [анонімну функцію](functions.anonymous.md) :

```php
<?php
$sv = array("мало", "много", "большая строка", "строка строка строка");
echo "Оригинальный массив:\n";
print_r($sv);
echo "Отсортированный:\n";
usort($sv, function($a,$b) { return strlen($b) - strlen($a); });
print_r($sv);
?>
```

Результат виконання наведеного прикладу:

```
Оригинальный массив:
Array
(
    [0] => мало
    [1] => много
    [2] => большая строка
    [3] => строка строка строка
)
Отсортированный:
Array
(
    [0] => строка строка строка
    [1] => большая строка
    [2] => много
    [3] => мало
)
```

### Дивіться також

-   [Анонімні функції](functions.anonymous.md)
