- [«Клонування об'єктів](language.oop5.cloning.md)
- [Пізнє статичне зв'язування »](language.oop5.late-static-bindings.md)

- [PHP Manual](index.md)
- [Класи та об'єкти](language.oop5.md)
- Порівняння об'єктів

## Порівняння об'єктів

При використанні оператора порівняння (`==`), властивості об'єктів просто
порівнюються один з одним, а саме: два об'єкти рівні, якщо вони мають
однакові атрибути та значення (значення порівнюються через `==`) та
є екземплярами одного й того ж класу.

З іншого боку, при використанні оператора ідентичності (`===`),
змінні, що містять об'єкти, вважаються ідентичними лише тоді,
коли вони посилаються на той самий екземпляр одного і того ж класу.

Наступний приклад пояснить ці правила.

**Приклад #1 Приклад порівняння об'єктів**

` <?phpfunction bool2str($bool){    return (string) $bool;}function compareObjects(&$o1, &$o2){   echo 'o1 == o2 : ' . bool2str($o1 ==$o2) . "
";   echo 'o1 != o2 : ' . bool2str($o1 != $o2) . "
";   echo 'o1 === o2 : ' . bool2str($o1 === $o2) . ""
";   echo 'o1 !== o2 : ' . bool2str($o1 !== $o2) . ""
";}class Flag{    public $flag;    function __construct($flag = true) {        $this->flag = $flag;    }}class OtherFlag{    public $flag;    function __construct($flag = true) {        $this-> flag = $flag;    }}$o = new Flag();$p = new Flag();$q = $o;$r = new OtherFlag();echo одного|
"; compareObjects($o, $p);echo "
Два посилання на один і той самий примірник
"; compareObjects($o, $q);echo "
Примірники двох різних класів
"; compareObjects($o, $r);?> `

Результат виконання цього прикладу:

Два екземпляри одного і того ж класу
o1 == o2 : TRUE
o1 != o2 : FALSE
o1 === o2 : FALSE
o1 !== o2 : TRUE

Два посилання на один і той самий екземпляр
o1 == o2 : TRUE
o1 != o2 : FALSE
o1 === o2 : TRUE
o1 !== o2 : FALSE

Примірники двох різних класів
o1 == o2 : FALSE
o1 != o2 : TRUE
o1 === o2 : FALSE
o1 !== o2 : TRUE

> **Примітка**:
>
> Модулі можуть визначати власні правила для порівняння своїх
> об'єктів (`==`).
