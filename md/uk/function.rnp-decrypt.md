---
navigation:
  - function.rnp-backend-version.md: « rnp\_backend\_version
  - function.rnp-dump-packets-to-json.md: rnp\_dump\_packets\_to\_json »
  - index.md: PHP Manual
  - ref.rnp.md: Функції Rnp
title: rnp\_decrypt
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rnp\_decrypt

(PECL rnp >= 0.1.1)

rnp\_decrypt — Розшифровує повідомлення PGP

### Опис

```methodsynopsis
rnp_decrypt(RnpFFI $ffi, string $input): string|false
```

Закриті ключі, які використовуються для розшифровки, повинні бути завантажені до об'єкта FFI перед викликом функції. Якщо використовувалось шифрування паролем, то провайдер пароля має бути встановлений викликом функції [rnp\_ffi\_set\_pass\_provider()](function.rnp-ffi-set-pass-provider.md)

### Список параметрів

`ffi`

Об'єкт FFI, що повертається функцією rnp\_ffi\_create.

`input`

Зашифровані повідомлення.

### Значення, що повертаються

Розшифроване повідомлення у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
