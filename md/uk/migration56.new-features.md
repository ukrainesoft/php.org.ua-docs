---
navigation:
  - migration56.incompatible.md: '« Зміни, що ламають зворотну сумісність'
  - migration56.deprecated.md: 'Функціонал, оголошений застарілим у PHP 5.6.x'
  - index.md: PHP Manual
  - migration56.md: Міграція з PHP 5.5.x на PHP 5.6.x
title: Нові можливості
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Нові можливості

### Константні вирази

Тепер можна надати скалярний вираз, що включає числові та рядкові літерали та/або константи, коли раніше очікувалося статичне значення, наприклад, в оголошеннях констант або значення аргументів функцій за умовчанням.

```php
<?php
const ONE = 1;
const TWO = ONE * 2;

class C {
    const THREE = TWO + 1;
    const ONE_THIRD = ONE / self::THREE;
    const SENTENCE = 'Значение константы THREE - '.self::THREE;

    public function f($a = ONE + self::THREE) {
        return $a;
    }
}

echo (new C)->f()."\n";
echo C::SENTENCE;
?>
```

Результат виконання наведеного прикладу:

```
4
Значение константы THREE -  3
```

Також можна визначити масив (array) із використанням ключового слова `const` :

```php
<?php
const ARR = ['a', 'b'];

echo ARR[0];
?>
```

Результат виконання наведеного прикладу:

```
a
```

### Функції зі змінною кількістю аргументів, використовуючи синтаксис `...`

[Функції зі змінною кількістю аргументів](functions.arguments.md#functions.variable-arg-list) тепер можна реалізовувати з використанням оператора `...` замість того, щоб покладатися на [func\_get\_args()](function.func-get-args.md)

```php
<?php
function f($req, $opt = null, ...$params) {
    // $params - массив, содержащий все остальные аргументы.
    printf('$req: %d; $opt: %d; количество параметров: %d'."\n",
           $req, $opt, count($params));
}

f(1);
f(1, 2);
f(1, 2, 3);
f(1, 2, 3, 4);
f(1, 2, 3, 4, 5);
?>
```

Результат виконання наведеного прикладу:

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
function add($a, $b, $c) {
    return $a + $b + $c;
}

$operators = [2, 3];
echo add(1, ...$operators);
?>
```

Результат виконання наведеного прикладу:

```
6
```

### Возведение в степень с помощью`**`

Доданий право-асоціативний оператор `**`, обозначающий возведение в степень. Также доступен короткий синтаксис`**=`

```php
<?php
printf("2 ** 3 ==      %d\n", 2 ** 3);
printf("2 ** 3 ** 2 == %d\n", 2 ** 3 ** 2);

$a = 2;
$a **= 3;
printf("a ==           %d\n", $a);
?>
```

Результат виконання наведеного прикладу:

```
2 ** 3 ==      8
2 ** 3 ** 2 == 512
a ==           8
```

### `use function`и`use const`

Оператор[`use`](language.namespaces.importing.md) був розширений для підтримки імпорту функцій та констант на додаток до класів. Це досягається за допомогою конструкцій `use function`и`use const`відповідно.

```php
<?php
namespace Name\Space {
    const FOO = 42;
    function f() { echo __FUNCTION__."\n"; }
}

namespace {
    use const Name\Space\FOO;
    use function Name\Space\f;

    echo FOO."\n";
    f();
}
?>
```

Результат виконання наведеного прикладу:

```
42
Name\Space\f
```

### phpdbg

Тепер PHP містить інтерактивний дебаггер, що називається "phpdbg" і реалізований як модуль SAPI. Подробиці дивіться у [документації phpdbg](book.phpdbg.md)

### Кодування за замовчуванням

Добавлен ini-параметр[default\_charset](ini.core.md#ini.default-charset), в якому можна вказати кодування за промовчанням для використання у функціях [htmlentities()](function.mdentities.md) [html\_entity\_decode()](function.md-entity-decode.md) і [htmlspecialchars()](function.mdspecialchars.md). Зверніть увагу, що якщо (зараз вважається застарілим) задані параметри кодування iconv та mbstring, вони матимуть перевагу перед default\_charset для iconv та mbstring.

Значення цієї настройки за промовчанням дорівнює `UTF-8`

### Переиспользование[`php://input`](wrappers.php.md#wrappers.php.input)

[`php://input`](wrappers.php.md#wrappers.php.input) тепер можна перевідкривати та зчитувати стільки разів, скільки потрібно. Це також призвело до значного зменшення обсягу пам'яті, необхідної для роботи з POST.

### Завантаження великих файлів

Тепер можна завантажувати файли розміром понад 2ГБ.

### [GMP](book.gmp.md) підтримує навантаження операторів

Об'єкти [GMP](book.gmp.md) тепер підтримують навантаження операторів та приведення до скалярних типів. Це дозволяє використовувати GMP у вашому коді більш виразно:

```php
<?php
$a = gmp_init(42);
$b = gmp_init(17);

if (version_compare(PHP_VERSION, '5.6', '<')) {
    echo gmp_intval(gmp_add($a, $b)), PHP_EOL;
    echo gmp_intval(gmp_add($a, 17)), PHP_EOL;
    echo gmp_intval(gmp_add(42, $b)), PHP_EOL;
} else {
    echo $a + $b, PHP_EOL;
    echo $a + 17, PHP_EOL;
    echo 42 + $b, PHP_EOL;
}
?>
```

Результат виконання наведеного прикладу:

```
59
59
59
```

### [hash\_equals()](function.hash-equals.md)для предотвращения атак по времени при сравнении строк

Була додана функція [hash\_equals()](function.hash-equals.md) для порівняння двох рядків за постійний час. Це має допомогти уникнути атак у часі; наприклад, під час тестування хешування паролів функцією [crypt()](function.crypt.md) (за умови, що ви не можете використовувати [password\_hash()](function.password-hash.md) і [password\_verify()](function.password-verify.md), які не піддаються атакам за часом).

```php
<?php
$expected  = crypt('12345', '$2a$07$usesomesillystringforsalt$');
$correct   = crypt('12345', '$2a$07$usesomesillystringforsalt$');
$incorrect = crypt('1234',  '$2a$07$usesomesillystringforsalt$');

var_dump(hash_equals($expected, $correct));
var_dump(hash_equals($expected, $incorrect));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(false)
```

### `__debugInfo()`

Було додано магічний метод [\_\_debugInfo()](language.oop5.magic.md#language.oop5.magic.debuginfo) для того, щоб дозволити об'єкту змінювати значення властивостей, що виводяться при використанні [var\_dump()](function.var-dump.md)

```php
<?php
class C {
    private $prop;

    public function __construct($val) {
        $this->prop = $val;
    }

    public function __debugInfo() {
        return [
            'propSquared' => $this->prop ** 2,
        ];
    }
}

var_dump(new C(42));
?>
```

Результат виконання наведеного прикладу:

```
object(C)#1 (1) {
  ["propSquared"]=>
  int(1764)
}
```

### Алгоритм хешування gost-crypto

Добавлен алгоритм хеширования`gost-crypto`. Він реалізує функцію хешування GOST, що використовується в таблицях CryptoPro S-box, визначених у [» RFC 4357, секція 11.2](http://www.faqs.org/rfcs/rfc4357)

### Поліпшення SSL/TLS

Дуже багато було зроблено для покращення підтримки SSL/TLS у PHP 5.6. Включно [дозвіл перевірки бенкетів за умовчанням](migration56.incompatible.md#migration56.incompatible.peer-verification), підтримка звірки відбитків сертифікатів, зниження впливу атаки переєднання TLS і безлічі нових [опцій контексту SSL](context.ssl.md) для більш точного контролю за параметрами протоколу та перевірок під час використання зашифрованих потоків.

Докладніше всі ці зміни описані в розділі цього посібника [Зміни OpenSSL у PHP 5.6.x](migration56.openssl.md)

### Поддержка асинхронности[pgsql](book.pgsql.md)

Модуль[pgsql](book.pgsql.md) тепер підтримує асинхронні з'єднання та запити, тим самим дозволяючи неблокуючу взаємодію з базами даних PostgreSQL. Асинхронні з'єднання можуть бути встановлені за допомогою константи **`PGSQL_CONNECT_ASYNC`**, та нові функції [pg\_connect\_poll()](function.pg-connect-poll.md) [pg\_socket()](function.pg-socket.md) [pg\_consume\_input()](function.pg-consume-input.md) і [pg\_flush()](function.pg-flush.md) можуть бути використані для обробки асинхронних з'єднань та запитів.
