---
navigation:
  - rnp.examples.md: « Приклади
  - ref.rnp.md: Функції Rnp »
  - index.md: PHP Manual
  - rnp.examples.md: Приклади
title: Підписання тексту
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Підписання тексту

У цьому прикладі буде підписання заданого тексту.

**Приклад #1 Приклад розрахунку RNP**

```php
<?php
// Инициализация объекта FFI
$ffi = rnp_ffi_create('GPG', 'GPG');

// Генерация ключа RSA
$key = rnp_op_generate_key($ffi, 'test@example.com', 'RSA');

// Подписание
$data = "Пример текста для подписи";
$signature = rnp_op_sign_cleartext($ffi, $data, array($key));

echo $signature;

// Уничтожение объекта FFI
rnp_ffi_destroy($ffi);
?>
```
