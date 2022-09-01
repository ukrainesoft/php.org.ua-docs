---
navigation:
  - reflectionextension.clone.html: '« ReflectionExtension::clone'
  - reflectionextension.export.html: 'ReflectionExtension::export »'
  - index.html: PHP Manual
  - class.reflectionextension.html: ReflectionExtension
title: 'ReflectionExtension::construct'
---
# ReflectionExtension::construct

(PHP 5, PHP 7, PHP 8)

ReflectionExtension::construct — Створює об'єкт класу ReflectionExtension

### Опис

public **ReflectionExtension::construct**(string `$name`

Створює об'єкт (object) класу [ReflectionExtension](class.reflectionextension.html)

### Список параметрів

`name`

Ім'я модуль.

### Приклади

**Приклад #1 Приклад використання [ReflectionExtension](class.reflectionextension.html)**

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

-   [ReflectionExtension::info()](reflectionextension.info.html) - Виведення інформації про модуль
-   [Конструктори](language.oop5.decon.html#language.oop5.decon.constructor)
