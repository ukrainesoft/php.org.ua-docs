---
navigation:
  - language.oop5.final.md: « Ключевое слово final
  - language.oop5.object-comparison.md: Порівняння об'єктів »
  - index.md: PHP Manual
  - language.oop5.md: Класи та об'єкти
title: Клонування об'єктів
---
## Клонування об'єктів

Створення копії об'єкта з абсолютно ідентичними властивостями завжди є прийнятним варіантом. Хорошим прикладом необхідності копіювання конструкторів може стати ситуація, коли у вас є об'єкт, що представляє собою вікно GTK і містить ресурс-ідентифікатор цього вікна; Якщо ви створюєте копію цього об'єкта, вам може знадобитися, щоб копія об'єкта містила ресурс-ідентифікатор нового вікна. Іншим прикладом може стати ситуація, коли ваш об'єкт містить посилання на будь-який інший використовуваний об'єкт і, коли ви створюєте копію батьківського об'єкта, вам потрібно також створити новий екземпляр цього іншого об'єкта, так, щоб копія об'єкта-контейнера містила власний окремий екземпляр об'єкта, що міститься. .

Копія об'єкта створюється за допомогою ключового слова `clone` (який викликає метод [clone()](language.oop5.cloning.md#object.clone) об'єкта, якщо це можливо).

```
$copy_of_object = clone $object;
```

При клонуванні об'єкта PHP виконує поверхневу копію всіх властивостей об'єкта. Будь-які властивості, які є посиланнями на інші змінні, залишаться посиланнями.

```methodsynopsis
__clone(): void
```

Після завершення клонування, якщо метод [clone()](language.oop5.cloning.md#object.clone) визначено, то буде викликаний метод [clone()](language.oop5.cloning.md#object.clone) новоствореного об'єкта для можливої ​​зміни всіх необхідних властивостей.

**Приклад #1 Клонування об'єкта**

```php
<?php
class SubObject
{
    static $instances = 0;
    public $instance;

    public function __construct() {
        $this->instance = ++self::$instances;
    }

    public function __clone() {
        $this->instance = ++self::$instances;
    }
}

class MyCloneable
{
    public $object1;
    public $object2;

    function __clone()
    {
        // Принудительно клонируем this->object1, иначе
        // он будет указывать на один и тот же объект.
        $this->object1 = clone $this->object1;
    }
}

$obj = new MyCloneable();

$obj->object1 = new SubObject();
$obj->object2 = new SubObject();

$obj2 = clone $obj;


print("Оригинальный объект:\n");
print_r($obj);

print("Клонированный объект:\n");
print_r($obj2);

?>
```

Результат виконання цього прикладу:

```
Оригинальный объект:
MyCloneable Object
(
    [object1] => SubObject Object
        (
            [instance] => 1
        )

    [object2] => SubObject Object
        (
            [instance] => 2
        )

)
Клонированный объект:
MyCloneable Object
(
    [object1] => SubObject Object
        (
            [instance] => 3
        )

    [object2] => SubObject Object
        (
            [instance] => 2
        )

)
```

Можливо звертатися до властивостей/методів щойно схиленого об'єкта:

**Приклад #2 Доступ до об'єкта, що щойно схиляється.**

```php
<?php
$dateTime = new DateTime();
echo (clone $dateTime)->format('Y');
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
2016
```
