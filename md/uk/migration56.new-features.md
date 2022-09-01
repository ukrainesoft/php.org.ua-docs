---
navigation:
  - migration56.incompatible.md: '« Зміни, що ламають зворотну сумісність'
  - migration56.deprecated.md: 'Функціонал, оголошений застарілим у PHP 5.6.x »'
  - index.md: PHP Manual
  - migration56.md: Миграция с PHP 5.5.x на PHP 5.6.x
title: Нові можливості
---
## Нові можливості

### Константні вирази

Тепер можна надати скалярний вираз, що включає числові та рядкові літерали та/або константи, коли раніше очікувалося статичне значення, наприклад, в оголошеннях констант або значення аргументів функцій за умовчанням.

```php
<?php
const ONE = 1;
const TWO = ONE * 2;

class C {
    const THREE = TWO + 1;
    const ONE_THIRD = ONE / self::THREE;
    const SENTENCE = 'Значение константы THREE - '.self::THREE;

    public function f($a = ONE + self::THREE) {
        return $a;
    }
}

echo (new C)->f()."\n";
echo C::SENTENCE;
?>
```

Результат виконання цього прикладу:

```
4
Значение константы THREE -  3
```

Також можна визначити масив (array) із використанням ключового слова `const`

```php
<?php
const ARR = ['a', 'b'];

echo ARR[0];
?>
```

Результат виконання цього прикладу:

```
a
```

### Функції зі змінною кількістю аргументів, використовуючи синтаксис `...`

[Функції зі змінною кількістю аргументів](functions.arguments.html#functions.variable-arg-list) тепер можна реалізовувати з використанням оператора `...` замість того, щоб покладатися на [funcgetargs()](function.func-get-args.md)

```php
<?php
function f($req, $opt = null, ...$params) {
    // $params - Масив, содержащий все остальные аргументы.
    printf('$req: %d; $opt: %d; количество параметров: %d'."\n",
           $req, $opt, count($params));
}

f(1);
f(1, 2);
f(1, 2, 3);
f(1, 2, 3, 4);
f(1, 2, 3, 4, 5);
?>
```

Результат виконання цього прикладу:

```
$req: 1; $opt: 0; количество параметров: 0
$req: 1; $opt: 2; количество параметров: 0
$req: 1; $opt: 2; количество параметров: 1
$req: 1; $opt: 2; количество параметров: 2
$req: 1; $opt: 2; количество параметров: 3
```

### Розпакування аргументів за допомогою `...`

[Масиви](language.types.array.md) та об'єкти, що реалізують інтерфейс [Traversable](class.traversable.md), можуть бути розпаковані в список аргументів під час передачі у функцію за допомогою оператора `...`

```php
<?php
function add($a, $b, $c) {
    return $a + $b + $c;
}

$operators = [2, 3];
echo add(1, ...$operators);
?>
```

Результат виконання цього прикладу:

```
6
```

### Зведення в ступінь за допомогою `**`

Доданий право-асоціативний оператор `**`, Що означає зведення у ступінь. Також доступний короткий синтаксис `**=`

```php
<?php
printf("2 ** 3 ==      %d\n", 2 ** 3);
printf("2 ** 3 ** 2 == %d\n", 2 ** 3 ** 2);

$a = 2;
$a **= 3;
printf("a ==           %d\n", $a);
?>
```

Результат виконання цього прикладу:

```
2 ** 3 ==      8
2 ** 3 ** 2 == 512
a ==           8
```

### `use function` і `use const`

Оператор [`use`](language.namespaces.importing.md) був розширений для підтримки імпорту функцій та констант на додаток до класів. Це досягається за допомогою конструкцій `use function` і `use const`відповідно.

```php
<?php
namespace Name\Space {
    const FOO = 42;
    function f() { echo __FUNCTION__."\n"; }
}

namespace {
    use const Name\Space\FOO;
    use function Name\Space\f;

    echo FOO."\n";
    f();
}
?>
```

Результат виконання цього прикладу:

```
42
Name\Space\f
```

### phpdbg

Тепер PHP містить інтерактивний дебаггер, що називається "phpdbg" і реалізований як модуль SAPI. Подробиці дивіться у [документации phpdbg](book.phpdbg.md)

### Кодування за замовчуванням

Доданий ini-параметр [defaultcharset](ini.core.html#ini.default-charset), в якому можна вказати кодування за промовчанням для використання у функціях [htmlentities()](function.htmlentities.md) [htmlentitydecode()](function.html-entity-decode.md) і [htmlspecialchars()](function.htmlspecialchars.md). Зверніть увагу, що якщо (зараз вважається застарілим) задані параметри кодування iconv та mbstring, вони матимуть перевагу перед defaultcharset для iconv та mbstring.

Значення цієї настройки за промовчанням дорівнює `UTF-8`

### Перевикористання [`php://input`](wrappers.php.html#wrappers.php.input)

[`php://input`](wrappers.php.html#wrappers.php.input) тепер можна перевідкривати та зчитувати стільки разів, скільки потрібно. Це також призвело до значного зменшення обсягу пам'яті, необхідної для роботи з POST.

### Завантаження великих файлів

Тепер можна завантажувати файли розміром понад 2ГБ.

### [GMP](book.gmp.md) підтримує навантаження операторів

Об'єкти [GMP](book.gmp.md) тепер підтримують перевантаження операторів та приведення до скалярних типів. Це дозволяє використовувати GMP у вашому коді більш виразно:

```php
<?php
$a = gmp_init(42);
$b = gmp_init(17);

if (version_compare(PHP_VERSION, '5.6', '<')) {
    echo gmp_intval(gmp_add($a, $b)), PHP_EOL;
    echo gmp_intval(gmp_add($a, 17)), PHP_EOL;
    echo gmp_intval(gmp_add(42, $b)), PHP_EOL;
} else {
    echo $a + $b, PHP_EOL;
    echo $a + 17, PHP_EOL;
    echo 42 + $b, PHP_EOL;
}
?>
```

Результат виконання цього прикладу:

```
59
59
59
```

### [hashequals()](function.hash-equals.md) для запобігання атакам за часом при порівнянні рядків

Була додана функція [hashequals()](function.hash-equals.html) для порівняння двох рядків за постійний час. Це має допомогти уникнути атак у часі; наприклад, під час тестування хешування паролів функцією [crypt()](function.crypt.md) (за умови, що ви не можете використовувати [passwordhash()](function.password-hash.html) і [passwordverify()](function.password-verify.md), які не піддаються атакам за часом).

```php
<?php
$expected  = crypt('12345', '$2a$07$usesomesillystringforsalt$');
$correct   = crypt('12345', '$2a$07$usesomesillystringforsalt$');
$incorrect = crypt('1234',  '$2a$07$usesomesillystringforsalt$');

var_dump(hash_equals($expected, $correct));
var_dump(hash_equals($expected, $incorrect));
?>
```

Результат виконання цього прикладу:

```
bool(true)
bool(false)
```

### `__debugInfo()`

Було додано магічний метод [debugInfo()](language.oop5.magic.html#language.oop5.magic.debuginfo) для того, щоб дозволити об'єкту змінювати значення властивостей, що виводяться при використанні [vardump()](function.var-dump.md)

```php
<?php
class C {
    private $prop;

    public function __construct($val) {
        $this->prop = $val;
    }

    public function __debugInfo() {
        return [
            'propSquared' => $this->prop ** 2,
        ];
    }
}

var_dump(new C(42));
?>
```

Результат виконання цього прикладу:

```
object(C)#1 (1) {
  ["propSquared"]=>
  int(1764)
}
```

### Алгоритм хешування gost-crypto

Доданий алгоритм хешування `gost-crypto`. Він реалізує функцію хешування GOST, що використовується в таблицях CryptoPro S-box, визначених у [» RFC 4357, секция 11.2](http://www.faqs.org/rfcs/rfc4357)

### Поліпшення SSL/TLS

Дуже багато було зроблено для покращення підтримки SSL/TLS у PHP 5.6. Включаючи [разрешение проверки пиров по умолчанию](migration56.incompatible.html#migration56.incompatible.peer-verification), підтримка звірки відбитків сертифікатів, зниження впливу атаки переєднання TLS і безлічі нових [опций контекста SSL](context.ssl.md) для більш точного контролю над параметрами протоколу та перевірок під час використання зашифрованих потоків.

Докладніше всі ці зміни описані в розділі цього посібника [Изменения OpenSSL в PHP 5.6.x](migration56.openssl.md)

### Підтримка асинхронності [pgsql](book.pgsql.md)

Модуль [pgsql](book.pgsql.md) тепер підтримує асинхронні з'єднання та запити, тим самим дозволяючи неблокуючу взаємодію з базами даних PostgreSQL. Асинхронні з'єднання можуть бути встановлені за допомогою константи **`PGSQL_CONNECT_ASYNC`**, та нові функції [пгconnectpoll()](function.pg-connect-poll.html) [пгsocket()](function.pg-socket.html) [пгconsumeinput()](function.pg-consume-input.html) і [пгflush()](function.pg-flush.md) можуть бути використані для обробки асинхронних з'єднань та запитів.
