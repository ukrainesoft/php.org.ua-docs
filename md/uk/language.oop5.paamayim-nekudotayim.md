Оператор роздільної здатності видимості (::)

-   [« Наследование](language.oop5.inheritance.md)
    
-   [Ключевое слово static »](language.oop5.static.md)
    
-   [PHP Manual](index.md)
    
-   [Класи та об'єкти](language.oop5.md)
    
-   Оператор роздільної здатності видимості (::)
    

## Оператор роздільної здатності видимості (::)

Оператор дозволу області видимості (також званий "Paamayim Nekudotayim") або просто "подвійна двокрапка" - це лексема, що дозволяє звертатися до [статичним](language.oop5.static.md) властивостям, [константам](language.oop5.constants.md) та перевизначеним властивостям або методам класу.

При зверненні до цих елементів ззовні класу необхідно використовувати ім'я цього класу.

Можна звернутися до класу за допомогою змінної. Значення змінної не повинно бути ключовим словом (наприклад, `self` `parent` або `static`

"Paamayim Nekudotayim" на перший погляд може здатися дивним словосполученням для позначення подвійної двокрапки. Однак, під час створення Zend Engine версії 0.5 (який входив до PHP3), команда Zend обрала саме це позначення. Воно насправді означає "подвійне двокрапка" - на івриті!

**Приклад #1 Використання :: поза оголошенням класу**

```php
<?php
class MyClass {
    const CONST_VALUE = 'Значение константы';
}

$classname = 'MyClass';
echo $classname::CONST_VALUE;

echo MyClass::CONST_VALUE;
?>
```

Для звернення до властивостей і методів усередині класу використовуються ключові слова self, parent і static.

**Приклад #2 Використання :: всередині оголошення класу**

```php
<?php
class OtherClass extends MyClass
{
    public static $my_static = 'статическая переменная';

    public static function doubleColon() {
        echo parent::CONST_VALUE . "\n";
        echo self::$my_static . "\n";
    }
}

$classname = 'OtherClass';
$classname::doubleColon();

OtherClass::doubleColon();
?>
```

Коли дочірній клас перевизначає методи, оголошені в батьківському класі, PHP не здійснюватиме автоматичний виклик методів, що належать класу-батькові. Ця функціональність покладається на метод, що перевизначається в дочірньому класі. Це правило поширюється на [конструктори та деструктори](language.oop5.decon.md) [перевантажені](language.oop5.overloading.md) і ["магічні"](language.oop5.magic.md) методи.

**Приклад #3 Звернення до методу батьківського класу**

```php
<?php
class MyClass
{
    protected function myFunc() {
        echo "MyClass::myFunc()\n";
    }
}

class OtherClass extends MyClass
{
    // Переопределить родительское определение
    public function myFunc()
    {
        // Но всё ещё вызываем родительскую функцию
        parent::myFunc();
        echo "OtherClass::myFunc()\n";
    }
}

$class = new OtherClass();
$class->myFunc();
?>
```

Дивіться також [деякі приклади статичних викликів](language.oop5.basic.html#language.oop5.basic.class.this)