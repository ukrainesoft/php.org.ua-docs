---
navigation:
  - reflectionextension.getdependencies.md: '« ReflectionExtension::getDependencies'
  - reflectionextension.getinientries.md: 'ReflectionExtension::getINIEntries »'
  - index.md: PHP Manual
  - class.reflectionextension.md: ReflectionExtension
title: 'ReflectionExtension::getFunctions'
---
# ReflectionExtension::getFunctions

(PHP 5, PHP 7, PHP 8)

ReflectionExtension::getFunctions — Отримання функцій модуля

### Опис

```methodsynopsis
public ReflectionExtension::getFunctions(): array
```

Отримує список функцій, визначених у модулі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Асоціативний масив об'єктів [ReflectionFunction](class.reflectionfunction.md), у якому ключами є назви визначених у модулі функцій. Якщо функцій у модулі не визначено, буде повернено порожній масив.

### Приклади

**Приклад #1 Приклад використання **ReflectionExtension::getFunctions()****

```php
<?php
$dom = new ReflectionExtension('SimpleXML');

print_r($dom->getFunctions());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
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
```

### Дивіться також

-   [ReflectionExtension::getClasses()](reflectionextension.getclasses.md) - Повертає класи
-   [getextensionfuncs()](function.get-extension-funcs.md) - Повертає масив імен функцій модуля
