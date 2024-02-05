---
navigation:
  - language.oop5.overloading.md: « Перевантаження
  - language.oop5.magic.md: Магічні методи »
  - index.md: PHP Manual
  - language.oop5.md: Класи та об'єкти
title: Ітератори об'єктів
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Ітератори об'єктів

PHP надає такий спосіб оголошення об'єктів, який дає можливість пройти за списком елементів даного об'єкта, наприклад, за допомогою оператора [foreach](control-structures.foreach.md). За умовчанням, у цьому обході (ітерації) братимуть участь усі [видимі](language.oop5.visibility.md) характеристики об'єкта.

**Приклад #1 Ітерація простого об'єкта**

```php
<?php
class MyClass
{
    public $var1 = 'значение 1';
    public $var2 = 'значение 2';
    public $var3 = 'значение 3';

    protected $protected = 'защищённая переменная';
    private   $private   = 'закрытая переменная';

    function iterateVisible() {
       echo "MyClass::iterateVisible:\n";
       foreach ($this as $key => $value) {
           print "$key => $value\n";
       }
    }
}

$class = new MyClass();

foreach($class as $key => $value) {
    print "$key => $value\n";
}
echo "\n";


$class->iterateVisible();

?>
```

Результат виконання наведеного прикладу:

```
var1 => значение 1
var2 => значение 2
var3 => значение 3

MyClass::iterateVisible:
var1 => значение 1
var2 => значение 2
var3 => значение 3
protected => защищённая переменная
private => закрытая переменная
```

Як показує результат, [foreach](control-structures.foreach.md) проітерував усі доступні та належать об'єкту [видимі](language.oop5.visibility.md)свойства.

### Дивіться також

-   [Генератори](language.generators.md)
-   [Iterator](class.iterator.md)
-   [IteratorAggregate](class.iteratoraggregate.md)
-   [Ітератори](spl.iterators.md)
