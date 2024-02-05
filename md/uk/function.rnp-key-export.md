---
navigation:
  - function.rnp-key-export-revocation.md: « rnp\_key\_export\_revocation
  - function.rnp-key-get-info.md: rnp\_key\_get\_info »
  - index.md: PHP Manual
  - ref.rnp.md: Функції Rnp
title: rnp\_key\_export
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rnp\_key\_export

(PECL rnp >= 0.1.1)

rnp\_key\_export — Експортує ключ

### Опис

```methodsynopsis
rnp_key_export(RnpFFI $ffi, string $key_fp, int $flags): string|false
```

### Список параметрів

`ffi`

Об'єкт FFI, що повертається функцією rnp\_ffi\_create.

`key_fp`

Цифровий відбиток ключа.

`flags`

Дивіться певні константи **`RNP_KEY_EXPORT_*`**(за исключением\*\*`RNP_KEY_EXPORT_BASE64`\*\*

### Значення, що повертаються

OpenPGP-пакети експортованого ключа (двійкові або ASCII-закодовані) у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
