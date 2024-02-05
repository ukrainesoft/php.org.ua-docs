---
navigation:
  - function.rnp-op-verify.md: « rnp\_op\_verify
  - function.rnp-save-keys.md: rnp\_save\_keys »
  - index.md: PHP Manual
  - ref.rnp.md: Функції Rnp
title: rnp\_save\_keys\_to\_path
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rnp\_save\_keys\_to\_path

(PECL rnp >= 0.1.1)

rnp\_save\_keys\_to\_path — Зберігає ключі вказаним шляхом

### Опис

```methodsynopsis
rnp_save_keys_to_path(    RnpFFI $ffi,    string $format,    string $output_path,    int $flags): bool
```

Зберігає ключі, присутні в об'єкті FFI (завантаженому або згенерованому), у вказаному файлі або каталозі.

### Список параметрів

`ffi`

Об'єкт FFI, що повертається функцією rnp\_ffi\_create.

`format`

Формат даних (GPG, KBX, G10).

`output_path`

Шлях до файлу або каталогу, до якого мають бути збережені ключі.

`flags`

Дивіться опис прапорів RNP\_LOAD\_SAVE\_\*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
