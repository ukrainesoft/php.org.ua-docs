---
navigation:
  - reflectionextension.clone.md: '« ReflectionExtension::\_\_clone'
  - reflectionextension.export.md: 'ReflectionExtension::export »'
  - index.md: PHP Manual
  - class.reflectionextension.md: ReflectionExtension
title: 'ReflectionExtension::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionExtension::\_\_construct

(PHP 5, PHP 7, PHP 8)

ReflectionExtension::\_\_construct — Створює об'єкт класу ReflectionExtension

### Опис

public**ReflectionExtension::\_\_construct**(string`$name`) .

Створює об'єкт (object) класу [ReflectionExtension](class.reflectionextension.md)

### Список параметрів

`name`

Ім'я модуль.

### Помилки

Викидає виняток [ReflectionException](class.reflectionexception.md)якщо модуль не існує.

### Приклади

**Пример #1 Пример использования[ReflectionExtension](class.reflectionextension.md)**

```php
<?php
$ext = new ReflectionExtension('Reflection');

printf('Модуль: %s (версия: %s)', $ext->getName(), $ext->getVersion());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Модуль: Reflection (версия: $Revision$)
```

### Дивіться також

-   [ReflectionExtension::info()](reflectionextension.info.md) \- Виведення інформації про модуль
-   [Конструктори](language.oop5.decon.md#language.oop5.decon.constructor)
