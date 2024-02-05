---
navigation:
  - function.rnp-ffi-destroy.md: « rnp\_ffi\_destroy
  - function.rnp-import-keys.md: rnp\_import\_keys »
  - index.md: PHP Manual
  - ref.rnp.md: Функції Rnp
title: rnp\_ffi\_set\_pass\_provider
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rnp\_ffi\_set\_pass\_provider

(PECL rnp >= 0.1.1)

rnp\_ffi\_set\_pass\_provider — Встановлює callback-функцію постачальника паролів

### Опис

```methodsynopsis
rnp_ffi_set_pass_provider(RnpFFI $ffi, callable $password_callback): bool
```

Встановлює callback-функцію постачальника пароля. Функція може запитувати пароль на стандартному вході (якщо PHP скрипт виконується в середовищі командного рядка), відображати діалог GUI або надавати пароль будь-яким іншим способом. Запитані паролі використовуються для шифрування або розшифрування секретних ключів або виконання операцій симетричного шифрування/дешифрування.

### Список параметрів

`ffi`

Об'єкт FFI, що повертається функцією rnp\_ffi\_create.

`password_callback`

Функція, яка буде викликатись для кожного запиту пароля. У неї наступна сигнатура:

```methodsynopsis
password_callback(string $key_fp, string $pgp_context, string &$password): bool
```

-   `$key_fp`\- Цифровий відбиток, якщо такий є. Може бути порожнім.
-   `$pgp_context`\- Рядок, що описує, чому запитується ключ.
-   `$password`\- Посилання на рядок пароля, в якому повинен зберігатись наданий пароль.

Callback-функція має повертати **`true`**, якщо пароль був успішно встановлений або \*\*`false`\*\*в случае возникновения ошибки.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад простої callback-функції**

```php
<?php
function password_callback(string $key_fp, string $pgp_context, string &$password)
{
    $password = "password";

    return true;
}

$ffi = rnp_ffi_create('GPG', 'GPG');

rnp_ffi_set_pass_provider($ffi, 'password_callback');
```
