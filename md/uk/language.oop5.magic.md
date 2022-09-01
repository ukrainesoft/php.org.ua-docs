---
navigation:
  - language.oop5.iterations.md: « Ітератори об'єктів
  - language.oop5.final.md: Ключевое слово final »
  - index.md: PHP Manual
  - language.oop5.md: Класи та об'єкти
title: Магічні методи
---
## Магічні методи

Магічні методи – це спеціальні методи, які перевизначають дію PHP за умовчанням, коли над об'єктом виконуються певні дії.

**Застереження**

Всі імена методів, що починаються з `__`, зарезервовані PHP Не рекомендується використовувати імена методів з у PHP, якщо ви не бажаєте використовувати відповідну магічну функціональність.

Наступні назви методів вважаються магічними: [construct()](language.oop5.decon.html#object.construct) [destruct()](language.oop5.decon.html#object.destruct) [call()](language.oop5.overloading.html#object.call) [callStatic()](language.oop5.overloading.html#object.callstatic) [get()](language.oop5.overloading.html#object.get) [set()](language.oop5.overloading.html#object.set) [isset()](language.oop5.overloading.html#object.isset) [unset()](language.oop5.overloading.html#object.unset) [sleep()](language.oop5.magic.html#object.sleep) [wakeup()](language.oop5.magic.html#object.wakeup) [serialize()](language.oop5.magic.html#object.serialize) [unserialize()](language.oop5.magic.html#object.unserialize) [toString()](language.oop5.magic.html#object.tostring) [invoke()](language.oop5.magic.html#object.invoke) [setstate()](language.oop5.magic.html#object.set-state) [clone()](language.oop5.cloning.html#object.clone) і [debugInfo()](language.oop5.magic.html#object.debuginfo)

**Увага**

Усі магічні методи, за винятком [construct()](language.oop5.decon.html#object.construct) [destruct()](language.oop5.decon.html#object.destruct) і [clone()](language.oop5.cloning.html#object.clone) *ПОВИННІ* бути оголошені як `public`, інакше буде викликана помилка рівня **`E_WARNING`**. До PHP 8.0.0 для магічних методів [sleep()](language.oop5.magic.html#object.sleep) [wakeup()](language.oop5.magic.html#object.wakeup) [serialize()](language.oop5.magic.html#object.serialize) [unserialize()](language.oop5.magic.html#object.unserialize) і [setstate()](language.oop5.magic.html#object.set-state) не виконувалась перевірка.

**Увага**

Якщо оголошення типу використовуються для визначення магічного методу, вони повинні бути ідентичними сигнатурі, описаної в цьому документі. В іншому випадку видається фатальна помилка. До PHP 8.0.0 діагностичні повідомлення не надсилалися. Однак [construct()](language.oop5.decon.html#object.construct) і [destruct()](language.oop5.decon.html#object.destruct) не повинні оголошувати тип, що повертається; в іншому випадку видається фатальна помилка.

### [sleep()](language.oop5.magic.html#object.sleep) і [wakeup()](language.oop5.magic.html#object.wakeup)

```methodsynopsis
public __sleep(): array
```

```methodsynopsis
public __wakeup(): void
```

Функція [serialize()](function.serialize.md) перевіряє, чи є у класі метод із магічним ім'ям [sleep()](language.oop5.magic.html#object.sleep). Якщо це так, цей метод виконується до будь-якої операції серіалізації. Він може очистити об'єкт і повинен повертати масив з іменами всіх змінних цього об'єкта, які мають бути серіалізовані. Якщо метод нічого не повертає, то серіалізується **`null`** та видається попередження **`E_NOTICE`**

> **Зауваження**
> 
> Неприпустимо повертати в [sleep()](language.oop5.magic.html#object.sleep) імена закритих властивостей у батьківському класі. Це призведе до помилки рівня **`E_NOTICE`**. Натомість ви можете використовувати [serialize()](language.oop5.magic.html#object.serialize)

Передбачуване використання [sleep()](language.oop5.magic.html#object.sleep) полягає в завершенні роботи над даними, що чекають на обробку або інших подібних завдань очищення. Крім того, цей метод може бути корисним, коли є дуже великі об'єкти, які немає потреби повністю зберігати.

З іншого боку, функція [unserialize()](function.unserialize.md) перевіряє наявність методу з магічним ім'ям [wakeup()](language.oop5.magic.html#object.wakeup). Якщо є, ця функція може відновлювати будь-які ресурси, які може мати об'єкт.

Передбачуване використання [wakeup()](language.oop5.magic.html#object.wakeup) полягає у відновленні будь-яких з'єднань з базою даних, які могли бути втрачені під час операції серіалізації та виконання інших операцій повторної ініціалізації.

**Приклад #1 Серіалізація та десеріалізація**

```php
<?php
class Connection
{
    protected $link;
    private $dsn, $username, $password;

    public function __construct($dsn, $username, $password)
    {
        $this->dsn = $dsn;
        $this->username = $username;
        $this->password = $password;
        $this->connect();
    }

    private function connect()
    {
        $this->link = new PDO($this->dsn, $this->username, $this->password);
    }

    public function __sleep()
    {
        return array('dsn', 'username', 'password');
    }

    public function __wakeup()
    {
        $this->connect();
    }
}?>
```

### [serialize()](language.oop5.magic.html#object.serialize) і [unserialize()](language.oop5.magic.html#object.unserialize)

```methodsynopsis
public __serialize(): array
```

```methodsynopsis
public __unserialize(array $data): void
```

[serialize()](function.serialize.md) перевіряє, чи є у класі функція з магічним ім'ям [serialize()](language.oop5.magic.html#object.serialize). Якщо так, то функція виконується перед будь-якою серіалізацією. Вона повинна створити та повернути асоціативний масив пар ключ/значення, які представляють серіалізовану форму об'єкта. Якщо масив не повернутий, буде видано [TypeError](class.typeerror.md)

> **Зауваження**
> 
> Якщо і [serialize()](language.oop5.magic.html#object.serialize) і [sleep()](language.oop5.magic.html#object.sleep) визначено в одному і тому ж об'єкті, буде викликано лише метод [serialize()](language.oop5.magic.html#object.serialize). . [sleep()](language.oop5.magic.html#object.sleep) ігноруватиметься. Якщо об'єкт реалізує інтерфейс [Serializable](class.serializable.md), метод `serialize()` інтерфейсу ігноруватиметься, а замість нього буде використаний [serialize()](language.oop5.magic.html#object.serialize)

Передбачуване використання [serialize()](language.oop5.magic.html#object.serialize) полягає у визначенні зручного для серіалізації довільного уявлення об'єкта. Елементи масиву можуть відповідати властивостям об'єкта, але не обов'язково.

І навпаки, [unserialize()](function.unserialize.md) перевіряє наявність магічної функції [unserialize()](language.oop5.magic.html#object.unserialize). Якщо функція присутня, їй буде передано відновлений масив, який було повернено з [serialize()](language.oop5.magic.html#object.serialize). Потім він може відновити властивості об'єкта цього масиву відповідним чином.

> **Зауваження**
> 
> Якщо і [unserialize()](language.oop5.magic.html#object.unserialize) і [wakeup()](language.oop5.magic.html#object.wakeup) визначено в одному і тому ж об'єкті, буде викликано лише метод [unserialize()](language.oop5.magic.html#object.unserialize). . [wakeup()](language.oop5.magic.html#object.wakeup) ігноруватиметься.

> **Зауваження**
> 
> Функція доступна з PHP 7.4.0.

**Приклад #2 Серіалізація та десеріалізація**

```php
<?php
class Connection
{
    protected $link;
    private $dsn, $username, $password;

    public function __construct($dsn, $username, $password)
    {
        $this->dsn = $dsn;
        $this->username = $username;
        $this->password = $password;
        $this->connect();
    }

    private function connect()
    {
        $this->link = new PDO($this->dsn, $this->username, $this->password);
    }

    public function __serialize(): array
    {
        return [
          'dsn' => $this->dsn,
          'user' => $this->username,
          'pass' => $this->password,
        ];
    }

    public function __unserialize(array $data): void
    {
        $this->dsn = $data['dsn'];
        $this->username = $data['user'];
        $this->password = $data['pass'];

        $this->connect();
    }
}?>
```

### [toString()](language.oop5.magic.html#object.tostring)

```methodsynopsis
public __toString(): string
```

Метод [toString()](language.oop5.magic.html#object.tostring) дозволяє класу вирішувати, як він повинен реагувати при перетворенні на рядок. Наприклад, що вивести під час виконання `echo $obj;`

**Увага**

Починаючи з PHP 8.0.0, значення, що повертається слід стандартній семантиці типу PHP, що означає, що воно буде перетворене в рядок (string), якщо можливо, і якщо [strict typing](language.types.declarations.html#language.types.declarations.strict) вимкнено.

Починаючи з PHP 8.0.0, будь-який клас, що містить метод [toString()](language.oop5.magic.html#object.tostring), також неявно реалізовуватиме інтерфейс [Stringable](class.stringable.md) і, таким чином, буде проходити перевірку типу для цього інтерфейсу. У будь-якому випадку рекомендується явно реалізувати інтерфейс.

У PHP 7.4 значення, що повертається *ПОВИННО* бути рядком (string), інакше видається [Error](class.error.md)

До PHP 7.4.0 значення, що повертається *повинно* бути рядком (string), інакше видається фатальна помилка **`E_RECOVERABLE_ERROR`**. is emitted.

**Увага**

Не можна викинути виняток із методу [toString()](language.oop5.magic.html#object.tostring) до PHP 7.4.0. Це призведе до фатальної помилки.

**Приклад #3 Простий приклад**

```php
<?php
// Объявление простого класса
class TestClass
{
    public $foo;

    public function __construct($foo)
    {
        $this->foo = $foo;
    }

    public function __toString()
    {
        return $this->foo;
    }
}

$class = new TestClass('Привет');
echo $class;
?>
```

Результат виконання цього прикладу:

```
Привет
```

### [invoke()](language.oop5.magic.html#object.invoke)

```methodsynopsis
__invoke( ...$values): mixed
```

Метод [invoke()](language.oop5.magic.html#object.invoke) викликається, коли скрипт намагається виконати об'єкт як функцію.

**Приклад #4 Використання [invoke()](language.oop5.magic.html#object.invoke)**

```php
<?php
class CallableClass
{
    public function __invoke($x)
    {
        var_dump($x);
    }
}
$obj = new CallableClass;
$obj(5);
var_dump(is_callable($obj));
?>
```

Результат виконання цього прикладу:

```
int(5)
bool(true)
```

### [setstate()](language.oop5.magic.html#object.set-state)

```methodsynopsis
static __set_state(array $properties): object
```

Цей [статичний](language.oop5.static.md) метод викликається тим класів, які експортуються функцією [varexport()](function.var-export.html)

Єдиним параметром цього методу є масив, що містить властивості, що експортуються у вигляді `['property' => value, ...]`

**Приклад #5 Використання [setstate()](language.oop5.magic.html#object.set-state)**

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

$b = var_export($a, true);
var_dump($b);
eval('$c = ' . $b . ';');
var_dump($c);
?>
```

Результат виконання цього прикладу:

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

> **Зауваження**: Під час експорту об'єкту [varexport()](function.var-export.html) не перевіряє, чи реалізує клас об'єкта метод [setstate()](language.oop5.magic.html#object.set-state)тому повторний імпорт об'єктів призведе до виключення [Error](class.error.md), якщо метод setstate() не реалізовано. Зокрема, це стосується деяких внутрішніх класів. Необхідність перевірки, чи реалізує імпортований клас метод setstate(), повністю лежить на розробнику.

### [debugInfo()](language.oop5.magic.html#object.debuginfo)

```methodsynopsis
__debugInfo(): array
```

Цей метод викликається функцією [vardump()](function.var-dump.html), коли потрібно вивести список властивостей об'єкта. Якщо цей метод не визначений, тоді будуть виведені всі властивості об'єкта з модифікаторами public, protected та private.

**Приклад #6 Використання [debugInfo()](language.oop5.magic.html#object.debuginfo)**

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
