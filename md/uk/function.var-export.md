---
navigation:
  - function.var-dump.html: « vardump
  - refs.webservice.md: Веб-сервіси »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: varexport
---
# varexport

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

varexport — Виводить або повертає рядкове представлення змінної, що інтерпретується.

### Опис

```methodsynopsis
var_export(mixed $value, bool $return = false): ?string
```

**varexport()** повертає структуровану інформацію про цю змінну. Функція аналогічна [vardump()](function.var-dump.md) за одним винятком: подання, що повертається, є повноцінним PHP-кодом.

### Список параметрів

`value`

Змінна, яку потрібно експортувати.

`return`

Якщо передано і значення дорівнює **`true`** **varexport()** поверне уявлення змінної замість його виведення.

### Значення, що повертаються

Повертає подання змінної, якщо параметр `return` переданий і дорівнює **`true`**. Інакше функція повертає **`null`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Тепер об'єкти **stdClass** експортуються у вигляді масиву, приведеного до об'єкту (масив `(object) array( ... )`), замість використання неіснуючого методу **stdClass::setState()**. Практичний ефект полягає в тому, що тепер **stdClass** можна експортувати, і отриманий код буде працювати навіть у попередніх версіях PHP. |

### Приклади

**Приклад #1 Приклади використання **varexport()****

```php
<?php
$a = array (1, 2, array ("a", "b", "c"));
var_export($a);
?>
```

Результат виконання цього прикладу:

```
array (
  0 => 1,
  1 => 2,
  2 =>
  array (
    0 => 'a',
    1 => 'b',
    2 => 'c',
  ),
)
```

```php
<?php

$b = 3.1;
$v = var_export($b, true);
echo $v;

?>
```

Результат виконання цього прикладу:

```
3.1
```

**Приклад #2 Експорт stdClass з PHP 7.3.0**

```php
<?php
$person = new stdClass;
$person->name = 'ElePHPant ElePHPantsdotter';
$person->website = 'https://php.net/elephpant.php';

var_export($person);
```

Результат виконання цього прикладу:

```
(object) array(
   'name' => 'ElePHPant ElePHPantsdotter',
   'website' => 'https://php.net/elephpant.php',
)
```

**Приклад #3 Експорт класів**

```php
<?php
class A { public $var; }
$a = new A;
$a->var = 5;
var_export($a);
?>
```

Результат виконання цього прикладу:

```
A::__set_state(array(
   'var' => 5,
))
```

**Приклад #4 Використання [setstate()](language.oop5.magic.html#object.set-state)**

```php
<?php
class A
{
    public $var1;
    public $var2;

    public static function __set_state($an_array)
    {
        $obj = new A;
        $obj->var1 = $an_array['var1'];
        $obj->var2 = $an_array['var2'];
        return $obj;
    }
}

$a = new A;
$a->var1 = 5;
$a->var2 = 'foo';

eval('$b = ' . var_export($a, true) . ';'); // $b = A::__set_state(array(
                                            //    'var1' => 5,
                                            //    'var2' => 'foo',
                                            // ));
var_dump($b);
?>
```

Результат виконання цього прикладу:

```
object(A)#2 (2) {
  ["var1"]=>
  int(5)
  ["var2"]=>
  string(3) "foo"
}
```

### Примітки

> **Зауваження**
> 
> Змінні типи ресурсів не можуть бути експортовані за допомогою цієї функції.

> **Зауваження**
> 
> **varexport()** не обробляє циклічні посилання, оскільки майже неможливо було згенерувати інтерпретований PHP-код для такого випадку. Якщо необхідно виконувати якісь дії з повним представленням масиву чи об'єкта, використовуйте функцію [serialize()](function.serialize.md)

**Увага**

При експорті об'єктів функцією **varexport()**, провідний зворотний слєш не додається в ім'я класу із зазначеним простором імен для найкращої зворотної сумісності.

> **Зауваження**
> 
> Для того, щоб можна було використовувати згенерований **varexport()** PHP-код, необхідно, щоб усі порушені об'єкти реалізовували магічний метод [setstate](language.oop5.magic.html#object.set-state). Єдиний виняток **stdClass**, який експортується за допомогою масиву, приведеного до об'єкта.

### Дивіться також

-   [printr()](function.print-r.md) - Виводить зручну для читання інформацію про змінну
-   [serialize()](function.serialize.md) - Генерує придатне для зберігання подання змінної
-   [vardump()](function.var-dump.md) - Виводить інформацію про змінну
