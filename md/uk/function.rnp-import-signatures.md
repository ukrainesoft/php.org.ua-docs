---
navigation:
  - function.rnp-import-keys.md: « rnp\_import\_keys
  - function.rnp-key-export-autocrypt.md: rnp\_key\_export\_autocrypt »
  - index.md: PHP Manual
  - ref.rnp.md: Функції Rnp
title: rnp\_import\_signatures
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rnp\_import\_signatures

(PECL rnp >= 0.1.1)

rnp\_import\_signatures — Імпортує автономні підписи у зв'язку ключів та отримує JSON з описом оновлених ключів

### Опис

```methodsynopsis
rnp_import_signatures(RnpFFI $ffi, string $input, int $flags): string|false
```

### Список параметрів

`ffi`

Об'єкт FFI, що повертається функцією rnp\_ffi\_create.

`input`

Пакети OpenPGP, що містять підписи, які потрібно імпортувати. Можуть бути бінарними або ASCII-кодованими.

`flags`

Нині має бути 0.

### Значення, що повертаються

JSON-рядок з інформацією про оновлені ключі у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
