---
navigation:
  - function.rnp-key-get-info.md: « rnp\_key\_get\_info
  - function.rnp-key-revoke.md: rnp\_key\_revoke »
  - index.md: PHP Manual
  - ref.rnp.md: Функції Rnp
title: rnp\_key\_remove
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rnp\_key\_remove

(PECL rnp >= 0.1.1)

rnp\_key\_remove — Видаляє ключ зі зв'язування

### Опис

```methodsynopsis
rnp_key_remove(RnpFFI $ffi, string $key_fp, int $flags): bool
```

Примітка: необхідно викликати функцію [rnp\_save\_keys()](function.rnp-save-keys.md) для запису оновлених зв'язок ключів.

### Список параметрів

`ffi`

Об'єкт FFI, що повертається функцією rnp\_ffi\_create.

`key_fp`

Цифровий відбиток ключа.

`flags`

Дивіться константи **`RNP_KEY_REMOVE_*`**Флаг**`RNP_KEY_REMOVE_SUBKEYS`** буде працювати тільки для первинного ключа і видалить також його підключи.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
