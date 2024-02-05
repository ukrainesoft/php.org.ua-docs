---
navigation:
  - function.openssl-csr-sign.md: « openssl\_csr\_sign
  - function.openssl-dh-compute-key.md: openssl\_dh\_compute\_key »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_decrypt
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_decrypt

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

openssl\_decrypt - Розшифровує дані

### Опис

```methodsynopsis
openssl_decrypt(    string $data,    string $cipher_algo,    string $passphrase,    int $options = 0,    string $iv = "",    ?string $tag = null,    string $aad = ""): string|false
```

Бере необроблений або кодований у base64 рядок і розшифровує його за допомогою заданого методу та ключа.

### Список параметрів

`data`

Дані для розшифрування.

`cipher_algo`

Метод шифрування. Список доступних методів можна отримати за допомогою функції [openssl\_get\_cipher\_methods()](function.openssl-get-cipher-methods.md)

`passphrase`

Ключ.

`options`

`options` можна задати одній з констант: **`OPENSSL_RAW_DATA`** **`OPENSSL_ZERO_PADDING`**

`iv`

Ненульовий вектор, що ініціалізує.

`tag`

Тег аутентифікації в режимі шифрування AEAD. Якщо він некоректний, то автентифікація завершиться невдачею та функція поверне **`false`**

**Застереження**

Довжина `tag` не перевіряється функцією. Сторона, що викликає, несе відповідальність за те, щоб довжина тега відповідала довжині тега, отриманого при виклику [openssl\_encrypt()](function.openssl-encrypt.md). В іншому випадку, дешифрування може бути успішним, якщо цей тег збігається тільки з початком правильного тега.

`aad`

Додаткові автентифіковані дані.

### Значення, що повертаються

Розшифрований рядок або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Видає помилку рівня **`E_WARNING`**, якщо параметр `cipher_algo` передано невідомий алгоритм шифрування.

Видає помилку рівня **`E_WARNING`**, якщо параметр `iv`передано пустое значение.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`tag` тепер допускає значення null. |
| 7.1.0 | Додані параметри `tag`и`aad` |

### Дивіться також

-   [openssl\_encrypt()](function.openssl-encrypt.md) \- Шифрує дані
