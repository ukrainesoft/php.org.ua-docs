---
navigation:
  - function.rnp-key-remove.md: « rnp\_key\_remove
  - function.rnp-list-keys.md: rnp\_list\_keys »
  - index.md: PHP Manual
  - ref.rnp.md: Функції Rnp
title: rnp\_key\_revoke
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rnp\_key\_revoke

(PECL rnp >= 0.1.1)

rnp\_key\_revoke — Відкликає ключ або дочірній ключ шляхом створення та додавання підпису відгуку

### Опис

```methodsynopsis
rnp_key_revoke(    RnpFFI $ffi,    string $key_fp,    int $flags,    array $options = ?): bool
```

Примітка: необхідно викликати функцію [rnp\_save\_keys()](function.rnp-save-keys.md) для запису оновлених зв'язок ключів.

### Список параметрів

`ffi`

Об'єкт FFI, що повертається функцією rnp\_ffi\_create.

`key_fp`

Цифровий відбиток ключа.

`flags`

Нині має бути 0.

`options`

Асоціативний масив із опціями.

| Ключ | Тип данных | Опис |
| --- | --- | --- |
| `"hash"` | string | Встановити хеш-алгоритм, який використовується під час обчислення підпису. |
| `"code"` | string | Код причини для коду відкликання. Можливі значення: 'no', 'supersed', 'compromised', 'retired'. Якщо не визначено, за замовчуванням буде використовуватися значення 'no'. |
| `"reason"` | string | Текстове подання причини відкликання. |

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
