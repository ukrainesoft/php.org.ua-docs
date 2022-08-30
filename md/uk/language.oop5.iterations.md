Ітератори об'єктів

-   [« Перегрузка](language.oop5.overloading.html)
    
-   [Магічні методи »](language.oop5.magic.html)
    
-   [PHP Manual](index.html)
    
-   [Классы и объекты](language.oop5.html)
    
-   Ітератори об'єктів
    

## Ітератори об'єктів

PHP надає такий спосіб оголошення об'єктів, який дає можливість пройти за списком елементів даного об'єкта, наприклад, за допомогою оператора [foreach](control-structures.foreach.html). За умовчанням, у цьому обході (ітерації) братимуть участь усі [видимі](language.oop5.visibility.html) характеристики об'єкта.

**Приклад #1 Ітерація простого об'єкта**

```php
<?php
class MyClass
{
    public $var1 = 'значение 1';
    public $var2 = 'значение 2';
    public $var3 = 'значение 3';

    protected $protected = 'защищённая переменная';
    private   $private   = 'закрытая переменная';

    function iterateVisible() {
       echo "MyClass::iterateVisible:\n";
       foreach ($this as $key => $value) {
           print "$key => $value\n";
       }
    }
}

$class = new MyClass();

foreach($class as $key => $value) {
    print "$key => $value\n";
}
echo "\n";


$class->iterateVisible();

?>
```

Результат виконання цього прикладу:

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

Як показує результат, [foreach](control-structures.foreach.html) проітерував усі доступні та належать об'єкту [видимі](language.oop5.visibility.html) властивості.

### Дивіться також

-   [Генераторы](language.generators.html)
-   [Iterator](class.iterator.html)
-   [IteratorAggregate](class.iteratoraggregate.html)
-   [Ітератори](spl.iterators.html)