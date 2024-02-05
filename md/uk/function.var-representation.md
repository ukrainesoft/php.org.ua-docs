---
navigation:
  - ref.var-representation.md: « Функції var\_representation
  - refs.remote.other.md: Інші служби »
  - index.md: PHP Manual
  - ref.var-representation.md: Функції var\_representation
title: var\_representation
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# var\_representation

(PECL var\_representation >= 0.1.0)

var\_representation - Повертає коротке, читане, розбірливе рядкове уявлення змінної

### Опис

```methodsynopsis
var_representation(mixed $value, int $flags = 0): string
```

**var\_representation()**(модуль PECL var\_representation) повертає рядок із структурованою інформацією про цю змінну. Функція схожа на [var\_export()](function.var-export.md) з відмінностями у відступах, екрануванні рядків та уявленнях масиву.

### Список параметрів

`value`

Змінна, на яку створюється уявлення.

`flags`

Бітова маска, що складається з: **`VAR_REPRESENTATION_SINGLE_LINE`** **`VAR_REPRESENTATION_UNESCAPED`**. Поведінка цих констант описана на сторінці [константи var\_representation](var-representation.constants.md)

### Значення, що повертаються

Повертає уявлення змінної.

### Приклади

**Пример #1 Пример использования**var\_representation()\*\*\*\*

```php
<?php
$a = [1, 2, ['key' => 'value']];
echo var_representation($a), "\n";
echo var_representation($a, VAR_REPRESENTATION_SINGLE_LINE), "\n";
?>
```

Результат виконання наведеного прикладу:

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
echo var_representation("Content-Length: 123\r\n");
```

Результат виконання наведеного прикладу:

```
"Content-Length: 123\r\n"
```

**Приклад #3 Експорт [stdClass](class.stdclass.md)**

```php
<?php
$person = new stdClass;
$person->name = 'ElePHPant ElePHPantsdotter';
$person->website = 'https://php.net/elephpant.php';

echo var_representation($person);
```

Результат виконання наведеного прикладу:

```
(object) [
  'name' => 'ElePHPant ElePHPantsdotter',
  'website' => 'https://php.net/elephpant.php',
]
```

**Приклад #4 Експортування класів**

```php
<?php
class A { public $var; }
$a = new A;
$a->var = 5;
echo var_representation($a);
?>
```

Результат виконання наведеного прикладу:

```
\A::__set_state([
  'var' => 5,
])
```

**Пример #5 Пример использования[\_\_set\_state()](language.oop5.magic.md#object.set-state)**

```php
<?php
class A
{
    public $var1;
    public $var2;

    public static function __set_state($an_array)
    {
        $obj = new A;
        $obj->var1 = $an_array['var1'];
        $obj->var2 = $an_array['var2'];
        return $obj;
    }
}

$a = new A;
$a->var1 = 5;
$a->var2 = 'foo';

eval('$b = ' . var_representation($a) . ';'); // $b = \A::__set_state([
                                              //   'var1' => 5,
                                              //   'var2' => 'foo',
                                              // ]);
var_dump($b);
?>
```

Результат виконання наведеного прикладу:

```
object(A)#2 (2) {
  ["var1"]=>
  int(5)
  ["var2"]=>
  string(3) "foo"
}
```

### Дивіться також

-   [var\_export()](function.var-export.md) \- Виводить або повертає інтерпретоване рядкове подання змінної
