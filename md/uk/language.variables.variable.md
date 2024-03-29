---
navigation:
  - language.variables.scope.md: « Область видимості змінної
  - language.variables.external.md: Змінні ззовні PHP »
  - index.md: PHP Manual
  - language.variables.md: Змінні
title: Змінні змінних
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Змінні змінних

Іноді буває зручно мати змінними імена змінних. Тобто ім'я змінної, яке може бути визначено та змінено динамічно. Звичайна змінна визначається приблизно таким виразом:

```php
<?php
$a = 'hello';
?>
```

Змінна змінної бере значення змінної та розглядає його як ім'я змінної. У наведеному вище прикладі *hello* може бути використаний як ім'я змінної за допомогою двох знаків долара. Тобто:

```php
<?php
$$a = 'world';
?>
```

Тепер у дереві символів PHP визначено та містяться дві змінні: $a, що містить "hello" і $hello, що містить "world". Таким чином, вираз

```php
<?php
echo "$a {$$a}";
?>
```

виведе те саме, що і

```php
<?php
echo "$a $hello";
?>
```

тобто вони обидва виведуть: hello world.

Для того, щоб використовувати змінні змінних з масивами, ви повинні вирішити проблему двозначності. Тобто якщо ви напишете $$a\[ \], обробнику необхідно знати, чи ви хочете використовувати $a\[ \] як змінна, або вам потрібна як змінна $$a, а потім її індекс \[ \]. Синтаксис для вирішення цієї двозначності такий: ${$a\[ \]} для першого випадку і ${$a}\[ \]для второго.

До властивостей класу можна отримати доступ динамічно. Змінне ім'я властивості буде дозволено в контексті, в якому відбудеться виклик до нього. Наприклад, у разі вираження $foo->$bar, локальна область видимості буде просканована на наявність змінної $bar, значення якої буде використано як ім'я властивості об'єкта $foo. Це також працює і в тому випадку, якщо $bar здійснює доступ до масиву.

Фігурні дужки можуть використовуватися, щоб чітко розмежувати ім'я властивості. Вони найкорисніші при отриманні доступу до значень всередині властивості, що містить масив, коли ім'я властивості складається з кількох частин, або коли ім'я властивості містить символи, які інакше не дійсні (наприклад, функції [json\_decode()](function.json-decode.md)или из[SimpleXML](book.simplexml.md)

**Приклад #1 Приклад змінного імені властивості**

```php
<?php
class foo {
    var $bar = 'I am bar.';
    var $arr = array('I am A.', 'I am B.', 'I am C.');
    var $r   = 'I am r.';
}

$foo = new foo();
$bar = 'bar';
$baz = array('foo', 'bar', 'baz', 'quux');
echo $foo->$bar . "\n";
echo $foo->{$baz[1]} . "\n";

$start = 'b';
$end   = 'ar';
echo $foo->{$start . $end} . "\n";

$arr = 'arr';
echo $foo->{$arr[1]} . "\n";

?>
```

Результат виконання наведеного прикладу:

I am bar.  
I am bar.  
I am bar.  
I am r.

**Увага**

Зверніть увагу, що змінні змінних не можуть використовуватися з [суперглобальними масивами](language.variables.superglobals.md)PHP. Переменная`$this` також є особливою, на неї не можна посилатися динамічно.
