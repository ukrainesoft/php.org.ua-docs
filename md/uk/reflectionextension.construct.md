---
navigation:
  - reflectionextension.clone.md: '« ReflectionExtension::clone'
  - reflectionextension.export.md: 'ReflectionExtension::export »'
  - index.md: PHP Manual
  - class.reflectionextension.md: ReflectionExtension
title: 'ReflectionExtension::construct'
---
# ReflectionExtension::construct

(PHP 5, PHP 7, PHP 8)

ReflectionExtension::construct — Створює об'єкт класу ReflectionExtension

### Опис

public **ReflectionExtension::construct**(string `$name`

Створює об'єкт (object) класу [ReflectionExtension](class.reflectionextension.md)

### Список параметрів

`name`

Ім'я модуль.

### Приклади

**Приклад #1 Приклад використання [ReflectionExtension](class.reflectionextension.md)**

```php
<?php
$ext = new ReflectionExtension('Reflection');

printf('Модуль: %s (версия: %s)', $ext->getName(), $ext->getVersion());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Модуль: Reflection (версия: $Revision$)
```

### Дивіться також

-   [ReflectionExtension::info()](reflectionextension.info.md) - Виведення інформації про модуль
-   [Конструктори](language.oop5.decon.md#language.oop5.decon.constructor)
