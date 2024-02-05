---
navigation:
  - language.oop5.inheritance.md: « Спадкування
  - language.oop5.static.md: Ключове слово static »
  - index.md: PHP Manual
  - language.oop5.md: Класи та об'єкти
title: 'Оператор роздільної здатності видимості (::)'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Оператор роздільної здатності видимості (::)

Оператор роздільної здатності області видимості (названий також Paamayim Nekudotayim) або, простіше кажучи, «подвійна двокрапка» - це лексема, що дозволяє звертатися до [константі](language.oop5.constants.md) [статичному](language.oop5.static.md)свойству или[статичному](language.oop5.static.md) методу класу чи одному з його батьків. Крім цього, статичні властивості або методи дозволено перевизначати через [пізніше статичне зв'язування](language.oop5.late-static-bindings.md)

При зверненні до цих елементів ззовні класу вказують ім'я класу.

Можна звертатись до класу через змінну. Значення змінної не повинно бути ключовим словом (наприклад, `self` `parent`или`static`

Paamayim Nekudotayim тільки спочатку здається дивним словосполученням для позначення подвійного двокрапки. Однак, поки писав двигун Zend Engine версії 0.5 (який входив в PHP3), команда Zend вирішила так і назвати його. Взагалі-то воно й означає «подвійну двокрапку» — на івриті!

**Приклад #1 Використання :: поза оголошенням класу**

```php
<?php
class MyClass {
    const CONST_VALUE = 'Значение константы';
}

$classname = 'MyClass';
echo $classname::CONST_VALUE;

echo MyClass::CONST_VALUE;
?>
```

До властивостей і методів усередині класу звертаються через ключові слова self, parent і static.

**Приклад #2 Використання :: всередині оголошення класу**

```php
<?php
class OtherClass extends MyClass
{
    public static $my_static = 'статическая переменная';

    public static function doubleColon() {
        echo parent::CONST_VALUE . "\n";
        echo self::$my_static . "\n";
    }
}

$classname = 'OtherClass';
$classname::doubleColon();

OtherClass::doubleColon();
?>
```

Коли дочірній клас перевизначає методи батьківського класу, PHP автоматично не викликає методи батьківського класу. Чи буде викликано метод батьківського класу, залежить від дочірнього. Це правило також поширюється на [конструктори та деструктори](language.oop5.decon.md) [перевантажені](language.oop5.overloading.md)и «[магічні](language.oop5.magic.md)методи.

**Приклад #3 Звернення до методу батьківського класу**

```php
<?php
class MyClass
{
    protected function myFunc() {
        echo "MyClass::myFunc()\n";
    }
}

class OtherClass extends MyClass
{
    // Переопределить родительское определение
    public function myFunc()
    {
        // Но всё ещё вызываем родительскую функцию
        parent::myFunc();
        echo "OtherClass::myFunc()\n";
    }
}

$class = new OtherClass();
$class->myFunc();
?>
```

Смотрите также[деякі приклади статичних викликів](language.oop5.basic.md#language.oop5.basic.class.this)
