---
navigation:
  - language.oop5.iterations.md: « Ітератори об'єктів
  - language.oop5.final.md: Ключове слово final »
  - index.md: PHP Manual
  - language.oop5.md: Класи та об'єкти
title: Магические методы
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Магические методы

Магічні методи – це спеціальні методи, які перевизначають дію PHP за умовчанням, коли над об'єктом виконуються певні дії.

**Застереження**

Все имена методов, начинающиеся с`__`зарезервовані PHP. Не рекомендується використовувати імена методів з \_\_ у PHP, якщо ви не бажаєте використовувати відповідну магічну функціональність.

Наступні назви методів вважаються магічними: [\_\_construct()](language.oop5.decon.md#object.construct) [\_\_destruct()](language.oop5.decon.md#object.destruct) [\_\_call()](language.oop5.overloading.md#object.call) [\_\_callStatic()](language.oop5.overloading.md#object.callstatic) [\_\_get()](language.oop5.overloading.md#object.get) [\_\_set()](language.oop5.overloading.md#object.set) [\_\_isset()](language.oop5.overloading.md#object.isset) [\_\_unset()](language.oop5.overloading.md#object.unset) [\_\_sleep()](language.oop5.magic.md#object.sleep) [\_\_wakeup()](language.oop5.magic.md#object.wakeup) [\_\_serialize()](language.oop5.magic.md#object.serialize) [\_\_unserialize()](language.oop5.magic.md#object.unserialize) [\_\_toString()](language.oop5.magic.md#object.tostring) [\_\_invoke()](language.oop5.magic.md#object.invoke) [\_\_set\_state()](language.oop5.magic.md#object.set-state) [\_\_clone()](language.oop5.cloning.md#object.clone) і [\_\_debugInfo()](language.oop5.magic.md#object.debuginfo)

**Увага**

Усі магічні методи, за винятком [\_\_construct()](language.oop5.decon.md#object.construct) [\_\_destruct()](language.oop5.decon.md#object.destruct) і [\_\_clone()](language.oop5.cloning.md#object.clone) *ПОВИННІ* бути оголошені як `public`, інакше буде викликана помилка рівня **`E_WARNING`**. До PHP 8.0.0 для магічних методів [\_\_sleep()](language.oop5.magic.md#object.sleep) [\_\_wakeup()](language.oop5.magic.md#object.wakeup) [\_\_serialize()](language.oop5.magic.md#object.serialize) [\_\_unserialize()](language.oop5.magic.md#object.unserialize) і [\_\_set\_state()](language.oop5.magic.md#object.set-state) не виконувалась перевірка.

**Увага**

Якщо оголошення типу використовуються для визначення магічного методу, вони повинні бути ідентичними сигнатурі, описаної в цьому документі. В іншому випадку видається фатальна помилка. До PHP 8.0.0 діагностичні повідомлення не надсилалися. Однак [\_\_construct()](language.oop5.decon.md#object.construct) і [\_\_destruct()](language.oop5.decon.md#object.destruct) не повинні оголошувати тип, що повертається; в іншому випадку видається фатальна помилка.

### [\_\_sleep()](language.oop5.magic.md#object.sleep) і [\_\_wakeup()](language.oop5.magic.md#object.wakeup)

```methodsynopsis
public __sleep(): array
```

```methodsynopsis
public __wakeup(): void
```

Функция[serialize()](function.serialize.md) перевіряє, чи є у класі метод із магічним ім'ям [\_\_sleep()](language.oop5.magic.md#object.sleep). Якщо це так, цей метод виконується до будь-якої операції серіалізації. Він може очистити об'єкт і повинен повертати масив з іменами всіх змінних цього об'єкта, які мають бути серіалізовані. Якщо метод нічого не повертає, то серіалізується **`null`** та видається попередження **`E_NOTICE`**

> **Зауваження** :
> 
> Неприпустимо повертати в [\_\_sleep()](language.oop5.magic.md#object.sleep) імена закритих властивостей у батьківському класі. Це призведе до помилки рівня **`E_NOTICE`**. Натомість ви можете використовувати [\_\_serialize()](language.oop5.magic.md#object.serialize)

> **Зауваження** :
> 
> Починаючи з PHP 8.0.0, повернення значення, що не є масивом, з [\_\_sleep()](language.oop5.magic.md#object.sleep) призводить до попередження. Раніше видавалося повідомлення.

Предполагаемое использование[\_\_sleep()](language.oop5.magic.md#object.sleep) полягає в завершенні роботи над даними, що чекають на обробку або інших подібних завдань очищення. Крім того, цей метод може бути корисним, коли є дуже великі об'єкти, які немає потреби повністю зберігати.

З іншого боку, функція [unserialize()](function.unserialize.md) перевіряє наявність методу з магічним ім'ям [\_\_wakeup()](language.oop5.magic.md#object.wakeup). Якщо є, ця функція може відновлювати будь-які ресурси, які може мати об'єкт.

Предполагаемое использование[\_\_wakeup()](language.oop5.magic.md#object.wakeup) полягає у відновленні будь-яких з'єднань з базою даних, які могли бути втрачені під час операції серіалізації та виконання інших операцій повторної ініціалізації.

**Приклад #1 Серіалізація та десеріалізація**

```php
<?php
class Connection
{
    protected $link;
    private $dsn, $username, $password;

    public function __construct($dsn, $username, $password)
    {
        $this->dsn = $dsn;
        $this->username = $username;
        $this->password = $password;
        $this->connect();
    }

    private function connect()
    {
        $this->link = new PDO($this->dsn, $this->username, $this->password);
    }

    public function __sleep()
    {
        return array('dsn', 'username', 'password');
    }

    public function __wakeup()
    {
        $this->connect();
    }
}?>
```

### [\_\_serialize()](language.oop5.magic.md#object.serialize) і [\_\_unserialize()](language.oop5.magic.md#object.unserialize)

```methodsynopsis
public __serialize(): array
```

```methodsynopsis
public __unserialize(array $data): void
```

[serialize()](function.serialize.md) перевіряє, чи є у класі функція з магічним ім'ям [\_\_serialize()](language.oop5.magic.md#object.serialize). Якщо так, то функція виконується перед будь-якою серіалізацією. Вона має створити та повернути асоціативний масив пар ключ/значення, які представляють серіалізовану форму об'єкта. Якщо масив не повернутий, буде видано [TypeError](class.typeerror.md)

> **Зауваження** :
> 
> Якщо і [\_\_serialize()](language.oop5.magic.md#object.serialize) і [\_\_sleep()](language.oop5.magic.md#object.sleep) визначено в одному і тому ж об'єкті, буде викликано лише метод [\_\_serialize()](language.oop5.magic.md#object.serialize). . [\_\_sleep()](language.oop5.magic.md#object.sleep) ігноруватиметься. Якщо об'єкт реалізує інтерфейс [Serializable](class.serializable.md), метод`serialize()` інтерфейсу ігноруватиметься, а замість нього буде використаний [\_\_serialize()](language.oop5.magic.md#object.serialize)

Предполагаемое использование[\_\_serialize()](language.oop5.magic.md#object.serialize) полягає у визначенні зручного для серіалізації довільного уявлення об'єкта. Елементи масиву можуть відповідати властивостям об'єкта, але це необов'язково.

И наоборот,[unserialize()](function.unserialize.md) перевіряє наявність магічної функції [\_\_unserialize()](language.oop5.magic.md#object.unserialize). Якщо функція присутня, їй буде передано відновлений масив, який було повернено з [\_\_serialize()](language.oop5.magic.md#object.serialize). Потім він може відновити властивості об'єкта цього масиву відповідним чином.

> **Зауваження** :
> 
> Якщо і [\_\_unserialize()](language.oop5.magic.md#object.unserialize) і [\_\_wakeup()](language.oop5.magic.md#object.wakeup) визначено в одному і тому ж об'єкті, буде викликано лише метод [\_\_unserialize()](language.oop5.magic.md#object.unserialize). . [\_\_wakeup()](language.oop5.magic.md#object.wakeup) ігноруватиметься.

> **Зауваження** :
> 
> Функція доступна з PHP 7.4.0.

**Приклад #2 Серіалізація та десеріалізація**

```php
<?php
class Connection
{
    protected $link;
    private $dsn, $username, $password;

    public function __construct($dsn, $username, $password)
    {
        $this->dsn = $dsn;
        $this->username = $username;
        $this->password = $password;
        $this->connect();
    }

    private function connect()
    {
        $this->link = new PDO($this->dsn, $this->username, $this->password);
    }

    public function __serialize(): array
    {
        return [
          'dsn' => $this->dsn,
          'user' => $this->username,
          'pass' => $this->password,
        ];
    }

    public function __unserialize(array $data): void
    {
        $this->dsn = $data['dsn'];
        $this->username = $data['user'];
        $this->password = $data['pass'];

        $this->connect();
    }
}?>
```

### [\_\_toString()](language.oop5.magic.md#object.tostring)

```methodsynopsis
public __toString(): string
```

Метод[\_\_toString()](language.oop5.magic.md#object.tostring) дозволяє класу вирішувати, як він повинен реагувати при перетворенні на рядок. Наприклад, що вивести під час виконання `echo $obj;`

**Увага**

Починаючи з PHP 8.0.0, значення, що повертається слід стандартній семантиці типу PHP, що означає, що воно буде перетворено в рядок (string), якщо можливо, і якщо [strict typing](language.types.declarations.md#language.types.declarations.strict) вимкнено.

Об'єкт, що реалізує [Stringable](class.stringable.md) *не* буде прийматись оголошенням типу string, якщо включена [сувора типізація](language.types.declarations.md#language.types.declarations.strict). Якщо така поведінка необхідна, то оголошення типу має приймати інтерфейс. [Stringable](class.stringable.md) та рядок (string) за допомогою об'єднання типів.

Начиная с PHP 8.0.0, любой класс, содержащий метод[\_\_toString()](language.oop5.magic.md#object.tostring), також неявно реалізовуватиме інтерфейс [Stringable](class.stringable.md) і, таким чином, проходитиме перевірку типу для цього інтерфейсу У будь-якому випадку рекомендується явно реалізувати інтерфейс.

В PHP 7.4 возвращаемое значение*ПОВИННО* бути рядком (string), інакше видається [Error](class.error.md)

До PHP 7.4.0 возвращаемое значение*повинно* бути рядком (string), інакше видається фатальна помилка \*\*`E_RECOVERABLE_ERROR`\*\*is emitted.

**Увага**

Не можна викинути виняток із методу [\_\_toString()](language.oop5.magic.md#object.tostring) до PHP 7.4.0. Це призведе до фатальної помилки.

**Приклад #3 Простий приклад**

```php
<?php
// Объявление простого класса
class TestClass
{
    public $foo;

    public function __construct($foo)
    {
        $this->foo = $foo;
    }

    public function __toString()
    {
        return $this->foo;
    }
}

$class = new TestClass('Привет');
echo $class;
?>
```

Результат виконання наведеного прикладу:

```
Привет
```

### [\_\_invoke()](language.oop5.magic.md#object.invoke)

```methodsynopsis
__invoke( ...$values): mixed
```

Метод[\_\_invoke()](language.oop5.magic.md#object.invoke) викликається, коли скрипт намагається виконати об'єкт як функцію.

**Приклад #4 Использование[\_\_invoke()](language.oop5.magic.md#object.invoke)**

```php
<?php
class CallableClass
{
    public function __invoke($x)
    {
        var_dump($x);
    }
}
$obj = new CallableClass;
$obj(5);
var_dump(is_callable($obj));
?>
```

Результат виконання наведеного прикладу:

```
int(5)
bool(true)
```

**Приклад #5 Приклад использования[\_\_invoke()](language.oop5.magic.md#object.invoke)**

```php
<?php
class Sort
{
    private $key;

    public function __construct(string $key)
    {
        $this->key = $key;
    }

    public function __invoke(array $a, array $b): int
    {
        return $a[$this->key] <=> $b[$this->key];
    }
}

$customers = [
    ['id' => 1, 'first_name' => 'John', 'last_name' => 'Do'],
    ['id' => 3, 'first_name' => 'Alice', 'last_name' => 'Gustav'],
    ['id' => 2, 'first_name' => 'Bob', 'last_name' => 'Filipe']
];

// сортировка клиентов по имени
usort($customers, new Sort('first_name'));
print_r($customers);

// сортировка клиентов по фамилии
usort($customers, new Sort('last_name'));
print_r($customers);
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [0] => Array
        (
            [id] => 3
            [first_name] => Alice
            [last_name] => Gustav
        )

    [1] => Array
        (
            [id] => 2
            [first_name] => Bob
            [last_name] => Filipe
        )

    [2] => Array
        (
            [id] => 1
            [first_name] => John
            [last_name] => Do
        )

)
Array
(
    [0] => Array
        (
            [id] => 1
            [first_name] => John
            [last_name] => Do
        )

    [1] => Array
        (
            [id] => 2
            [first_name] => Bob
            [last_name] => Filipe
        )

    [2] => Array
        (
            [id] => 3
            [first_name] => Alice
            [last_name] => Gustav
        )

)
```

### [\_\_set\_state()](language.oop5.magic.md#object.set-state)

```methodsynopsis
static __set_state(array $properties): object
```

Цей [статичний](language.oop5.static.md) метод викликається тим класів, які експортуються функцією [var\_export()](function.var-export.md)

Єдиним параметром цього методу є масив, що містить властивості, що експортуються у вигляді `['property' => value, ...]`

**Приклад #6 Использование[\_\_set\_state()](language.oop5.magic.md#object.set-state)**

```php
<?php

class A
{
    public $var1;
    public $var2;

    public static function __set_state($an_array)
    {
        $obj = new A;
        $obj->var1 = $an_array['var1'];
        $obj->var2 = $an_array['var2'];
        return $obj;
    }
}

$a = new A;
$a->var1 = 5;
$a->var2 = 'foo';

$b = var_export($a, true);
var_dump($b);
eval('$c = ' . $b . ';');
var_dump($c);
?>
```

Результат виконання наведеного прикладу:

```
string(60) "A::__set_state(array(
   'var1' => 5,
   'var2' => 'foo',
))"
object(A)#2 (2) {
  ["var1"]=>
  int(5)
  ["var2"]=>
  string(3) "foo"
}
```

> **Зауваження**: Під час експорту об'єкту [var\_export()](function.var-export.md) не перевіряє, чи реалізує клас об'єкта метод [\_\_set\_state()](language.oop5.magic.md#object.set-state)тому повторний імпорт об'єктів призведе до виключення [Error](class.error.md), якщо метод \_\_set\_state() не реалізовано. Зокрема, це стосується деяких внутрішніх класів. Необхідність перевірки, чи реалізує імпортований клас метод \_\_set\_state(), повністю лежить на розробнику.

### [\_\_debugInfo()](language.oop5.magic.md#object.debuginfo)

```methodsynopsis
__debugInfo(): array
```

Цей метод викликається функцією [var\_dump()](function.var-dump.md), коли потрібно вивести список властивостей об'єкта. Якщо цей метод не визначений, тоді будуть виведені всі властивості об'єкта з модифікаторами public, protected та private.

**Приклад #7 Использование[\_\_debugInfo()](language.oop5.magic.md#object.debuginfo)**

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
