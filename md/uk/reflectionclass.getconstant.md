- [« ReflectionClass::getAttributes](reflectionclass.getattributes.md)
- [ReflectionClass::getConstants »](reflectionclass.getconstants.md)

- [PHP Manual](index.md)
- [ReflectionClass](class.reflectionclass.md)
- Повертає певну константу

# ReflectionClass::getConstant

(PHP 5, PHP 7, PHP 8)

ReflectionClass::getConstant — Повертає певну константу

### Опис

public **ReflectionClass::getConstant**(string `$name`):
[mixed](language.types.declarations.md#language.types.declarations.mixed)

Повертає певну константу.

### Список параметрів

`name`
Назва константи класу.

### Значення, що повертаються

Значення константи з ім'ям `name`. Повертає **`false`** якщо
константа відсутня у класі.

### Приклади

**Приклад #1 Приклад використання **ReflectionClass::getConstant()****

`<?phpclass Example {    const C1 = false; const C2 = 'I am a constant';}$reflection = new ReflectionClass('Example');var_dump($reflection->getConstant('C1'));var_dump($reflection->getConstant('C2')); var_dump($reflection->getConstant('C3'));?> `

Результат виконання цього прикладу:

bool(false)
string(15) "I am a constant"
bool(false)

### Дивіться також

- [ReflectionClass::getConstants()](reflectionclass.getconstants.md) -
Повертає константи
