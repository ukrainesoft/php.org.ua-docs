---
navigation:
  - sensitiveparametervalue.construct.md: '« SensitiveParameterValue::\_\_construct'
  - sensitiveparametervalue.getvalue.md: 'SensitiveParameterValue::getValue »'
  - index.md: PHP Manual
  - class.sensitiveparametervalue.md: SensitiveParameterValue
title: 'SensitiveParameterValue::\_\_debugInfo'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SensitiveParameterValue::\_\_debugInfo

(PHP 8 >= 8.2.0)

SensitiveParameterValue::\_\_debugInfo — Захист чутливих значень від випадкової дії

### Опис

```methodsynopsis
public SensitiveParameterValue::__debugInfo(): array
```

Повертає порожній масив (array) для захисту чутливого значення від випадкового розкриття під час використання функції [var\_dump()](function.var-dump.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Порожній масив (Array).

### Приклади

**Приклад #1 Передача об'єкту [SensitiveParameterValue](class.sensitiveparametervalue.md) у функцію [var\_dump()](function.var-dump.md)**

```php
<?php
$s = new \SensitiveParameterValue('secret');

var_dump($s);
?>
```

Результат виконання наведеного прикладу:

```
object(SensitiveParameterValue)#1 (0) {
}
```
