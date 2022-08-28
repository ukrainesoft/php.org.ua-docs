Приклади

-   [« Предопределённые константы](classobj.constants.html)
    
-   [Функции работы с классами и объектами »](ref.classobj.html)
    
-   [PHP Manual](index.html)
    
-   [Классы и объекты](book.classobj.html)
    
-   Приклади
    

# Приклади

У наведеному нижче прикладі ми спочатку визначимо базовий клас і клас його наслідуючий. Базовий клас описує овоч: чи їстівний він і якого кольору. Дочірній клас Spinach додає метод приготування овочів та перевірки, чи був він уже приготовлений.

**Приклад #1 Визначення класів**

Овочі

```php
<?php

class Vegetable {
    public $edible;

    public $color;

    public function __construct($edible, $color = "green")
    {
        $this->edible = $edible;
        $this->color = $color;
    }

    public function isEdible()
    {
        return $this->edible;
    }

    public function getColor()
    {
        return $this->color;
    }
}

?>
```

Шпинат

```php
<?php

class Spinach extends Vegetable {
    public $cooked = false;

    public function __construct()
    {
        parent::__construct(true, "green");
    }

    public function cook()
    {
        $this->cooked = true;
    }

    public function isCooked()
    {
        return $this->cooked;
    }
}

?>
```

Тепер ми створимо об'єкт кожного класу і роздрукуємо інформацію про них, включаючи порядок їх успадкування. Також ми оголосимо кілька функцій-утиліт, головним чином для зручного виведення результатів.

**Приклад #2 testscript.php**

```php
<?php

// зарегистрировать автозагрузчик для загрузки классов
spl_autoload_register();

function printProperties($obj)
{
    foreach (get_object_vars($obj) as $prop => $val) {
        echo "\t$prop = $val\n";
    }
}

function printMethods($obj)
{
    $arr = get_class_methods(get_class($obj));
    foreach ($arr as $method) {
        echo "\tфункция $method()\n";
    }
}

function objectBelongsTo($obj, $class)
{
    if (is_subclass_of($obj, $class)) {
        echo "Объект принадлежит к классу " . get_class($obj);
        echo ", подкласс $class\n";
    } else {
        echo "Объект не принадлежит к подклассу $class\n";
    }
}

// создание 2 объектов
$veggie = new Vegetable(true, "blue");
$leafy = new Spinach();

// вывод информации об объектах
echo "вегетарианский: CLASS " . get_class($veggie) . "\n";
echo "листовой: CLASS " . get_class($leafy);
echo ", PARENT " . get_parent_class($leafy) . "\n";

// показать вегетарианские свойства
echo "\nвегетарианский: Свойства\n";
printProperties($veggie);

// и листовые методы
echo "\nleafy: Методы\n";
printMethods($leafy);

echo "\nПроисхождение:\n";
objectBelongsTo($leafy, Spinach::class);
objectBelongsTo($leafy, Vegetable::class);

?>
```

Результат виконання даних прикладів:

```
вегетарианский: CLASS Vegetable
листовой: CLASS Spinach, PARENT Vegetable

вегетарианский: Свойства
        edible = 1
        color = blue

листовой: Методы
        function __construct()
        function cook()
        function isCooked()
        function isEdible()
        function getColor()

Происхождение:
Объект не принадлежит к подклассу Spinach
Объект принадлежит к классу Spinach, подкласс Vegetable
```

Важливо зауважити, що у наведеному вище прикладі об'єкт $leafy - екземпляр класу **Spinach**, який успадковує клас **Vegetable**