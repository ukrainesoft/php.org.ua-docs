---
navigation:
  - reflectionfunction.isdisabled.md: '« ReflectionFunction::isDisabled'
  - class.reflectionfunctionabstract.md: ReflectionFunctionAbstract »
  - index.md: PHP Manual
  - class.reflectionfunction.md: ReflectionFunction
title: 'ReflectionFunction::\_\_function toString() { \[native code\] }'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionFunction::\_\_function toString() { \[native code\] }

(PHP 5, PHP 7, PHP 8)

ReflectionFunction::\_\_toString — Повертає строкове представлення об'єкта ReflectionFunction

### Опис

```methodsynopsis
public ReflectionFunction::__toString(): string
```

Отримує рядкове представлення функції, її параметрів та значень, що повертаються.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Метод повертає рядок.

### Приклади

**Приклад #1 Приклад використання** ReflectionFunction::\_\_toString()\*\*\*\*

```php
<?php
function title($title, $name)
{
    return sprintf("%s. %s\r\n", $title, $name);
}

echo new ReflectionFunction('title');
?>
```

Висновок наведеного прикладу буде схожим на:

```
Function [ <user> function title ] {
  @@ Command line code 1 - 1

  - Parameters [2] {
    Parameter #0 [ <required> $title ]
    Parameter #1 [ <required> $name ]
  }
}
```

### Дивіться також

-   [ReflectionFunction::export()](reflectionfunction.export.md) \- Експортує функції
-   [\_\_toString()](language.oop5.magic.md#object.tostring)
