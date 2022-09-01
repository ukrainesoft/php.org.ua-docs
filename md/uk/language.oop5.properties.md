---
navigation:
  - language.oop5.basic.md: « Основи
  - language.oop5.constants.md: Константи класів »
  - index.md: PHP Manual
  - language.oop5.md: Класи та об'єкти
title: Властивості
---
## Властивості

Змінні, які є членами класу, називаються *властивості*. Також їх називають, використовуючи інші терміни, такі як *поля*, але в рамках цієї документації, ми будемо називати їх *властивостями*. Вони визначаються з використанням хоча б одного необов'язкового (за винятком `readonly`властивостей) модифікатора (наприклад, [Область видимості](language.oop5.visibility.md) [Ключевое слово static](language.oop5.static.md) або, починаючи з PHP 8.1.0, [readonly](language.oop5.properties.html#language.oop5.properties.readonly-properties)), починаючи з PHP 7.4, за яким слідує необов'язкове оголошення типу, за яким слідує звичайне оголошення змінної. Це оголошення може містити ініціалізацію, але ця ініціалізація має бути [постійним значенням](language.constants.md)

> **Зауваження**
> 
> Застарілий спосіб оголошення властивостей класу – використання ключового слова `var` замість модифікатора.

> **Зауваження**: Властивість, оголошена без модифікатора [Область видимості](language.oop5.visibility.md), буде оголошено як `public`

У межах методів класу доступ до нестатичних властивостей може бути отриманий за допомогою `->` (об'єктного оператора): $this->property (де `property` - Ім'я якості). Доступ до статичних властивостей здійснюється за допомогою `::` (подвійного двокрапки): self::$property. Додаткову інформацію про відмінність статичних та нестатичних властивостей дивіться у розділі [Ключевое слово static](language.oop5.static.md)

Псевдозмінна $this доступна всередині будь-якого методу класу, коли цей метод викликається з контексту об'єкта. $this - значення об'єкта, що викликає.

**Приклад #1 Визначення властивостей**

```php
<?php
class SimpleClass
{
   public $var1 = 'hello ' . 'world';
   public $var2 = <<<EOD
hello world
EOD;
   public $var3 = 1+2;
   // неправильное определение свойств:
   public $var4 = self::myStaticMethod();
   public $var5 = $myVar;

   // правильное определение свойств:
   public $var6 = myConstant;
   public $var7 = [true, false];

   public $var8 = <<<'EOD'
hello world
EOD;

   // Без модификатора области видимости:
   static $var9;
   readonly int $var10;

}
?>
```

> **Зауваження**
> 
> Існують різні функції для обробки класів та об'єктів. Дивіться довідник з [функцій для класів/об'єктів](ref.classobj.md)

### Оголошення типів

Починаючи з PHP 7.4.0, визначення властивостей можуть містити [Оголошення типів](language.types.declarations.md), за винятком типу [callable](language.types.callable.md)

**Приклад #2 Приклад використання типизованих властивостей**

```php
<?php

class User
{
    public int $id;
    public ?string $name;

    public function __construct(int $id, ?string $name)
    {
        $this->id = $id;
        $this->name = $name;
    }
}

$user = new User(1234, null);

var_dump($user->id);
var_dump($user->name);

?>
```

Результат виконання цього прикладу:

```
int(1234)
NULL
```

Перед зверненням до типізованої властивості у нього має бути задане значення, інакше буде викинуто виняток [Error](class.error.md)

**Приклад #3 Звернення до властивостей**

```php
<?php

class Shape
{
    public int $numberOfSides;
    public string $name;

    public function setNumberOfSides(int $numberOfSides): void
    {
        $this->numberOfSides = $numberOfSides;
    }

    public function setName(string $name): void
    {
        $this->name = $name;
    }

    public function getNumberOfSides(): int
    {
        return $this->numberOfSides;
    }

    public function getName(): string
    {
        return $this->name;
    }
}

$triangle = new Shape();
$triangle->setName("triangle");
$triangle->setNumberofSides(3);
var_dump($triangle->getName());
var_dump($triangle->getNumberOfSides());

$circle = new Shape();
$circle->setName("circle");
var_dump($circle->getName());
var_dump($circle->getNumberOfSides());
?>
```

Результат виконання цього прикладу:

```
string(8) "triangle"
int(3)
string(6) "circle"

Fatal error: Uncaught Error: Typed property Shape::$numberOfSides must not be accessed before initialization
```

### Readonly-властивості

Починаючи з PHP 8.1.0, властивість можна оголосити за допомогою модифікатора `readonly`, який запобігає зміні властивості після ініціалізації.

**Приклад #4 Приклади readonly-властивостей**

```php
<?php
class Test {
   public readonly string $prop;
   public function __construct(string $prop) {
       // Правильная инициализация.
       $this->prop = $prop;
   }
}
$test = new Test("foobar");
// Правильное чтение.
var_dump($test->prop); // string(6) "foobar"
// Неправильное переопределение. Не имеет значения, что присвоенное значение такое же.
$test->prop = "foobar";
// Ошибка: невозможно изменить readonly-свойство Test::$prop
?>
```

> **Зауваження**
> 
> Модифікатор readonly може застосовуватися тільки до [типізованим властивостям](language.oop5.properties.html#language.oop5.properties.typed-properties). Readonly-властивість без обмежень типу можна створити за допомогою типу [mixed](language.types.declarations.html#language.types.declarations.mixed)

> **Зауваження**
> 
> Статичні реально-властивості не підтримуються.

Readonly-властивість можна ініціалізувати лише один раз і тільки з області, в якій вона була оголошена. Будь-яке інше присвоєння чи зміна властивості призведе до виключення [Error](class.error.md)

**Приклад #5 Неправильна ініціалізація readonly-властивостей**

```php
<?php
class Test1 {
    public readonly string $prop;
}
$test1 = new Test1;
// Неправильная инициализация за пределами закрытой области.
$test1->prop = "foobar";
// Ошибка: не удаётся инициализировать readonly-свойство Test1::$prop из глобальной области
?>
```

> **Зауваження**
> 
> Вказівка ​​явного значення за умовчанням для readonly-властивостей не допускається, тому що readonly-властивість зі значенням за умовчанням, по суті, те саме, що і константа і тому не особливо корисно.
> 
> ```php
> <?php
> class Test {
>     // Ошибка: у readonly-свойства Test::$prop не может быть значения по умолчанию
>     public readonly int $prop = 42;
> }
> ?>
> ```

> **Зауваження**
> 
> Readonly-властивості не можуть бути знищені за допомогою [unset()](function.unset.md) після їхньої ініціалізації. Однак можна знищити readonly-властивість до ініціалізації з області, в якій було оголошено властивість.

Модифікації не обов'язково є простими присвоєннями, все наведене нижче також призведе до виключення [Error](class.error.md)

```php
<?php
class Test {
    public function __construct(
        public readonly int $i = 0,
        public readonly array $ary = [],
    ) {}
}
$test = new Test;
$test->i += 1;
$test->i++;
++$test->i;
$test->ary[] = 1;
$test->ary[0][] = 1;
$ref =& $test->i;
$test->i =& $ref;
byRef($test->i);
foreach ($test as &$prop);
?>
```

Однак реально-властивості не виключають внутрішньої мінливості. Об'єкти (або ресурси), що зберігаються в readonly-властивості, як і раніше, можуть бути змінені всередині:

```php
<?php
class Test {
    public function __construct(public readonly object $obj) {}
}
$test = new Test(new stdClass);
// Правильное внутреннее изменение.
$test->obj->foo = 1;
// Неправильное переопределение.
$test->obj = new stdClass;
?>
```
