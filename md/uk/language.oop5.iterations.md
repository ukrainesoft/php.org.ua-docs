- [« Перевантаження](language.oop5.overloading.md)
- [Магічні методи»](language.oop5.magic.md)

- [PHP Manual](index.md)
- [Класи та об'єкти](language.oop5.md)
- Ітератори об'єктів

## Ітератори об'єктів

PHP надає такий спосіб оголошення об'єктів, який дає
можливість пройти по списку елементів даного об'єкта, наприклад,
за допомогою оператора [foreach](control-structures.foreach.md). за
замовчуванням, у цьому обході (ітерації) братимуть участь всі
[видимые](language.oop5.visibility.md) властивості об'єкта.

**Приклад #1 Ітерація простого об'єкта**

`<?phpclass MyClass{    public $var1 = 'значення 1'; public $var2 = 'значення 2'; public $var3 = 'значення 3'; protected $protected = 'захищена змінна'; private   $private   = 'закрита змінна'; function iterateVisible() {       echo "MyClass::iterateVisible:
";       foreach ($this as $key => $value) {            print "$key => $value
";       }    }}$class = new MyClass();foreach($class as $key => $value) {    print "$key => $value
";}echo "
";$class->iterateVisible();?> `

Результат виконання цього прикладу:

var1 => значення 1
var2 => значення 2
var3 => значення 3

MyClass::iterateVisible:
var1 => значення 1
var2 => значення 2
var3 => значення 3
protected => захищена змінна
private => закрита змінна

Як показує результат, [foreach](control-structures.foreach.md)
проітерував усі доступні та належать об'єкту
[видимі](language.oop5.visibility.md) властивості.

### Дивіться також

- [Генератори](language.generators.md)
- [Iterator](class.iterator.md)
- [IteratorAggregate](class.iteratoraggregate.md)
- [Ітератори](spl.iterators.md)
