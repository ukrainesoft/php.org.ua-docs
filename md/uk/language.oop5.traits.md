---
navigation:
  - language.oop5.interfaces.md: « Інтерфейси об'єктів
  - language.oop5.anonymous.md: Анонімні класи »
  - index.md: PHP Manual
  - language.oop5.md: Класи та об'єкти
title: Трейти
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Трейти

PHP реалізує спосіб перевикористання коду, званий трейтами (Traits).

Трейт - це механізм перевикористання коду в мовах з підтримкою поодинокого успадкування, до яких належить PHP. Завдання трейту - зменшити обмеження одиночного успадкування, дозволяючи розробнику легко перевикористовувати набори методів у кількох незалежних класах, що у різних ієрархіях класів. Семантика комбінації трейтів та класів визначена так, щоб знизити рівень складності, а також уникнути типових проблем, властивих множинному спадкуванню та домішкам (Mixins).

Трейт дуже схожий на клас, але розрахований лише на угруповання функціональності тонко контрольованим та узгодженим чином. Не можна створити окремий примірник трейту. Трейт — це доповнення до звичайного успадкування та інструмент побудови горизонтальної композиції поведінки, тобто роботи з членами класу (трейту) без вимоги успадкування.

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

Член, успадкований із базового класу, перевизначається членом, введеним трейтом. Порядок пріоритету наступний: члени поточного класу перевизначають методи трейту, які зі свого боку перевизначають успадковані методи.

**Приклад #2 Приклад пріоритету старшинства**

Спадкований від базового класу метод перевизначається методом, доданим у клас MyHelloWorld із трейту SayWorld. Поведінка методів трейту повторює поведінку методів класу MyHelloWorld. Порядок пріоритету такий: методи поточного класу перевизначають методи трейту, які зі свого боку перевизначають методи базового класу.

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

Результат виконання наведеного прикладу:

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

Результат виконання наведеного прикладу:

```
Hello Universe!
```

### Декілька трейтів

До класу можна додати кілька трейтів, перерахувавши їх у директиві `use`через запятую.

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

Результат виконання наведеного прикладу:

```
Hello World!
```

### Вирішення конфліктів

Якщо два трейти додають метод з тим самим ім'ям, буде викликана фатальна помилка, якщо конфлікт явно не вирішений.

Для вирішення конфліктів іменування між трейтами, включеними в той самий клас, викликають оператор `insteadof`, щоб точно вибрати один із конфліктуючих методів.

Оскільки попередній оператор тільки виключає методи, оператор `as` може включити один із конфліктуючих методів під іншим ім'ям. Зверніть увагу, що оператор `as` не перейменовує метод, а також не впливає на будь-який інший метод.

**Приклад #5 Приклад вирішення конфліктів**

У цьому прикладі клас Talker включені трейти A і B. Оскільки в трейтах A і B є конфліктуючі методи, клас використовує варіант методу smallTalk з трейту B, а варіант методу bigTalk — з трейту A.

Клас Aliased\_Talker застосовує оператор `as`, щоб використати реалізацію методу bigTalk із класу B під додатковим псевдонімом `talk`

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

Применяя оператор`as`, можна також змінити видимість методу у класі, до якого включено трейт.

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

Трейти можна включати і до класів, і до інших трейтів. Трейт може бути повністю або частково складений із членів, описаних в інших трейтах, один або кілька з яких включені до визначення трейту.

**Приклад #7 Приклад трейтів, що складаються з трейтів**

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

Результат виконання наведеного прикладу:

```
Hello World!
```

### Абстрактні члени трейтів

Трейти підтримують абстрактні методи, щоб встановити вимоги до класу, до якого буде включено трейт. Підтримуються загальнодоступні, захищені та закриті методи. До PHP 8.0.0 підтримувалися лише загальнодоступні та захищені абстрактні методи.

**Застереження**

Начиная с PHP 8.0.0 сигнатура конкретного метода должна следовать[правилам сумісності сигнатур](language.oop5.basic.md#language.oop.lsp)Ранее сигнатура метода могла несовпадать.

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

> **Зауваження** :
> 
> Починаючи з PHP 8.1.0 прямий виклик статичного методу або прямий доступ до статичної властивості у трейті застарілий. До статичних методів і властивостей потрібно звертатися лише у класі, до якого включено трейт.

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
        echo 'Что-либо делаем';
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

Трейти також можуть визначати властивості.

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

Якщо трейт визначає властивість, то клас не може визначити властивість з таким самим ім'ям, крім випадків повного збігу (та сама область видимості і тип, модифікатор readonly і початкове значення), інакше буде викинуто фатальну помилку.

**Приклад #13 Вирішення конфліктів**

```php
<?php
trait PropertiesTrait {
    public $same = true;
    public $different1 = false;
    public bool $different2;
    public bool $different3;
}

class PropertiesExample {
    use PropertiesTrait;
    public $same = true;
    public $different1 = true; // Фатальная ошибка
    public string $different2; // Фатальная ошибка
    readonly protected bool $different3; // Фатальная ошибка
}
?>
```

### Константи

Починаючи з версії PHP 8.2.0, трейти можуть також визначати константи.

**Приклад #14 Визначення констант**

```php
<?php
trait ConstantsTrait {
    public const FLAG_MUTABLE = 1;
    final public const FLAG_IMMUTABLE = 5;
}

class ConstantsExample {
    use ConstantsTrait;
}

$example = new ConstantsExample;
echo $example::FLAG_MUTABLE; // 1
?>
```

Якщо трейт визначає константу, то клас не може визначити константу з таким же ім'ям, якщо вони не сумісні (однакова область видимості, початкове значення і модифікатор final), інакше викидається фатальна помилка.

**Приклад #15 Вирішення конфліктів**

```php
<?php
trait ConstantsTrait {
    public const FLAG_MUTABLE = 1;
    final public const FLAG_IMMUTABLE = 5;
}

class ConstantsExample {
    use ConstantsTrait;
    public const FLAG_IMMUTABLE = 5; // Фатальная ошибка
}
?>
```
