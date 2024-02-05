---
navigation:
  - function.rnp-load-keys-from-path.md: « rnp\_load\_keys\_from\_path
  - function.rnp-locate-key.md: rnp\_locate\_key »
  - index.md: PHP Manual
  - ref.rnp.md: Функції Rnp
title: rnp\_load\_keys
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rnp\_load\_keys

(PECL rnp >= 0.1.1)

rnp\_load\_keys — Завантажує ключі з рядка PHP

### Опис

```methodsynopsis
rnp_load_keys(    RnpFFI $ffi,    string $format,    string $input,    int $flags): bool
```

Зверніть увагу, що для G10 вхідними даними має бути каталог (який має вже існувати).

### Список параметрів

`ffi`

Об'єкт FFI, що повертається функцією rnp\_ffi\_create.

`format`

Формат даних (GPG, KBX, G10).

`input`

Пакети OpenPGP, які містять ключ(и), які потрібно завантажити. Можуть бути бінарними або ASCII-кодованими.

`flags`

Дивіться опис прапорів RNP\_LOAD\_SAVE\_\*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
