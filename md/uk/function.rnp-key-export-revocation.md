---
navigation:
  - function.rnp-key-export-autocrypt.md: « rnp\_key\_export\_autocrypt
  - function.rnp-key-export.md: rnp\_key\_export »
  - index.md: PHP Manual
  - ref.rnp.md: Функції Rnp
title: rnp\_key\_export\_revocation
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rnp\_key\_export\_revocation

(PECL rnp >= 0.1.1)

rnp\_key\_export\_revocation — Генерує та експортує підпис відкликання первинного ключа

### Опис

```methodsynopsis
rnp_key_export_revocation(    RnpFFI $ffi,    string $key_fp,    int $flags,    array $options = ?): string|false
```

Примітка: щоб відкликати ключ, потрібно імпортувати підпис у сховище ключів або скористатися функцією [rnp\_key\_revoke()](function.rnp-key-revoke.md)

### Список параметрів

`ffi`

Об'єкт FFI, що повертається функцією rnp\_ffi\_create.

`key_fp`

Цифровий відбиток первинного ключа, який має бути відкликаний.

`flags`

\*\*`RNP_KEY_EXPORT_ARMORED`\*\*или 0.

`options`

Асоціативний масив із опціями.

| Ключ | Тип данных | Опис |
| --- | --- | --- |
| `"hash"` | string | Встановити хеш-алгоритм, який використовується під час обчислення підпису. |
| `"code"` | string | Код причини для коду відкликання. Можливі значення: 'no', 'supersed', 'compromised', 'retired'. Якщо не визначено, за замовчуванням буде використовуватися значення 'no'. |
| `"reason"` | string | Текстове подання причини відкликання. |

### Значення, що повертаються

Експортований підпис відкликання у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
