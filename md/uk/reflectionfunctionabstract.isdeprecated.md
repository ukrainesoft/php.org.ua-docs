---
navigation:
  - reflectionfunctionabstract.isclosure.md: '« ReflectionFunctionAbstract::isClosure'
  - reflectionfunctionabstract.isgenerator.md: 'ReflectionFunctionAbstract::isGenerator »'
  - index.md: PHP Manual
  - class.reflectionfunctionabstract.md: ReflectionFunctionAbstract
title: 'ReflectionFunctionAbstract::isDeprecated'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionFunctionAbstract::isDeprecated

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

ReflectionFunctionAbstract::isDeprecated — Перевіряє, чи функція застаріла

### Опис

```methodsynopsis
public ReflectionFunctionAbstract::isDeprecated(): bool
```

Перевіряє, чи є функція застарілої.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**`true`**, если функция устарела,**`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання** ReflectionFunctionAbstract::isDeprecated()\*\*\*\*

```php
<?php
$rf = new ReflectionFunction('ereg');
var_dump($rf->isDeprecated());
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
```

### Дивіться також

-   [ReflectionFunctionAbstract::getDocComment()](reflectionfunctionabstract.getdoccomment.md) \- Отримує doc-коментар
