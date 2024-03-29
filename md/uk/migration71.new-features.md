---
navigation:
  - migration71.md: « Міграція з PHP 7.0.x на PHP 7.1.x
  - migration71.new-functions.md: Нові функції »
  - index.md: PHP Manual
  - migration71.md: Міграція з PHP 7.0.x на PHP 7.1.x
title: Нові можливості
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Нові можливості

### Типи, що обнулюються

Типи для параметрів і значень, що повертаються можуть бути позначені як обнулювані шляхом додавання префікса у вигляді знака питання. Це означає, що зазначені параметри і значення, що повертаються, можуть бути як зазначеного типу, так і **`null`**

```php
<?php

function testReturn(): ?string
{
    return 'elePHPant';
}

var_dump(testReturn());

function testReturn(): ?string
{
    return null;
}

var_dump(testReturn());

function test(?string $name)
{
    var_dump($name);
}

test('elePHPant');
test(null);
test();
```

Результат виконання наведеного прикладу:

```
string(10) "elePHPant"
NULL
string(10) "elePHPant"
NULL
Uncaught Error: Too few arguments to function test(), 0 passed in...
```

### Функції, що нічого не повертають

Був доданий тип значення, що повертається void. Функції з таким заданим типом значення, що повертається, не повинні нічого повертати. Тобто або взагалі не містити жодного оператора return, або використовувати його без параметра . **`null`** не є коректним значенням для повернення таких функцій.

```php
<?php
function swap(&$left, &$right): void
{
    if ($left === $right) {
        return;
    }

    $tmp = $left;
    $left = $right;
    $right = $tmp;
}

$a = 1;
$b = 2;
var_dump(swap($a, $b), $a, $b);
```

Результат виконання наведеного прикладу:

```
null
int(2)
int(1)
```

Спроба використовувати значення таких функцій, що повертається, призведе до того, що це значення буде вважатися за \*\*`null`\*\*без виведення попередження. Причина цього в тому, що попередження викликатимуть спільні функції вищого порядку.

### Симетрична деструктуризація масиву

Можна використовувати короткий синтаксис (`[]`) для деструктуризації масивів з метою присвоєння (у тому числі в `foreach`), як альтернатива функції [list()](function.list.md)яка, втім, все ще підтримується.

```php
<?php
$data = [
    [1, 'Tom'],
    [2, 'Fred'],
];

// используя list()
list($id1, $name1) = $data[0];

// используя []
[$id1, $name1] = $data[0];

// используя list()
foreach ($data as list($id, $name)) {
    // код, содержащий $id и $name
}

// используя []
foreach ($data as [$id, $name]) {
    // код, содержащий $id и $name
}
```

### Видимість констант класу

Додано підтримку визначення області видимості для констант класу.

```php
<?php
class ConstDemo
{
    const PUBLIC_CONST_A = 1;
    public const PUBLIC_CONST_B = 2;
    protected const PROTECTED_CONST = 3;
    private const PRIVATE_CONST = 4;
}
```

### Псевдотип[iterable](language.types.iterable.md)

Було додано новий псевдотип (схожий на [callable](language.types.callable.md)), названий [iterable](language.types.iterable.md). Він може використовуватися як параметр, так і як значення, що повертається там, де використовується масив або об'єкт, що реалізує інтерфейс [Traversable](class.traversable.md). Що стосується підтипів, типи параметрів із дочірніх класів можуть розширити декларацію батьків типу array або [Traversable](class.traversable.md)до[iterable](language.types.iterable.md). Для типів повернення, дочірні класи можуть звужувати тип значення, що повертається з [iterable](language.types.iterable.md) до array або об'єкта реалізуючого [Traversable](class.traversable.md)

```php
<?php
function iterator(iterable $iter)
{
    foreach ($iter as $val) {
        //
    }
}
```

### Обробка кількох винятків в одному блоці catch

У блоці catch тепер можна обробляти кілька винятків, перераховуючи їх через символ вертикальної межі ( ). Це може бути корисним, якщо різні винятки обробляються однаково.

```php
<?php
try {
    // Какой то код
} catch (FirstException | SecondException $e) {
    // Обрабатываем оба исключения
}
```

### Підтримка ключів у [list()](function.list.md)

Тепер можна вказувати ключі в операторі [list()](function.list.md) або в його новому короткому синтаксисі `[]`. Це дозволяє деструктурувати масиви з нечисловими чи непослідовними ключами.

```php
<?php
$data = [
    ["id" => 1, "name" => 'Tom'],
    ["id" => 2, "name" => 'Fred'],
];

// стиль list()
list("id" => $id1, "name" => $name1) = $data[0];

// стиль []
["id" => $id1, "name" => $name1] = $data[0];

// стиль list()
foreach ($data as list("id" => $id, "name" => $name)) {
    // logic here with $id and $name
}

// стиль []
foreach ($data as ["id" => $id, "name" => $name]) {
    // logic here with $id and $name
}
```

### Підтримка негативних зсувів для рядків

Підтримка негативних зсувів для рядків додана в [функції для роботи з рядками](book.strings.md), а також у [індексацію рядків](language.types.string.md#language.types.string.substr) за допомогою `[]`или`{}`. У цих випадках негативні усунення інтерпретуються як усунення щодо кінця рядка.

```php
<?php
var_dump("abcdef"[-2]);
var_dump(strpos("aabbcc", "b", -3));
```

Результат виконання наведеного прикладу:

```
string (1) "e"
int(3)
```

Тепер підтримуються негативні зміщення у простому синтаксисі вказівки індексу у рядках та масивах.

```php
<?php
$string = 'bar';
echo "Последний символ '$string' - '$string[-1]'.\n";
?>
```

Результат виконання наведеного прикладу:

```
Последний символ 'bar' - 'r'.
```

### Підтримка AEAD в ext/openssl

Підтримка AEAD (режими GCM та CCM) була додана шляхом розширення функцій [openssl\_encrypt()](function.openssl-encrypt.md) і [openssl\_decrypt()](function.openssl-decrypt.md) додатковими параметрами.

### Преобразование callable в[Closure](class.closure.md) за допомогою [Closure::fromCallable()](closure.fromcallable.md)

В класс[Closure](class.closure.md) додано новий статичний метод для можливості легко перетворити [callable](language.types.callable.md) в об'єкти типу [Closure](class.closure.md)

```php
<?php
class Test
{
    public function exposeFunction()
    {
        return Closure::fromCallable([$this, 'privateFunction']);
    }

    private function privateFunction($param)
    {
        var_dump($param);
    }
}

$privFunc = (new Test)->exposeFunction();
$privFunc('значение');
```

Результат виконання наведеного прикладу:

```
string(16) "значение"
```

### Асинхронне оброблення сигналів

Нова функція [pcntl\_async\_signals()](function.pcntl-async-signals.md) була додана для дозволу асинхронної обробки сигналів без використання тиків (які виробляють багато накладних витрат).

```php
<?php
pcntl_async_signals(true); // включает асинхронные сигналы

pcntl_signal(SIGHUP,  function($sig) {
    echo "SIGHUP\n";
});

posix_kill(posix_getpid(), SIGHUP);
```

Результат виконання наведеного прикладу:

```
SIGHUP
```

### Підтримка HTTP/2 server push в ext/curl

Підтримка "server push" додана в модуль CURL (потрібна версія 7.46 та вище). Використовувати можна у функції [curl\_multi\_setopt()](function.curl-multi-setopt.md) з новою константою **`CURLMOPT_PUSHFUNCTION`**. Також додані константи **`CURL_PUSH_OK`** і **`CURL_PUSH_DENY`** для визначення, було прийнято чи відхилено "server push".

### Контекстні опції потоку

Додано опцію контексту потоку [tcp\_nodelay](context.socket.md#context.socket.tcp_nodelay)
