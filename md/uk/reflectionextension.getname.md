---
navigation:
  - reflectionextension.getinientries.md: '« ReflectionExtension::getINIEntries'
  - reflectionextension.getversion.md: 'ReflectionExtension::getVersion »'
  - index.md: PHP Manual
  - class.reflectionextension.md: ReflectionExtension
title: 'ReflectionExtension::getName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionExtension::getName

(PHP 5, PHP 7, PHP 8)

ReflectionExtension::getName — Отримання імені модуля

### Опис

```methodsynopsis
public ReflectionExtension::getName(): string
```

Отримує ім'я модуля.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ім'я модуль.

### Приклади

**Пример #1 Пример использования**ReflectionExtension::getName()\*\*\*\*

```php
<?php
$ext = new ReflectionExtension('mysqli');
var_dump($ext->getName());
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(6) "mysqli"
```

### Дивіться також

-   [ReflectionExtension::getClassNames()](reflectionextension.getclassnames.md) \- Отримання імен класів
