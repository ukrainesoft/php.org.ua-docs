- [«get_declared_traits](function.get-declared-traits.md)
- [get_object_vars »](function.get-object-vars.md)

- [PHP Manual](index.md)
- [Функції роботи з класами та об'єктами](ref.classobj.md)
- Повертає масив спотворених властивостей об'єкту

#get_mangled_object_vars

(PHP 7 \>= 7.4.0, PHP 8)

get_mangled_object_vars — Повертає масив спотворених властивостей об'єкту

### Опис

**get_mangled_object_vars**(object `$object`): array

Повертає масив (array), в елементах якого властивості
(Змінні-члени) цього об'єкта. Ключами будуть імена змінних-членів,
з деякими примітними винятками: до закритих полів класу
(private) попереду буде дописано ім'я класу; до захищених полів класу
(protected) попереду буде додано символ `*`. Ці додані значення
з обох боків також мають `NUL` байти. Неініціалізовані
[типізовані властивості](language.oop5.properties.md#language.oop5.properties.typed-properties)
автоматично відкидаються.

### Список параметрів

`object`
Примірник об'єкта.

### Значення, що повертаються

Повертає масив (array), що містить усі властивості об'єкта `object`,
незалежно від області видимості.

### Приклади

**Приклад #1 Приклад використання **get_mangled_object_vars()****

`<?phpclass A{    public $public = 1; protected $protected = 2; private $private = 3;}class B extends A{   private $private = 4;}$object = new B;$object->dynamic = 5;$object->{'6'}_=_6; object));class AO extends ArrayObject{    private $private = 1;}$arrayObject = new AO(['x' => 'y']);$arrayObject->dynamic = _2;var_dump ; `

Результат виконання цього прикладу:

array(6) {
["Bprivate"]=>
int(4)
["public"]=>
int(1)
["*protected"]=>
int(2)
["Aprivate"]=>
int(3)
["dynamic"]=>
int(5)
[6]=>
int(6)
}
array(2) {
["AOprivate"]=>
int(1)
["dynamic"]=>
int(2)
}

### Дивіться також

- [get_class_vars()](function.get-class-vars.md) - Повертає
оголошені за замовчуванням властивості класу
- [get_object_vars()](function.get-object-vars.md) - Повертає
властивості вказаного об'єкта
