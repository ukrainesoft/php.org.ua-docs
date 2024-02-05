---
navigation:
  - function.rnp-save-keys-to-path.md: « rnp\_save\_keys\_to\_path
  - function.rnp-supported-features.md: rnp\_supported\_features »
  - index.md: PHP Manual
  - ref.rnp.md: Функції Rnp
title: rnp\_save\_keys
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rnp\_save\_keys

(PECL rnp >= 0.1.1)

rnp\_save\_keys — Зберігає ключі у рядку PHP

### Опис

```methodsynopsis
rnp_save_keys(    RnpFFI $ffi,    string $format,    string &$output,    int $flags): bool
```

Обратите внимание, что для G10 значением`output` має бути каталог (який вже має існувати).

### Список параметрів

`ffi`

Об'єкт FFI, що повертається функцією rnp\_ffi\_create.

`format`

Формат даних (GPG, KBX, G10).

`output`

Ключові пакети будуть збережені у рядку, на який посилається `output`

`flags`

Дивіться опис прапорів RNP\_LOAD\_SAVE\_\*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
