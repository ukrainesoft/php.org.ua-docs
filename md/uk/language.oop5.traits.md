---
navigation:
  - language.oop5.interfaces.md: « Інтерфейси об'єктів
  - language.oop5.anonymous.md: Анонімні класи »
  - index.md: PHP Manual
  - language.oop5.md: Класи та об'єкти
title: Трейти
---
## Трейти

PHP реалізує метод повторного використання коду під назвою трейт (trait).

Трейт - це механізм забезпечення повторного використання коду в мовах із підтримкою лише одиночного успадкування, таких як PHP. Трейт призначений зменшення деяких обмежень одиночного успадкування, дозволяючи розробнику повторно використовувати набори методів вільно, у кількох незалежних класах і реалізованих з допомогою різних архітектур побудови класів. Семантика комбінації трейтів та класів визначена таким чином, щоб знизити рівень складності, а також уникнути типових проблем, пов'язаних із множинним спадкуванням та змішуванням (mixins).

Трейт дуже схожий на клас, але призначений для групування функціоналу добре структурованим та послідовним чином. Неможливо створити самостійний екземпляр трейту. Це доповнення до звичайного успадкування і дозволяє зробити горизонтальну композицію поведінки, тобто застосування членів класу без наслідування.

**Приклад #1 Приклад використання трейту**

```php
<?php
trait ezcReflectionReturnInfo {
    function getReturnType() { /*1*/ }
    function getReturnDescription() { /*2*/ }
}

class ezcReflectionMethod extends ReflectionMethod {
    use ezcReflectionReturnInfo;
    /* ... */
}

class ezcReflectionFunction extends ReflectionFunction {
    use ezcReflectionReturnInfo;
    /* ... */
}
?>
```

### Пріоритет

Спадкований член з базового класу перевизначається членом, який у трейте. Порядок пріоритету наступний: члени з поточного класу перевизначають методи у трейті, які у свою чергу перевизначають успадковані методи.

**Приклад #2 Приклад пріоритету старшинства**

Спадкований метод від базового класу перевизначається методом, доданим MyHelloWorld з трейту SayWorld. Поведінка така сама як і для методів, визначених у класі MyHelloWorld. Порядок пріоритету такий: методи із поточного класу перевизначають методи трейту, які у свою чергу перевизначають методи з базового класу.

```php
<?php
class Base {
    public function sayHello() {
        echo 'Hello ';
    }
}

trait SayWorld {
    public function sayHello() {
        parent::sayHello();
        echo 'World!';
    }
}

class MyHelloWorld extends Base {
    use SayWorld;
}

$o = new MyHelloWorld();
$o->sayHello();
?>
```

Результат виконання цього прикладу:

```
Hello World!
```

**Приклад #3 Приклад альтернативного порядку пріоритету**

```php
<?php
trait HelloWorld {
    public function sayHello() {
        echo 'Hello World!';
    }
}

class TheWorldIsNotEnough {
    use HelloWorld;
    public function sayHello() {
        echo 'Hello Universe!';
    }
}

$o = new TheWorldIsNotEnough();
$o->sayHello();
?>
```

Результат виконання цього прикладу:

```
Hello Universe!
```

### Декілька трейтів

До класу можна додати кілька трейтів, перерахувавши їх у директиві `use` через кому.

**Приклад #4 Приклад використання кількох трейтів**

```php
<?php
trait Hello {
    public function sayHello() {
        echo 'Hello ';
    }
}

trait World {
    public function sayWorld() {
        echo 'World';
    }
}

class MyHelloWorld {
    use Hello, World;
    public function sayExclamationMark() {
        echo '!';
    }
}

$o = new MyHelloWorld();
$o->sayHello();
$o->sayWorld();
$o->sayExclamationMark();
?>
```

Результат виконання цього прикладу:

```
Hello World!
```

### Вирішення конфліктів

Якщо два трейти додають метод з тим самим ім'ям, це призводить до фатальної помилки у випадку, якщо конфлікт явно не вирішений.

Для вирішення конфліктів іменування між трейтами, що використовуються в тому самому класі, необхідно використовувати оператор `insteadof` для того, щоб точно вибрати один із конфліктуючих методів.

Оскільки попередній оператор дозволяє лише виключати методи, оператор `as` може бути використаний включення одного з конфліктуючих методів під іншим ім'ям. Зверніть увагу, що оператор `as` не перейменовує метод і не впливає на будь-який інший метод.

**Приклад #5 Приклад вирішення конфліктів**

У цьому прикладі Talker використовує трейти A і B. Так як в A і B є методи, що конфліктують, він використовує варіант smallTalk з трейту B, а варіант bigTalk - з трейту A.

Клас AliasedTalker застосовує оператор `as`щоб отримати можливість використовувати реалізацію bigTalk з B під додатковим псевдонімом `talk`

```php
<?php
trait A {
    public function smallTalk() {
        echo 'a';
    }
    public function bigTalk() {
        echo 'A';
    }
}

trait B {
    public function smallTalk() {
        echo 'b';
    }
    public function bigTalk() {
        echo 'B';
    }
}

class Talker {
    use A, B {
        B::smallTalk insteadof A;
        A::bigTalk insteadof B;
    }
}

class Aliased_Talker {
    use A, B {
        B::smallTalk insteadof A;
        A::bigTalk insteadof B;
        B::bigTalk as talk;
    }
}
?>
```

### Зміна видимості методу

Використовуючи синтаксис оператора `as`, можна також змінити видимість методу у класі, що використовує трейт.

**Приклад #6 Приклад зміни видимості методу**

```php
<?php
trait HelloWorld {
    public function sayHello() {
        echo 'Hello World!';
    }
}

// Изменение видимости метода sayHello
class MyClass1 {
    use HelloWorld { sayHello as protected; }
}

// Создание псевдонима метода с изменённой видимостью
// видимость sayHello не изменилась
class MyClass2 {
    use HelloWorld { sayHello as private myPrivateHello; }
}
?>
```

### Трейти, що складаються з трейтів

Трейти можуть використовуватись як у класах, так і в інших трейтах. Використовуючи один або більше трейтів для визначення іншого трейту, він може частково або повністю складатися з членів, визначених у цих трейтах.

**Приклад #7 Приклад трейтів, складених із трейтів**

```php
<?php
trait Hello {
    public function sayHello() {
        echo 'Hello ';
    }
}

trait World {
    public function sayWorld() {
        echo 'World!';
    }
}

trait HelloWorld {
    use Hello, World;
}

class MyHelloWorld {
    use HelloWorld;
}

$o = new MyHelloWorld();
$o->sayHello();
$o->sayWorld();
?>
```

Результат виконання цього прикладу:

```
Hello World!
```

### Абстрактні члени трейтів

Трейти підтримують використання абстрактних методів для того, щоб встановити вимоги до класу, що використовує. Підтримуються загальнодоступні, захищені та закриті методи. До PHP 8.0.0 підтримувалися лише загальнодоступні та захищені абстрактні методи.

**Застереження**

Конкретний клас виконує ці вимоги шляхом визначення конкретного методу з тим самим ім'ям; при цьому сигнатура методу може відрізнятись.

**Приклад #8 Вимоги трейту за допомогою абстрактних методів**

```php
<?php
trait Hello {
    public function sayHelloWorld() {
        echo 'Hello'.$this->getWorld();
    }
    abstract public function getWorld();
}

class MyHelloWorld {
    private $world;
    use Hello;
    public function getWorld() {
        return $this->world;
    }
    public function setWorld($val) {
        $this->world = $val;
    }
}
?>
```

### Статичні члени трейту

У трейтах можна визначати статичні змінні, статичні методи та статичні властивості.

> **Зауваження**
> 
> Починаючи з PHP 8.1.0, виклик статичного методу або доступ до статичної властивості безпосередньо у трейті застарів. До статичних методів та властивостей слід звертатися лише у класі, який використовує трейт.

**Приклад #9 Статичні змінні**

```php
<?php
trait Counter {
    public function inc() {
        static $c = 0;
        $c = $c + 1;
        echo "$c\n";
    }
}

class C1 {
    use Counter;
}

class C2 {
    use Counter;
}

$o = new C1(); $o->inc(); // echo 1
$p = new C2(); $p->inc(); // echo 1
?>
```

**Приклад #10 Статичні методи**

```php
<?php
trait StaticExample {
    public static function doSomething() {
        return 'Что-либо делаем';
    }
}

class Example {
    use StaticExample;
}

Example::doSomething();
?>
```

**Приклад #11 Статичні властивості**

```php
<?php
trait StaticExample {
    public static $static = 'foo';
}
class Example {
    use StaticExample;
}
echo Example::$static;
?>
```

### Властивості

Трейти можуть також визначати властивості.

**Приклад #12 Визначення властивостей**

```php
<?php
trait PropertiesTrait {
    public $x = 1;
}

class PropertiesExample {
    use PropertiesTrait;
}

$example = new PropertiesExample;
$example->x;
?>
```

Якщо трейт визначає властивість, клас не може визначити властивість з таким же ім'ям, крім випадків повного збігу (те ж початкове значення і модифікатор видимості), інакше буде згенерована фатальна помилка.

**Приклад #13 Вирішення конфліктів**

```php
<?php
trait PropertiesTrait {
    public $same = true;
    public $different = false;
}

class PropertiesExample {
    use PropertiesTrait;
    public $same = true;
    public $different = true; // Фатальная ошибка
}
?>
```
