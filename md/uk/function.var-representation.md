- [« Функції var_representation](ref.var-representation.md)
- [Інші служби »](refs.remote.other.md)

- [PHP Manual](index.md)
- [Функції var_representation](ref.var-representation.md)
- Повертає коротку, читаючу, розбірливу рядкову виставу
змінної

# var_representation

(PECL var_representation \>= 0.1.0)

var_representation - Повертає коротке, читане, розбірливе
рядкове подання змінної

### Опис

**var_representation**([mixed](language.types.declarations.md#language.types.declarations.mixed)
`$value`, int `$flags` = 0): string

**var_representation()** (модуль PECL var_representation) повертає
рядок зі структурованою інформацією про цю змінну. Функція
схожа на [var_export()](function.var-export.md) з відмінностями у
відступах, екрануванні рядків та уявленнях масиву.

### Список параметрів

`value`
Змінна, на яку створюється уявлення.

`flags`
Бітова маска, що складається з: **`VAR_REPRESENTATION_SINGLE_LINE`**,
**`VAR_REPRESENTATION_UNESCAPED`**. Поведінка цих констант описано на
сторінці [константи var_representation](var-representation.constants.md).

### Значення, що повертаються

Повертає уявлення змінної.

### Приклади

**Приклад #1 Приклад використання **var_representation()****

` <?php$a = [1, 2, ['key' => 'value']];echo var_representation($a), "
";echo var_representation($a, VAR_REPRESENTATION_SINGLE_LINE), "
";?> `

Результат виконання цього прикладу:

[
1,
2,
[
'key' => 'value',
],
]
[1, 2, ['key' => 'value']]

**Приклад #2 Екранування символів керування**

`<?phpecho var_representation("Content-Length: 123
");

Результат виконання цього прикладу:

"Content-Length: 123
"

**Приклад #3 Експорт **stdClass****

` <?php$person = new stdClass;$person->name = 'ElePHPant ElePHPantsdotter';$person->website = 'https://php.net/elephpant.php';echo var_representation($person); `

Результат виконання цього прикладу:

(object) [
'name' => 'ElePHPant ElePHPantsdotter',
'website' => 'https://php.net/elephpant.php',
]

**Приклад #4 Експортування класів**

`<?phpclass A { public $var; }$a = new A;$a->var = 5;echo var_representation($a);?> `

Результат виконання цього прикладу:

\A::__set_state([
'var' => 5,
])

**Приклад #5 Приклад використання
[\_\_set_state()](language.oop5.magic.md#object.set-state)**

`<?phpclass A{    public $var1; public $var2; public static function __set_state($an_array)    {        $obj = new A; $obj->var1 = $an_array['var1']; $obj->var2 = $an_array['var2']; return $obj; }}$a = new A;$a->var1 = 5;$a->var2 = 'foo';eval('$b = ' . var_representation($a) . ';'); // $b = \A::__set_state([                                              //   'var1' => 5,                                              //   'var2' => 'foo',                                              // ]);var_dump($b);?> `

Результат виконання цього прикладу:

object(A)#2 (2) {
["var1"]=>
int(5)
["var2"]=>
string(3) "foo"
}

### Дивіться також

- [var_export()](function.var-export.md) - Виводить або повертає
інтерпретоване рядкове подання змінної
