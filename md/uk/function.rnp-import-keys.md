---
navigation:
  - function.rnp-ffi-set-pass-provider.md: « rnp\_ffi\_set\_pass\_provider
  - function.rnp-import-signatures.md: rnp\_import\_signatures »
  - index.md: PHP Manual
  - ref.rnp.md: Функції Rnp
title: rnp\_import\_keys
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rnp\_import\_keys

(PECL rnp >= 0.1.1)

rnp\_import\_keys — Імпортує ключі з рядка PHP у зв'язок ключів і отримує JSON з описом нових/оновлених ключів

### Опис

```methodsynopsis
rnp_import_keys(RnpFFI $ffi, string $input, int $flags): string|false
```

### Список параметрів

`ffi`

Об'єкт FFI, що повертається функцією rnp\_ffi\_create.

`input`

Пакети OpenPGP, які містять ключ(и), які потрібно завантажити. Можуть бути бінарними або ASCII-кодованими.

`flags`

Дивіться певні константи **`RNP_LOAD_SAVE_*`**

### Значення, що повертаються

JSON-рядок з інформацією про нові та оновлені ключі у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
