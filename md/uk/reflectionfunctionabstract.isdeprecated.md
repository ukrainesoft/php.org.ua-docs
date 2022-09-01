---
navigation:
  - reflectionfunctionabstract.isclosure.md: '« ReflectionFunctionAbstract::isClosure'
  - reflectionfunctionabstract.isgenerator.md: 'ReflectionFunctionAbstract::isGenerator »'
  - index.md: PHP Manual
  - class.reflectionfunctionabstract.md: ReflectionFunctionAbstract
title: 'ReflectionFunctionAbstract::isDeprecated'
---
# ReflectionFunctionAbstract::isDeprecated

(PHP 5> = 5.2.0, PHP 7, PHP 8)

ReflectionFunctionAbstract::isDeprecated — Перевіряє, чи функція застаріла

### Опис

```methodsynopsis
public ReflectionFunctionAbstract::isDeprecated(): bool
```

Перевіряє, чи функція застаріла.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

\*\*`true`\*\*якщо функція застаріла, **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **ReflectionFunctionAbstract::isDeprecated()****

```php
<?php
$rf = new ReflectionFunction('ereg');
var_dump($rf->isDeprecated());
?>
```

Результат виконання цього прикладу:

```
bool(true)
```

### Дивіться також

-   [ReflectionFunctionAbstract::getDocComment()](reflectionfunctionabstract.getdoccomment.md) - Отримує doc-коментар
