---
navigation:
  - function.rnp-key-revoke.md: « rnp\_key\_revoke
  - function.rnp-load-keys-from-path.md: rnp\_load\_keys\_from\_path »
  - index.md: PHP Manual
  - ref.rnp.md: Функції Rnp
title: rnp\_list\_keys
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rnp\_list\_keys

(PECL rnp >= 0.1.1)

rnp\_list\_keys — Перерахує всі ключі, які є у зв'язці ключів, за вказаним типом ідентифікатора

### Опис

```methodsynopsis
rnp_list_keys(RnpFFI $ffi, string $identifier_type): array|false
```

### Список параметрів

`ffi`

Об'єкт FFI, що повертається функцією rnp\_ffi\_create.

`identifier_type`

Тип ідентифікатора ключа ("userid", "keyid", "grip", "fingerprint").

### Значення, що повертаються

Асоціативний масив, де ключ - рядок ідентифікатора, а значення - цифровий відбиток ключа PGP або \*\*`false`\*\*в случае возникновения ошибки.
