---
navigation:
  - filter.examples.md: « Приклади
  - filter.examples.sanitization.md: Очищення (нормалізація) »
  - index.md: PHP Manual
  - filter.examples.md: Приклади
title: Перевірка (валідація)
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Перевірка (валідація)

**Пример #1 Валидация e-mail адреса, используя функцию[filter\_var()](function.filter-var.md)**

```php
<?php
$email_a = 'joe@example.com';
$email_b = 'bogus';

if (filter_var($email_a, FILTER_VALIDATE_EMAIL)) {
    echo "E-mail адрес '$email_a' указан верно.\n";
}
if (filter_var($email_b, FILTER_VALIDATE_EMAIL)) {
    echo "E-mail адрес '$email_b' указан верно.\n";
} else {
    echo "E-mail адрес '$email_b' указан неверно.\n";
}
?>
```

Результат виконання наведеного прикладу:

```
E-mail адрес 'joe@example.com' указан верно.
E-mail адрес 'bogus' указан неверно.
```

**Пример #2 Валидация IP-адреса, используя функцию[filter\_var()](function.filter-var.md)**

```php
<?php
$ip_a = '127.0.0.1';
$ip_b = '42.42';

if (filter_var($ip_a, FILTER_VALIDATE_IP)) {
    echo "IP-адрес '$ip_a' указан верно.";
}
if (filter_var($ip_b, FILTER_VALIDATE_IP)) {
    echo "IP-адрес '$ip_b' указан верно.";
}
?>
```

Результат виконання наведеного прикладу:

```
Адрес '127.0.0.1' указан верно.
```

**Приклад #3 Додаткові параметри функції [filter\_var()](function.filter-var.md)**

```php
<?php
$int_a = '1';
$int_b = '-1';
$int_c = '4';
$options = array(
    'options' => array(
        'min_range' => 0,
        'max_range' => 3,
    )
);
if (filter_var($int_a, FILTER_VALIDATE_INT, $options) !== FALSE) {
    echo "Число A '$int_a' является верным (от 0 до 3).\n";
}
if (filter_var($int_b, FILTER_VALIDATE_INT, $options) !== FALSE) {
    echo "Число B '$int_b' является верным (от 0 до 3).\n";
}
if (filter_var($int_c, FILTER_VALIDATE_INT, $options) !== FALSE) {
    echo "Число C '$int_c' является верным (от 0 до 3).\n";
}

$options['options']['default'] = 1;
if (($int_c = filter_var($int_c, FILTER_VALIDATE_INT, $options)) !== FALSE) {
    echo "Число C '$int_c' является верным (от 0 и 3).";
}
?>
```

Результат виконання наведеного прикладу:

```
Число A '1' является верным (от 0 до 3).
Число C '1' является верным (от 0 до 3).
```
