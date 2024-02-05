---
navigation:
  - function.rnp-dump-packets.md: « rnp\_dump\_packets
  - function.rnp-ffi-destroy.md: rnp\_ffi\_destroy »
  - index.md: PHP Manual
  - ref.rnp.md: Функції Rnp
title: rnp\_ffi\_create
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rnp\_ffi\_create

(PECL rnp >= 0.1.1)

rnp\_ffi\_create — Створює об'єкт верхнього рівня, який використовується для взаємодії з бібліотекою

### Опис

```methodsynopsis
rnp_ffi_create(string $pub_format, string $sec_format): RnpFFI|false
```

### Список параметрів

`pub_format`

Формат відкритого ключа, RNP\_KEYSTORE\_GPG або інша константа RNP\_KEYSTORE\_\*

`sec_format`

Формат закритого ключа, RNP\_KEYSTORE\_GPG або інша константа RNP\_KEYSTORE\_\*

### Значення, що повертаються

Повертає об'єкт [RnpFFI](class.rnpffi.md) у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
