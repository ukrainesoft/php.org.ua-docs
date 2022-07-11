- [« ReflectionExtension::getDependencies](reflectionextension.getdependencies.md)
- [ReflectionExtension::getINIEntries »](reflectionextension.getinientries.md)

- [PHP Manual](index.md)
- [ReflectionExtension](class.reflectionextension.md)
- Отримання функцій модуля

# ReflectionExtension::getFunctions

(PHP 5, PHP 7, PHP 8)

ReflectionExtension::getFunctions — Отримання функцій модуля

### Опис

public **ReflectionExtension::getFunctions**(): array

Отримує список функцій, визначених у модулі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Асоціативний масив об'єктів
[ReflectionFunction](class.reflectionfunction.md), у якому ключами
є назви визначених у модулі функцій. Якщо функцій у модулі
не визначено, чи буде повернутий порожній масив.

### Приклади

**Приклад #1 Приклад використання
**ReflectionExtension::getFunctions()****

` <?php$dom = new ReflectionExtension('SimpleXML');print_r($dom->getFunctions());?> `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[simplexml_load_file] => ReflectionFunction Object
(
[name] => simplexml_load_file
)

[simplexml_load_string] => ReflectionFunction Object
(
[name] => simplexml_load_string
)

[simplexml_import_dom] => ReflectionFunction Object
(
[name] => simplexml_import_dom
)

)

### Дивіться також

- [ReflectionExtension::getClasses()](reflectionextension.getclasses.md) -
Повертає класи
- [get_extension_funcs()](function.get-extension-funcs.md) -
Повертає масив імен функцій модуля
