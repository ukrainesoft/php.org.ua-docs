- [« Closure::bindTo](closure.bindto.md)
- [Closure::fromCallable »](closure.fromcallable.md)

- [PHP Manual](index.md)
- [Closure](class.closure.md)
- Зв'язує та запускає замикання

# Closure::call

(PHP 7, PHP 8)

Closure::call — Зв'язує та запускає замикання

### Опис

public **Closure::call**(object `$newThis`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`...$args`):
[mixed](language.types.declarations.md#language.types.declarations.mixed)

Тимчасово пов'язує замикання з `newThis` і викликає його із заданими
параметрами.

### Список параметрів

`newThis`
Об'єкт (object) для прив'язки до замикання під час його виклику.

`args`
Нуль або більше параметрів, що передаються замиканню.

### Значення, що повертаються

Повертає значення замикання, що повертається

### Приклади

**Приклад #1 Приклад **Closure::call()****

`<?phpclass Value {   protected$value; public function __construct($value) {        $this->value = $value; }    public function getValue() {        return $this->value; }}$three== new Value(3);$four = new Value(4);$closure = function ($delta) { var_dump($this->getValue() + $delta); };$closure->call($three, 4);$closure->call($four, 4);?> `

Результат виконання цього прикладу:

int(7)
int(8)
