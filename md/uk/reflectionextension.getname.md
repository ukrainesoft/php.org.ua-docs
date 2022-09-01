---
navigation:
  - reflectionextension.getinientries.html: '« ReflectionExtension::getINIEntries'
  - reflectionextension.getversion.html: 'ReflectionExtension::getVersion »'
  - index.html: PHP Manual
  - class.reflectionextension.html: ReflectionExtension
title: 'ReflectionExtension::getName'
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

**Приклад #1 Приклад використання **ReflectionExtension::getName()****

```php
<?php
$ext = new ReflectionExtension('mysqli');
var_dump($ext->getName());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(6) "mysqli"
```

### Дивіться також

-   [ReflectionExtension::getClassNames()](reflectionextension.getclassnames.html) - Отримання імен класів
