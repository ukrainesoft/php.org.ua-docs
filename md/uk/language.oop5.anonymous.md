---
navigation:
  - language.oop5.traits.md: « Трейти
  - language.oop5.overloading.md: Перегрузка »
  - index.md: PHP Manual
  - language.oop5.md: Класи та об'єкти
title: Анонімні класи
---
## Анонімні класи

Анонімні класи корисні, коли потрібно створити прості одноразові об'єкти.

```php
<?php

// Использование явного класса
class Logger
{
    public function log($msg)
    {
        echo $msg;
    }
}

$util->setLogger(new Logger());

// Использование анонимного класса
$util->setLogger(new class {
    public function log($msg)
    {
        echo $msg;
    }
});
```

Вони можуть передавати аргументи в конструктори, розширювати інші класи, реалізовувати інтерфейси та використовувати трейти як звичайний клас:

```php
<?php

class SomeClass {}
interface SomeInterface {}
trait SomeTrait {}

var_dump(new class(10) extends SomeClass implements SomeInterface {
    private $num;

    public function __construct($num)
    {
        $this->num = $num;
    }

    use SomeTrait;
});
```

Результат виконання цього прикладу:

```
object(class@anonymous)#1 (1) {
  ["Command line code0x104c5b612":"class@anonymous":private]=>
  int(10)
}
```

Вкладення анонімного класу в інший клас не дає йому доступу до закритих або захищених методів і властивостей цього зовнішнього класу. Щоб використовувати захищені властивості і методи зовнішнього класу, анонімний клас може розширити зовнішній клас. Щоб використовувати закриті властивості зовнішнього класу в анонімному класі, їх потрібно передати до конструктора:

```php
<?php

class Outer
{
    private $prop = 1;
    protected $prop2 = 2;

    protected function func1()
    {
        return 3;
    }

    public function func2()
    {
        return new class($this->prop) extends Outer {
            private $prop3;

            public function __construct($prop)
            {
                $this->prop3 = $prop;
            }

            public function func3()
            {
                return $this->prop2 + $this->prop3 + $this->func1();
            }
        };
    }
}

echo (new Outer)->func2()->func3();
```

Результат виконання цього прикладу:

```
6
```

Всі об'єкти, створені тим самим оголошенням анонімного класу, є екземплярами цього самого класу.

```php
<?php
function anonymous_class()
{
    return new class {};
}

if (get_class(anonymous_class()) === get_class(anonymous_class())) {
    echo 'Тот же класс';
} else {
    echo 'Другой класс';
}
```

Результат виконання цього прикладу:

```
Тот же класс
```

> **Зауваження**
> 
> Зверніть увагу, що анонімним класам надаються імена двигуном PHP, як показано в прикладі нижче. Це слід розглядати як особливість реалізації, яку слід покладатися.
> 
> ```php
> <?php
> echo get_class(new class {});
> ```
> 
> Результатом виконання цього прикладу буде щось подібне:
> 
> ```
> class@anonymous/in/oNi1A0x7f8636ad2021
> ```
