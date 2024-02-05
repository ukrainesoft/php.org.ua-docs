---
navigation:
  - function.rnp-list-keys.md: « rnp\_list\_keys
  - function.rnp-load-keys.md: rnp\_load\_keys »
  - index.md: PHP Manual
  - ref.rnp.md: Функції Rnp
title: rnp\_load\_keys\_from\_path
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rnp\_load\_keys\_from\_path

(PECL rnp >= 0.1.1)

rnp\_load\_keys\_from\_path — Завантажує ключі із зазначеного шляху

### Опис

```methodsynopsis
rnp_load_keys_from_path(    RnpFFI $ffi,    string $format,    string $input_path,    int $flags): bool
```

Зверніть увагу, що для G10 вхідними даними має бути каталог (який має вже існувати).

### Список параметрів

`ffi`

Об'єкт FFI, що повертається функцією rnp\_ffi\_create.

`format`

Формат даних (GPG, KBX, G10).

`input_path`

Файл або каталог, який містить ключі.

`flags`

Дивіться опис прапорів RNP\_LOAD\_SAVE\_\*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
