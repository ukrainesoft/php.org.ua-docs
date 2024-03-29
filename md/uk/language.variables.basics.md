---
navigation:
  - language.variables.md: « Змінні
  - language.variables.predefined.md: Зумовлені змінні »
  - index.md: PHP Manual
  - language.variables.md: Змінні
title: Основи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Основи

Змінні PHP представлені знаком долара з наступним ім'ям змінної. Ім'я змінної чутливе до регістру.

Імена змінних відповідають тим самим правилам, як і інші назви в PHP. Правильне ім'я змінної повинно починатися з літери або символу підкреслення та складатися з букв, цифр та символів підкреслення у будь-якій кількості. Це можна відобразити регулярним виразом: `^[a-zA-Z_\x80-\xff][a-zA-Z0-9_\x80-\xff]*$`

> **Зауваження**: Під літерами тут маються на увазі символи a-z, A-Z і байти від 128 до 255 (`0x80-0xff`

> **Зауваження** `$this` - це спеціальна змінна, якій не можна нічого присвоювати. До PHP 7.1.0 було можливе опосередковане присвоєння (наприклад, з використанням [змінних змінних](language.variables.variable.md)

**Підказка**

Смотрите также[Посібник з іменування](userlandnaming.md)

Для отримання інформації про функції роботи зі змінними звертайтесь до розділу [функцій роботи зі змінними](ref.var.md)

```php
<?php
$var = 'Боб';
$Var = 'Джо';
echo "$var, $Var";      // выведет "Боб, Джо"

$4site = 'ещё нет';     // неверно; начинается с цифры
$_4site = 'ещё нет';    // верно; начинается с символа подчёркивания
$täyte = 'mansikka';    // верно; 'ä' это (Расширенный) ASCII 228.
?>
```

За умовчанням змінні завжди надаються за значенням. Тобто, коли ви надаєте вираз змінної, все значення оригінального виразу копіюється в цю змінну. Це означає, наприклад, що як однієї змінної присвоєно значення інший, зміна однієї з них впливає іншу. Додаткову інформацію про цей спосіб присвоєння дивіться у розділі [Вирази](language.expressions.md)

PHP також пропонує інший спосіб присвоєння значень змінним: [присвоєння за посиланням](language.references.md). . Це означає, що нова змінна просто посилається (інакше кажучи, стає псевдонімом або вказує) на оригінальну змінну. Зміни у новій змінній відбиваються на оригіналі, і навпаки.

Для присвоєння за посиланням просто додайте амперсанд (&) до початку імені присвоюваної (вихідної) змінної. Наприклад, наступний фрагмент коду двічі виводить '`Мене звуть Боб`':

```php
<?php
$foo = 'Боб';              // Присваивает $foo значение 'Боб'
$bar = &$foo;              // Ссылка на $foo через $bar.
$bar = "Меня зовут $bar";  // Изменение $bar...
echo $bar;
echo $foo;                 // меняет и $foo.
?>
```

За посиланням можуть бути присвоєні лише іменовані змінні.

```php
<?php
$foo = 25;
$bar = &$foo;      // Это верное присвоение.
$bar = &(24 * 7);  // Неверно; ссылка на неименованное выражение.

function test()
{
   return 25;
}

$bar = &test();    // Неверно.
?>
```

Хорошою практикою вважається ініціалізувати змінні, хоча у PHP це і не обов'язкова вимога. Неініціалізовані змінні набувають значення за умовчанням залежно від їх типу, що визначається з контексту їх першого використання: логічні змінні набувають значення **`false`**, цілі числа та числа з плаваючою точкою - нуль, рядки (наприклад, при виклику з конструкцією [echo](function.echo.md)) - Порожній рядок, а масиви стають порожніми масивами.

**Приклад #1 Значення за замовчуванням у неініціалізованих змінних**

```php
<?php
// Неустановленная И не имеющая ссылок (то есть без контекста использования) переменная; выведет NULL
var_dump($unset_var);

// Использование логической переменной; выведет 'false' (Подробнее по этому синтаксису смотрите раздел о тернарном операторе)
echo $unset_bool ? "true\n" : "false\n";

// Строковое использование; выведет 'string(3) "abc"'
$unset_str .= 'abc';
var_dump($unset_str);

// Целочисленное использование; выведет 'int(25)'
$unset_int += 25; // 0 + 25 => 25
var_dump($unset_int);

// Использование в качестве числа с плавающей точкой (float); выведет 'float(1.25)'
$unset_float += 1.25;
var_dump($unset_float);

// Использование в качестве массива; выведет array(1) {  [3]=>  string(3) "def" }
$unset_arr[3] = "def"; // array() + array(3 => "def") => array(3 => "def")
var_dump($unset_arr);

// Использование в качестве объекта; создаёт новый объект stdClass (смотрите http://www.php.net/manual/ru/reserved.classes.php)
// Выведет: object(stdClass)#1 (1) {  ["foo"]=>  string(3) "bar" }
$unset_obj->foo = 'bar';
var_dump($unset_obj);
?>
```

Покладатися на значення за замовчуванням неініціалізованих змінних досить проблематично при включенні файлу до іншого файлу, який використовує змінну з тим самим ім'ям. У разі роботи з неініціалізованою змінною викликається помилка рівня **`E_WARNING`** (до PHP 8.0.0 викидалася помилка рівня **`E_NOTICE`**), за винятком випадку додавання елементів у неініціалізований масив. Для виявлення ініціалізації змінної може бути використана мовна конструкція [isset()](function.isset.md)
