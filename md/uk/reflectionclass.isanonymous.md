- [« ReflectionClass::isAbstract](reflectionclass.isabstract.md)
- [ReflectionClass::isCloneable »](reflectionclass.iscloneable.md)

- [PHP Manual](index.md)
- [ReflectionClass](class.reflectionclass.md)
- Перевіряє, чи є клас анонімним

# ReflectionClass::isAnonymous

(PHP 7, PHP 8)

ReflectionClass::isAnonymous — Перевіряє, чи є клас анонімним

### Опис

public **ReflectionClass::isAnonymous**(): bool

Перевіряє, чи анонімний клас ні.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад **ReflectionClass::isAnonymous()****

` <?phpclass TestClass {}$anonClass = new class {};$normalClass = new ReflectionClass('TestClass');$anonClass = new ReflectionClass($anonClass);var_dump($normalClass->is anonClass->isAnonymous());?> `

Результат виконання цього прикладу:

bool(false)
bool(true)

### Дивіться також

- [ReflectionClass::isFinal()](reflectionclass.isfinal.md) -
Перевіряє, чи є клас остаточним (final)
