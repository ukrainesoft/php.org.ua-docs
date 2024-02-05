---
navigation:
  - language.oop5.abstract.md: « Абстрактні класи
  - language.oop5.traits.md: Трейти »
  - index.md: PHP Manual
  - language.oop5.md: Класи та об'єкти
title: Інтерфейси об'єктів
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Інтерфейси об'єктів

Інтерфейси об'єктів дозволяють створювати код, який вказує, які методи має реалізувати клас, без необхідності визначати, як саме вони мають бути реалізовані. Інтерфейси поділяють простір імен із класами та трейтами, тому вони не можуть називатися однаково.

Інтерфейси оголошуються так само, як і звичайні класи, але з використанням ключового слова `interface` замість `class`. Тіла методів інтерфейсів мають бути порожніми.

Усі методи, визначені в інтерфейсах, мають бути загальнодоступними, що випливає із самої природи інтерфейсу.

На практиці інтерфейси використовуються у двох взаємодоповнюючих випадках:

-   Щоб дозволити розробникам створювати об'єкти різних класів, які можуть використовуватися взаємозамінно, оскільки вони реалізують той самий інтерфейс або інтерфейси. Типовий приклад – кілька служб доступу до бази даних, кілька платіжних шлюзів або різних стратегій кешування. Різні реалізації можуть бути замінені без будь-яких змін у коді, що їх використовує.
-   Щоб дозволити функції або методу приймати та оперувати параметром, який відповідає інтерфейсу, не переймаючись тим, що ще може робити об'єкт або як він реалізований. Ці інтерфейси часто називають`Iterable` `Cacheable` `Renderable`і так далі, щоб описати їхню поведінку.

Інтерфейси можуть визначати [магічні методи](language.oop5.magic.md), Вимагаючи від реалізуючих класів реалізації цих методів.

> **Зауваження** :
> 
> Хотя они поддерживаются, использование[конструкторів](language.oop5.decon.md#language.oop5.decon.constructor) в інтерфейсах не рекомендується. Це значно знижує гнучкість об'єкта, що реалізує інтерфейс. Крім того, до конструкторів не застосовуються правила успадкування, що може призвести до суперечливої ​​та несподіваної поведінки.

### `implements`

Для реализации интерфейса используется оператор`implements`. Клас повинен реалізувати всі методи, описані в інтерфейсі, інакше буде фатальна помилка. За бажанням класи можуть реалізовувати більше одного інтерфейсу, розділяючи кожен інтерфейс комою.

**Увага**

Клас, що реалізує інтерфейс, може використовувати для своїх параметрів ім'я, відмінне від імені інтерфейсу. Однак, починаючи з PHP 8.0, у мові підтримуються [іменовані аргументи](functions.arguments.md#functions.named-arguments), і код, що викликає, може покладатися на ім'я параметра в інтерфейсі. З цієї причини рекомендується, щоб розробники використовували ті ж імена параметрів, що і інтерфейс, що реалізується.

> **Зауваження** :
> 
> Інтерфейси можуть бути успадковані один від одного, так само, як і класи, за допомогою оператора [extends](language.oop5.inheritance.md)

> **Зауваження** :
> 
> Клас, що реалізує інтерфейс, повинен оголосити всі методи в інтерфейсі з [сумісною сигнатурою](language.oop5.basic.md#language.oop.lsp). Клас може реалізовувати кілька інтерфейсів, які оголошують метод із однаковим ім'ям. У цьому випадку реалізація має слідувати [правилам сумісності сигнатури](language.oop5.basic.md#language.oop.lsp) для інтерфейсів. Таким чином, можна застосовувати [коваріантність та контраваріантність](language.oop5.variance.md)

### Константи

Інтерфейси можуть містити константи. Константи інтерфейсів працюють так само, як і [константи класів](language.oop5.constants.md). До PHP 8.1.0 вони не могли бути перевизначені класом чи інтерфейсом, що їх успадковує.

### Приклади

**Приклад #1 Приклад інтерфейсу**

```php
<?php

// Объявим интерфейс 'Template'
interface Template
{
    public function setVariable($name, $var);
    public function getHtml($template);
}

// Реализация интерфейса
// Это будет работать
class WorkingTemplate implements Template
{
    private $vars = [];

    public function setVariable($name, $var)
    {
        $this->vars[$name] = $var;
    }

    public function getHtml($template)
    {
        foreach($this->vars as $name => $value) {
            $template = str_replace('{' . $name . '}', $value, $template);
        }

        return $template;
    }
}

// Это не будет работать
// Fatal error: Class BadTemplate contains 1 abstract methods
// and must therefore be declared abstract (Template::getHtml)
// (Фатальная ошибка: Класс BadTemplate содержит 1 абстрактный метод
// и поэтому должен быть объявлен абстрактным (Template::getHtml))
class BadTemplate implements Template
{
    private $vars = [];

    public function setVariable($name, $var)
    {
        $this->vars[$name] = $var;
    }
}
?>
```

**Приклад #2 Спадкування інтерфейсів**

```php
<?php
interface A
{
    public function foo();
}

interface B extends A
{
    public function baz(Baz $baz);
}

// Это сработает
class C implements B
{
    public function foo()
    {
    }

    public function baz(Baz $baz)
    {
    }
}

// Это не сработает и выдаст фатальную ошибку
class D implements B
{
    public function foo()
    {
    }

    public function baz(Foo $foo)
    {
    }
}
?>
```

**Приклад #3 Сумісність із кількома інтерфейсами**

```php
<?php
class Foo {}
class Bar extends Foo {}

interface A {
    public function myfunc(Foo $arg): Foo;
}

interface B {
    public function myfunc(Bar $arg): Bar;
}

class MyClass implements A, B
{
    public function myfunc(Foo $arg): Bar
    {
        return new Bar();
    }
}
?>
```

**Приклад #4 Множинне наслідування інтерфейсів**

```php
<?php
interface A
{
    public function foo();
}

interface B
{
    public function bar();
}

interface C extends A, B
{
    public function baz();
}

class D implements C
{
    public function foo()
    {
    }

    public function bar()
    {
    }

    public function baz()
    {
    }
}
?>
```

**Приклад #5 Інтерфейси з константами**

```php
<?php
interface A
{
    const B = 'Константа интерфейса';
}

// Выведет: Константа интерфейса
echo A::B;


class B implements A
{
    const B = 'Константа класса';
}

// Выведет: Константа класса
// До PHP 8.1.0 этот код не будет работать,
// потому что было нельзя переопределять константы.
echo B::B;
?>
```

**Приклад #6 Інтерфейси з абстрактними класами**

```php
<?php
interface A
{
    public function foo(string $s): string;

    public function bar(int $i): int;
}

// Абстрактный класс может реализовывать только часть интерфейса.
// Классы, расширяющие абстрактный класс, должны реализовать все остальные.
abstract class B implements A
{
    public function foo(string $s): string
    {
        return $s . PHP_EOL;
    }
}

class C extends B
{
    public function bar(int $i): int
    {
        return $i * 2;
    }
}
?>
```

**Приклад #7 Одночасне розширення та впровадження**

```php
<?php

class One
{
    /* ... */
}

interface Usable
{
    /* ... */
}

interface Updatable
{
    /* ... */
}

// Порядок ключевых слов здесь важен. "extends" должно быть первым.
class Two extends One implements Usable, Updatable
{
    /* ... */
}
?>
```

Інтерфейс, разом із оголошеннями типів, надає відмінний спосіб перевірки те, що певний об'єкт містить певний набір методів. Дивіться також оператор [instanceof](language.operators.type.md) і [оголошення типів](language.types.declarations.md)
