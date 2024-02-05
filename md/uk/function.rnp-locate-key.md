---
navigation:
  - function.rnp-load-keys.md: « rnp\_load\_keys
  - function.rnp-op-encrypt.md: rnp\_op\_encrypt »
  - index.md: PHP Manual
  - ref.rnp.md: Функції Rnp
title: rnp\_locate\_key
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rnp\_locate\_key

(PECL rnp >= 0.1.1)

rnp\_locate\_key — Пошук ключа

### Опис

```methodsynopsis
rnp_locate_key(RnpFFI $ffi, string $identifier_type, string $identifier): string|false
```

Примітка: під час пошуку userid перевіряються лише дійсні імена користувачів.

### Список параметрів

`ffi`

Об'єкт FFI, що повертається функцією rnp\_ffi\_create.

`identifier_type`

Рядок типу ідентифікатора: "userid", "keyid", "fingerprint", "grip".

`identifier`

PGP ідентифікатор користувача (ім'я та e-mail) для типу "userid", шістнадцятковий рядок, який являє собою ідентифікатор ключа, цифровий відбиток або захоплення ключа відповідно.

### Значення, що повертаються

Повертає шістнадцятковий цифровий відбиток ключа, знайденого у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
