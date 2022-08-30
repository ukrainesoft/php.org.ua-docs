Зміни, що ламають зворотну сумісність

-   [« Нові глобальні константи](migration72.constants.md)
    
-   [Функціонал, оголошений застарілим у PHP 7.2.x »](migration72.deprecated.md)
    
-   [PHP Manual](index.md)
    
-   [Миграция с PHP 7.1.x на PHP 7.2.x](migration72.md)
    
-   Зміни, що ламають зворотну сумісність
    

## Зміни, що ламають зворотну сумісність

### Запобігання поверненню негативного нуля з [numberformat()](function.number-format.html)

Раніше функція [numberformat()](function.number-format.html) повертала `-0`. Хоча це абсолютно правильно відповідно до специфікації чисел з плаваючою точкою IEEE 754, ця дивина небажана для відображення відформатованих чисел у формі, що легко читається.

```php
<?php

var_dump(number_format(-0.01)); // теперь выводит string(1) "0" вместо string(2) "-0"
```

### Перетворення числових ключів при приведенні об'єктів та масивів

Тепер числові ключі краще обробляються при приведенні масивів до об'єктів та об'єктів до масивів (через явне приведення, або використовуючи [settype()](function.settype.md)

Це означає, що числові (або числа у вигляді рядків) ключі з масивів, конвертовані в об'єкти, тепер будуть доступні:

```php
<?php

// приведение Масива к объекту
$arr = [0 => 1];
$obj = (object)$arr;
var_dump(
    $obj,
    $obj->{'0'}, // теперь работает
    $obj->{0} // теперь работает
);
```

Результат виконання цього прикладу:

```
object(stdClass)#1 (1) {
  ["0"]=>    // теперь это строковый ключ, а не числовой
  int(1)
}
int(1)
int(1)
```

І тепер числові (або числа у вигляді рядків) ключі об'єктів доступні при конвертації в масиви:

```php
<?php

// приведение объекта в Масив
$obj = new class {
    public function __construct()
    {
        $this->{0} = 1;
    }
};
$arr = (array)$obj;
var_dump(
    $arr,
    $arr[0], // теперь работает
    $arr['0'] // теперь работает
);
```

Результат виконання цього прикладу:

```
array(1) {
  [0]=>    // теперь это числовой ключ, а не строковый
  int(1)
}
int(1)
int(1)
```

### Заборонено передачу **`null`** в [getclass()](function.get-class.html)

Раніше передача **`null`** у функцію [getclass()](function.get-class.html) повертала ім'я класу, з якого було зроблено виклик. Ця поведінка була видалена і тепер натомість буде викликана помилка рівня **`E_WARNING`**. Для досягнення тієї самої поведінки, як і раніше, слід просто опустити аргумент.

### Попередження при підрахунку нечисленних типів

Тепер при використанні [count()](function.count.md) з параметром, який не можна вважати буде виникати помилка рівня **`E_WARNING`** (це також стосується [sizeof()](function.sizeof.md) як псевдоніма цієї функції).

```php
<?php

var_dump(
    count(null), // NULL нельзя подсчитать
    count(1), // числа нельзя подсчитать
    count('abc'), // строки нельзя подсчитать
    count(new stdclass), // объекты, не реализующие интерфейс Countable, нельзя подсчитать
    count([1,2]) // Масиви можно подсчитать
);
```

Результат виконання цього прикладу:

```
Warning: count(): Parameter must be an array or an object that implements Countable in %s on line %d

Warning: count(): Parameter must be an array or an object that implements Countable in %s on line %d

Warning: count(): Parameter must be an array or an object that implements Countable in %s on line %d

Warning: count(): Parameter must be an array or an object that implements Countable in %s on line %d
int(0)
int(1)
int(1)
int(1)
int(2)
```

### Перехід від ресурсів до об'єктів у модулі Hash

В рамках довгострокової міграції відмови від ресурсів, модуль [Hash](book.hash.md) було оновлено для використання об'єктів замість ресурсів. Ця зміна повинна бути плавною для PHP-розробників, за винятком випадків, коли використовуються перевірки [ісresource()](function.is-resource.html) (які потрібно замінити на використання [ісobject()](function.is-object.html)

### Покращено значення за замовчуванням у SSL/TLS

Були зроблені такі зміни до значень за замовчуванням:

-   `tls://` тепер за умовчанням використовується TLSv1.0 чи TLSv1.1 чи TLSv1.2
-   `ssl://` псевдонім `tls://`
-   Константи `STREAM_CRYPTO_METHOD_TLS_*` за умовчанням рівні TLSv1.0 або TLSv1.1 + TLSv1.2 замість TLSv1.0

### Значення, що повертається [gettype()](function.gettype.md) для закритих ресурсів

Раніше використання [gettype()](function.gettype.md) на закритому ресурсі повертало рядок `"unknown type"`. Тепер буде повернуто рядок `"resource (closed)"`

### [ісobject()](function.is-object.html) і **PHPIncompleteClass**

Раніше використання [ісobject()](function.is-object.html) на класі **PHPIncompleteClass** повертало **`false`**. Тепер повертатиметься **`true`**

### Підвищено рівні помилок невизначених констант

Не повністю визначені посилання на невизначені константи тепер генеруватимуть **`E_WARNING`** (замість **`E_NOTICE`**). У наступній основній версії PHP вони генеруватимуть винятки [Error](class.error.md)

### Підтримка Windows

Офіційно підтримувані мінімальні версії Windows тепер є Windows 7/Server 2008 R2.

### Перевірка значень властивостей за промовчанням трейту

Перевірка сумісності значень властивостей за промовчанням трейту більше не виконує приведення типу.

### `object` для імен класів

Ім'я `object` раніше було м'яко зарезервовано з PHP 7.0. Тепер воно повноцінне зарезервоване слово, що забороняє використовувати його як ім'я класу, трейту або інтерфейсу.

### Підтримка NetWare

Підтримка NetWare було видалено.

### [arrayunique()](function.array-unique.html) with **`SORT_STRING`**

Якщо `sort_flags` дорівнює **`SORT_STRING`**, раніше масив `array` копіювався, а не унікальні елементи видалялися (зберігаючи значення цифрових індексів), але тепер створюється новий масив шляхом додавання унікальних елементів. Це може призвести до різних числових індексів.

### Зміни [bcmod()](function.bcmod.md) з числами з плаваючою точкою

Функція [bcmod()](function.bcmod.md) більше не обрізає числа з плаваючою точкою до цілих. Таким чином, її поведінка тепер відповідає [fmod()](function.fmod.md), а не оператору `%`. Наприклад, `bcmod('4', '3.5')` тепер повертає `0.5` замість `1`

### Функції хешування та некриптографічні хеші

Функції [hashhmac()](function.hash-hmac.html) [hashhmacfile()](function.hash-hmac-file.html) [hashpbkdf2()](function.hash-pbkdf2.html) і [hashinit()](function.hash-init.html) (з **`HASH_HMAC`**) більше не приймають некриптографічні хеші.

### Опції функції [jsondecode()](function.json-decode.html)

Опція функції [jsondecode()](function.json-decode.html) **`JSON_OBJECT_AS_ARRAY`**, тепер використовується, якщо другий параметр (assoc) дорівнює **`null`**. Раніше **`JSON_OBJECT_AS_ARRAY`** завжди ігнорувався.

### Висновок [rand()](function.rand.md) і [мтrand()](function.mt-rand.html)

Числа, що генеруються [rand()](function.rand.md) і [мтrand()](function.mt-rand.html) для певного параметра переініціалізації (seed) можуть відрізнятися від PHP 7.1 на 64-бітних машинах (через виправлення помилки модульного зміщення в реалізації).

### Видалення ini-налаштувань [`sql.safe_mode`](ini.core.html#ini.sql.safe-mode)

Налаштування конфігурації `sql.safe_mode` було видалено.

### Зміни в [dateparse()](function.date-parse.html) і [dateparsefromformat()](function.date-parse-from-format.html)

Елемент масиву `zone`, що повертається функціями [dateparsefromformat()](function.date-parse-from-format.html) і [dateparse()](function.date-parse.html) тепер відображає секунди замість хвилин, а його знак інвертується. Наприклад, `-120` тепер буде `7200`

### Вхідні Cookies

Починаючи з PHP 7.2.34 *імена* вхідні cookie більше не декодуються з URL-закодованого рядка з міркувань безпеки.