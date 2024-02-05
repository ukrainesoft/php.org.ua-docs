---
navigation:
  - sensitiveparametervalue.debuginfo.md: '« SensitiveParameterValue::\_\_debugInfo'
  - reserved.attributes.md: Зумовлені атрибути »
  - index.md: PHP Manual
  - class.sensitiveparametervalue.md: SensitiveParameterValue
title: 'SensitiveParameterValue::getValue'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SensitiveParameterValue::getValue

(PHP 8 >= 8.2.0)

SensitiveParameterValue::getValue — Повертає чутливе значення

### Опис

```methodsynopsis
public SensitiveParameterValue::getValue(): mixed
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Чутливе значення.

### Приклади

**Приклад #1 Приклад використання** SensitiveParameterValue::getValue()\*\*\*\*

```php
<?php
$s = new \SensitiveParameterValue('secret');

echo "Защищённое значение: ", $s->getValue(), "\n";
?>
```

Результат виконання наведеного прикладу:

```
Защищённое значение: secret
```
