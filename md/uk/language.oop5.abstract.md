---
navigation:
  - language.oop5.static.md: « Ключове слово static
  - language.oop5.interfaces.md: Інтерфейси об'єктів »
  - index.md: PHP Manual
  - language.oop5.md: Класи та об'єкти
title: Абстрактні класи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Абстрактні класи

PHP підтримує визначення абстрактних класів та методів. На основі абстрактного класу не можна створювати об'єкти, і будь-який клас, що містить хоча б один абстрактний метод, має бути визначений як абстрактний. Методи, оголошені абстрактними, несуть, сутнісно, ​​лише описовий зміст і що неспроможні включати реалізацію.

При успадкування від абстрактного класу, всі методи, помічені абстрактними в батьківському класі, повинні бути визначені в дочірньому класі та дотримуватися звичайних правил [успадкування](language.oop5.inheritance.md) і [сумісності сигнатури](language.oop5.basic.md#language.oop.lsp)

**Приклад #1 Приклад абстрактного класу**

```php
<?php
abstract class AbstractClass
{
    // Данные методы должны быть определены в дочернем классе
    abstract protected function getValue();
    abstract protected function prefixValue($prefix);

    // Общий метод
    public function printOut() {
        print $this->getValue() . "\n";
    }
}

class ConcreteClass1 extends AbstractClass
{
    protected function getValue() {
        return "ConcreteClass1";
    }

    public function prefixValue($prefix) {
        return "{$prefix}ConcreteClass1";
    }
}

class ConcreteClass2 extends AbstractClass
{
    public function getValue() {
        return "ConcreteClass2";
    }

    public function prefixValue($prefix) {
        return "{$prefix}ConcreteClass2";
    }
}

$class1 = new ConcreteClass1;
$class1->printOut();
echo $class1->prefixValue('FOO_') ."\n";

$class2 = new ConcreteClass2;
$class2->printOut();
echo $class2->prefixValue('FOO_') ."\n";
?>
```

Результат виконання наведеного прикладу:

```
ConcreteClass1
FOO_ConcreteClass1
ConcreteClass2
FOO_ConcreteClass2
```

**Приклад #2 Приклад абстрактного класу**

```php
<?php
abstract class AbstractClass
{
    // Наш абстрактный метод требует только определить необходимые аргументы
    abstract protected function prefixName($name);

}

class ConcreteClass extends AbstractClass
{

    // Наш дочерний класс может определить необязательные аргументы, не указанные в объявлении родительского метода
    public function prefixName($name, $separator = ".") {
        if ($name == "Pacman") {
            $prefix = "Mr";
        } elseif ($name == "Pacwoman") {
            $prefix = "Mrs";
        } else {
            $prefix = "";
        }
        return "{$prefix}{$separator} {$name}";
    }
}

$class = new ConcreteClass;
echo $class->prefixName("Pacman"), "\n";
echo $class->prefixName("Pacwoman"), "\n";
?>
```

Результат виконання наведеного прикладу:

```
Mr. Pacman
Mrs. Pacwoman
```
