Повертає коротке, читанне, розбірливе рядкове уявлення змінної

-   [« Функции varrepresentation](ref.var-representation.html)
    
-   [Другие службы »](refs.remote.other.html)
    
-   [PHP Manual](index.html)
    
-   [Функции varrepresentation](ref.var-representation.html)
    
-   Повертає коротке, читанне, розбірливе рядкове уявлення змінної
    

# varrepresentation

(PECL varrepresentation >= 0.1.0)

varrepresentation - Повертає коротке, читане, розбірливе рядкове уявлення змінної

### Опис

```methodsynopsis
var_representation(mixed $value, int $flags = 0): string
```

**varrepresentation()** (модуль PECL varrepresentation) повертає рядок із структурованою інформацією про цю змінну. Функція схожа на [varexport()](function.var-export.html) з відмінностями у відступах, екрануванні рядків та уявленнях масиву.

### Список параметрів

`value`

Змінна, на яку створюється уявлення.

`flags`

Бітова маска, що складається з: **`VAR_REPRESENTATION_SINGLE_LINE`** **`VAR_REPRESENTATION_UNESCAPED`**. Поведінка цих констант описана на сторінці [константы varrepresentation](var-representation.constants.html)

### Значення, що повертаються

Повертає уявлення змінної.

### Приклади

**Приклад #1 Приклад використання **varrepresentation()****

```php
<?php
$a = [1, 2, ['key' => 'value']];
echo var_representation($a), "\n";
echo var_representation($a, VAR_REPRESENTATION_SINGLE_LINE), "\n";
?>
```

Результат виконання цього прикладу:

```
[
  1,
  2,
  [
    'key' => 'value',
  ],
]
[1, 2, ['key' => 'value']]
```

**Приклад #2 Екранування символів керування**

```php
<?php
echo var_representation("Content-Length: 123\r\n");
```

Результат виконання цього прикладу:

```
"Content-Length: 123\r\n"
```

**Приклад #3 Експорт **stdClass****

```php
<?php
$person = new stdClass;
$person->name = 'ElePHPant ElePHPantsdotter';
$person->website = 'https://php.net/elephpant.php';

echo var_representation($person);
```

Результат виконання цього прикладу:

```
(object) [
  'name' => 'ElePHPant ElePHPantsdotter',
  'website' => 'https://php.net/elephpant.php',
]
```

**Приклад #4 Експортування класів**

```php
<?php
class A { public $var; }
$a = new A;
$a->var = 5;
echo var_representation($a);
?>
```

Результат виконання цього прикладу:

```
\A::__set_state([
  'var' => 5,
])
```

**Приклад #5 Приклад використання [setstate()](language.oop5.magic.html#object.set-state)**

```php
<?php
class A
{
    public $var1;
    public $var2;

    public static function __set_state($an_array)
    {
        $obj = new A;
        $obj->var1 = $an_array['var1'];
        $obj->var2 = $an_array['var2'];
        return $obj;
    }
}

$a = new A;
$a->var1 = 5;
$a->var2 = 'foo';

eval('$b = ' . var_representation($a) . ';'); // $b = \A::__set_state([
                                              //   'var1' => 5,
                                              //   'var2' => 'foo',
                                              // ]);
var_dump($b);
?>
```

Результат виконання цього прикладу:

```
object(A)#2 (2) {
  ["var1"]=>
  int(5)
  ["var2"]=>
  string(3) "foo"
}
```

### Дивіться також

-   [varexport()](function.var-export.html) - Виводить або повертає інтерпретоване рядкове подання змінної