Коваріантність та контраваріантність

-   [« Сериализация объектов](language.oop5.serialization.html)
    
-   [Журнал изменений ООП »](language.oop5.changelog.html)
    
-   [PHP Manual](index.html)
    
-   [Классы и объекты](language.oop5.html)
    
-   Коваріантність та контраваріантність
    

## Коваріантність та контраваріантність

У PHP 7.2.0 було додано часткову контраваріантність шляхом усунення обмежень типу для параметрів у дочірньому методі. Починаючи з PHP 7.4.0, додано повну підтримку коваріантності та контраваріантності.

Коваріантність дозволяє дочірньому методу повертати більш конкретний тип, ніж тип значення його батьківського методу, що повертається. У той час як контраваріантність дозволяє типу параметра в дочірньому методі бути менш специфічним, ніж у батьківському.

Оголошення типу вважається більш конкретним у наступному випадку:

-   Вилучено [объединение типов](language.types.declarations.html#language.types.declarations.composite.union)
-   Додано [пересечение типов](language.types.declarations.html#language.types.declarations.composite.intersection)
-   Тип класу змінюється на тип дочірнього класу
-   [iterable](language.types.iterable.html) змінений на масив (array) або [Traversable](class.traversable.html)

В іншому випадку клас типу вважається менш конкретним.

### Коваріантність

Щоб проілюструвати, як працює підступність, створимо простий абстрактний батьківський клас Animal. Animal буде розширено за рахунок дочірніх класів Cat та Dog.

```php
<?php

abstract class Animal
{
    protected string $name;

    public function __construct(string $name)
    {
        $this->name = $name;
    }

    abstract public function speak();
}

class Dog extends Animal
{
    public function speak()
    {
        echo $this->name . " лает";
    }
}

class Cat extends Animal
{
    public function speak()
    {
        echo $this->name . " мяукает";
    }
}
```

Зверніть увагу, що на прикладі немає методів, які повертають значення. Буде додано декілька фабрик, які повертають новий об'єкт типу класу Animal, Cat або Dog.

```php
<?php

interface AnimalShelter
{
    public function adopt(string $name): Animal;
}

class CatShelter implements AnimalShelter
{
    public function adopt(string $name): Cat // Возвращаем класс Cat вместо Animal
    {
        return new Cat($name);
    }
}

class DogShelter implements AnimalShelter
{
    public function adopt(string $name): Dog // Возвращаем класс Dog вместо Animal
    {
        return new Dog($name);
    }
}

$kitty = (new CatShelter)->adopt("Рыжик");
$kitty->speak();
echo "\n";

$doggy = (new DogShelter)->adopt("Бобик");
$doggy->speak();
```

Результат виконання цього прикладу:

```
Рыжик мяукает
Бобик лает
```

### Контраваріантність

Продовжуючи попередній приклад, де ми використовували класи Animal, Cat і Dog, ми введемо нові класи Food і AnimalFood і додамо в абстрактний клас Animal новий метод eat(AnimalFood $food).

```php
<?php

class Food {}

class AnimalFood extends Food {}

abstract class Animal
{
    protected string $name;

    public function __construct(string $name)
    {
        $this->name = $name;
    }

    public function eat(AnimalFood $food)
    {
        echo $this->name . " ест " . get_class($food);
    }
}
```

Щоб побачити суть контраваріантності, ми перевизначимо метод eat класу Dog таким чином, щоб він міг приймати будь-який об'єкт класу Food. Клас Cat залишимо без змін.

```php
<?php

class Dog extends Animal
{
    public function eat(Food $food) {
        echo $this->name . " ест " . get_class($food);
    }
}
```

Наступний приклад покаже поведінку контраваріантності.

```php
<?php

$kitty = (new CatShelter)->adopt("Рыжик");
$catFood = new AnimalFood();
$kitty->eat($catFood);
echo "\n";

$doggy = (new DogShelter)->adopt("Бобик");
$banana = new Food();
$doggy->eat($banana);
```

Результат виконання цього прикладу:

```
Рыжик ест AnimalFood
Бобик ест Food
```

Але що станеться, якщо $kitty спробує з'їсти банан ($banana)?

```php
$kitty->eat($banana);
```

Результат виконання цього прикладу:

```
Fatal error: Uncaught TypeError: Argument 1 passed to Animal::eat() must be an instance of AnimalFood, instance of Food given
```