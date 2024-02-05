---
navigation:
  - migration83.incompatible.md: '« Зміни, що ламають зворотну сумісність'
  - migration83.other-changes.md: Інші зміни »
  - index.md: PHP Manual
  - migration83.md: Міграція з PHP 8.2.x на PHP 8.3.x
title: Застаріла функціональність
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Застаріла функціональність

### Ядро PHP

#### Оператори Increment/Decrement

Передача оператору[increment](language.operators.increment.md) `++`) порожніх, нечислових чи не літерно-числових рядків застаріла. До того ж інкрементування нечислових рядків застаріло м'яко. Поняття «м'яке старіння» означає, що діагностика рівня **`E_DEPRECATED`** виконуватись не буде, але потрібно відмовитися від застарілих правил у новому коді. Замість застарілого способу інкрементування необхідно викликати нову функцію [str\_increment()](function.str-increment.md)

Использование оператора[decrement](language.operators.increment.md) `--`) для порожніх чи нечислових рядків тепер неактуально.

#### Виклик функції get\_class()/get\_parent\_class() без аргументів

Виклик функцій [get\_class()](function.get-class.md) і [get\_parent\_class()](function.get-parent-class.md)без аргументов устарел.

### DBA

Виклик функції [dba\_fetch()](function.dba-fetch.md)с параметром`$dba` як третій аргумент застарів.

### FFI

Статичний виклик методу [FFI::cast()](ffi.cast.md) [FFI::new()](ffi.new.md) і [FFI::type()](ffi.type.md)устарел.

### Intl

Константа\*\*`U_MULTIPLE_DECIMAL_SEP*E*RATORS`\*\* застаріла, замість неї рекомендується використовувати константу **`U_MULTIPLE_DECIMAL_SEP*A*RATORS`**

Константа\*\*`NumberFormatter::TYPE_CURRENCY`\*\*устарела.

### LDAP

Виклик функції [ldap\_connect()](function.ldap-connect.md) з окремими параметрами `$hostname`и`$port`устарел.

### MBString

Передача негативного значення параметр `$width` функції [mb\_strimwidth()](function.mb-strimwidth.md)устарела.

### Phar

Виклик методу [Phar::setStub()](phar.setstub.md) з типом resource та параметром `$length` застарів. Такі дзвінки повинні бути замінені на: `$phar->setStub(stream_get_contents($resource));`

### Random

Варіант константи \*\*`MT_RAND_PHP`\*\*Mt19937 устарел.

### Reflection

Виклик методу [ReflectionProperty::setValue()](reflectionproperty.setvalue.md) лише з одним параметром застарів. Щоб встановити статичні властивості, передайте **`null`** як перший параметр.

### Стандартні функції

Функция[assert\_options()](function.assert-options.md)устарела.

Константи **`ASSERT_ACTIVE`** **`ASSERT_BAIL`** **`ASSERT_CALLBACK`** \*\*`ASSERT_EXCEPTION`**и**`ASSERT_WARNING`\*\*устарели.

INI-параметри `assert.*`устарели. Смотрите[зміни у роботі з INI-файлами](migration83.other-changes.md#migration83.other-changes.ini) для більш детальної інформації.

### SQLite3

Робота з винятками тепер краща, попередження будуть видалені в майбутньому. Виклик `SQLite3::enableExceptions(false)` у цій версії видасть попередження про старіння.

### Zip

Константа\*\*`ZipArchive::FL_RECOMPRESS`\*\* застаріла та буде видалена у майбутній версії libzip.
