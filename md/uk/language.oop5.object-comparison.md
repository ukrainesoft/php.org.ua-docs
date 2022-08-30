Порівняння об'єктів

-   [« Клонирование объектов](language.oop5.cloning.html)
    
-   [Пізніше статичне зв'язування »](language.oop5.late-static-bindings.html)
    
-   [PHP Manual](index.html)
    
-   [Классы и объекты](language.oop5.html)
    
-   Порівняння об'єктів
    

## Порівняння об'єктів

При використанні оператора порівняння (`==`), властивості об'єктів просто порівнюються один з одним, а саме: два об'єкти рівні, якщо вони мають однакові атрибути та значення (значення порівнюються через `==`) і є екземплярами одного й того ж класу.

З іншого боку, при використанні оператора ідентичності (`===`), змінні, що містять об'єкти, вважаються ідентичними лише тоді, коли вони посилаються на той самий екземпляр одного й того ж класу.

Наступний приклад пояснить ці правила.

**Приклад #1 Приклад порівняння об'єктів**

```php
<?php
function bool2str($bool)
{
    return (string) $bool;
}

function compareObjects(&$o1, &$o2)
{
    echo 'o1 == o2 : ' . bool2str($o1 == $o2) . "\n";
    echo 'o1 != o2 : ' . bool2str($o1 != $o2) . "\n";
    echo 'o1 === o2 : ' . bool2str($o1 === $o2) . "\n";
    echo 'o1 !== o2 : ' . bool2str($o1 !== $o2) . "\n";
}

class Flag
{
    public $flag;

    function __construct($flag = true) {
        $this->flag = $flag;
    }
}

class OtherFlag
{
    public $flag;

    function __construct($flag = true) {
        $this->flag = $flag;
    }
}

$o = new Flag();
$p = new Flag();
$q = $o;
$r = new OtherFlag();

echo "Два экземпляра одного и того же класса\n";
compareObjects($o, $p);

echo "\nДве ссылки на один и тот же экземпляр\n";
compareObjects($o, $q);

echo "\nЭкземпляры двух разных классов\n";
compareObjects($o, $r);
?>
```

Результат виконання цього прикладу:

```
Два экземпляра одного и того же класса
o1 == o2 : TRUE
o1 != o2 : FALSE
o1 === o2 : FALSE
o1 !== o2 : TRUE

Две ссылки на один и тот же экземпляр
o1 == o2 : TRUE
o1 != o2 : FALSE
o1 === o2 : TRUE
o1 !== o2 : FALSE

Экземпляры двух разных классов
o1 == o2 : FALSE
o1 != o2 : TRUE
o1 === o2 : FALSE
o1 !== o2 : TRUE
```

> **Зауваження**
> 
> Модулі можуть визначати власні правила для порівняння своїх об'єктів (`==`