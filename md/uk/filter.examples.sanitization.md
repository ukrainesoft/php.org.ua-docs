---
navigation:
  - filter.examples.validation.md: « Перевірка (валідація)
  - ref.filter.md: Функції фільтрації даних »
  - index.md: PHP Manual
  - filter.examples.md: Приклади
title: Очищення (нормалізація)
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Очищення (нормалізація)

**Приклад #1 Нормалізація та валідація e-mail адрес**

```php
<?php
$a = 'joe@example.org';
$b = 'bogus - at - example dot org';
$c = '(bogus@example.org)';

$sanitized_a = filter_var($a, FILTER_SANITIZE_EMAIL);
if (filter_var($sanitized_a, FILTER_VALIDATE_EMAIL)) {
    echo "Нормализованный e-mail (a) является верным.\n";
}

$sanitized_b = filter_var($b, FILTER_SANITIZE_EMAIL);
if (filter_var($sanitized_b, FILTER_VALIDATE_EMAIL)) {
    echo "Нормализованный e-mail (b) является верным.";
} else {
    echo "Нормализованный e-mail (b) является неверным.\n";
}

$sanitized_c = filter_var($c, FILTER_SANITIZE_EMAIL);
if (filter_var($sanitized_c, FILTER_VALIDATE_EMAIL)) {
    echo "Нормализованный e-mail (c) является верным.\n";
    echo "До нормализации: $c\n";
    echo "После нормализации: $sanitized_c\n";
}
?>
```

Результат виконання наведеного прикладу:

```
Нормализованный e-mail (a) является верным.
Нормализованный e-mail (b) является неверным.
Нормализованный e-mail (c) является верным.
До нормализации: (bogus@example.org)
После нормализации: bogus@example.org
```

**Приклад #2 Налаштування стандартного фільтра**

```php
filter.default = full_special_chars
filter.default_flags = 0
```
