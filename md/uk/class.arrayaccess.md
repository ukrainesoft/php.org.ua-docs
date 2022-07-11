- [« Throwable::\_\_toString](throwable.tostring.md)
- [ArrayAccess::offsetExists »](arrayaccess.offsetexists.md)

- [PHP Manual](index.md)
- [Вбудовані інтерфейси та класи](reserved.interfaces.md)
- Інтерфейс ArrayAccess

# Інтерфейс ArrayAccess

(PHP 5, PHP 7, PHP 8)

## Вступ

Інтерфейс забезпечує доступ до об'єктів як масивів.

## Огляд інтерфейсів

interface **ArrayAccess** {

/\* Методи \*/

public
[offsetExists](arrayaccess.offsetexists.md)([mixed](language.types.declarations.md#language.types.declarations.mixed)
`$offset`): bool

public
[offsetGet](arrayaccess.offsetget.md)([mixed](language.types.declarations.md#language.types.declarations.mixed)
`$offset`):
[mixed](language.types.declarations.md#language.types.declarations.mixed)

public
[offsetSet](arrayaccess.offsetset.md)([mixed](language.types.declarations.md#language.types.declarations.mixed)
`$offset`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$value`): void

public
[offsetUnset](arrayaccess.offsetunset.md)([mixed](language.types.declarations.md#language.types.declarations.mixed)
`$offset`): void

}

**Приклад #1 Основи використання**

` <?phpclass Obj implements ArrayAccess {    private $container = array(); public function __construct() {        $this->container = array(            "one"   => 1,            "two"   => 2,            "three" => 3,        ); }   public function offsetSet($offset, $value) {       if (is_null($offset)) {             $$$| } else {             $this->container[$offset] = $value; }    }    public function offsetExists($offset) {       return isset($this->container[$offset]); }    public function offsetUnset($offset) {        unset($this->container[$offset]); }    public function offsetGet($offset) {        return isset($this->container[$offset]) ? $this->container[$offset] : null; }}$obj = new Obj;var_dump(isset($obj["two"]));var_dump($obj["two"]);unset($obj["two"]);var_dump(isset($obj ["two"]));$obj["two"] = "A value";var_dump($obj["two"]);$obj[] = 'Append 1';$obj[] = 'Append 2 ';$obj[] = 'Append 3';print_r($obj);?> `

Результатом виконання цього прикладу буде щось подібне:

bool(true)
int(2)
bool(false)
string(7) "A value"
obj Object
(
[container:obj:private] => Array
(
[one] => 1
[three] => 3
[two] => A value
[0] => Append 1
[1] => Append 2
[2] => Append 3
)

)

## Зміст
 - [ArrayAccess::offsetExists](arrayaccess.offsetexists.md) -
Визначає, чи існує задане усунення (ключ)
- [ArrayAccess::offsetGet](arrayaccess.offsetget.md) — Повертає
задане зміщення (ключ)
- [ArrayAccess::offsetSet](arrayaccess.offsetset.md) - Надає
значення заданого зміщення
- [ArrayAccess::offsetUnset](arrayaccess.offsetunset.md) — Видаляє
зміщення
