---
navigation:
  - function.rnp-import-signatures.md: « rnp\_import\_signatures
  - function.rnp-key-export-revocation.md: rnp\_key\_export\_revocation »
  - index.md: PHP Manual
  - ref.rnp.md: Функції Rnp
title: rnp\_key\_export\_autocrypt
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rnp\_key\_export\_autocrypt

(PECL rnp >= 0.1.1)

rnp\_key\_export\_autocrypt — Експортує мінімальний ключ для функції автоматичного шифрування (загалом 5 пакетів: ключ, uid, підпис, дочірній ключ шифрування, підпис)

### Опис

```methodsynopsis
rnp_key_export_autocrypt(    RnpFFI $ffi,    string $key_fp,    string $subkey_fp,    string $uid,    int $flags): string|false
```

### Список параметрів

`ffi`

Об'єкт FFI, що повертається функцією rnp\_ffi\_create.

`key_fp`

Цифровий відбиток первинного ключа.

`subkey_fp`

Дочірній ключ експорту. Може бути порожнім рядком, щоб вибрати перший відповідний дочірній ключ.

`uid`

Ідентифікатор користувача експорту. Може бути порожнім рядком, якщо у ключа, що експортується, тільки один uid.

`flags`

В даний час підтримується тільки **`RNP_KEY_EXPORT_BASE64`**. Увімкнення приведе до експорту даних ключа в кодуванні base64 замість двійкового.

### Значення, що повертаються

OpenPGP-пакети експортованого ключа у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
