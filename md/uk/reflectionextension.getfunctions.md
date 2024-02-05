---
navigation:
  - reflectionextension.getdependencies.md: '« ReflectionExtension::getDependencies'
  - reflectionextension.getinientries.md: 'ReflectionExtension::getINIEntries »'
  - index.md: PHP Manual
  - class.reflectionextension.md: ReflectionExtension
title: 'ReflectionExtension::getFunctions'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

**Пример #1 Пример использования**ReflectionExtension::getFunctions()\*\*\*\*

```php
<?php
$dom = new ReflectionExtension('SimpleXML');

print_r($dom->getFunctions());
?>
```

Висновок наведеного прикладу буде схожим на:

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

-   [ReflectionExtension::getClasses()](reflectionextension.getclasses.md) \- Повертає класи
-   [get\_extension\_funcs()](function.get-extension-funcs.md) \- Повертає масив імен функцій модуля
