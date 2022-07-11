- [«openssl_digest](function.openssl-digest.md)
- [openssl_error_string »](function.openssl-error-string.md)

- [PHP Manual](index.md)
- [Функції OpenSSL](ref.openssl.md)
- Шифрує дані

#openssl_encrypt

(PHP 5 \>= 5.3.0, PHP 7, PHP 8)

openssl_encrypt — Шифрує дані

### Опис

**openssl_encrypt**(
string `$data`,
string `$cipher_algo`,
string `$passphrase`,
int `$options` = 0,
string `$iv` = "",
string `&$tag` = **`null`**,
string `$aad` = "",
int `$tag_length` = 16
): string\|false

Шифрує дані із заданим шифром та ключем і повертає необроблену
рядок, або рядок, закодований у base64

### Список параметрів

`data`
Дані для шифрування.

`cipher_algo`
Метод шифрування. Список доступних методів можна отримати за допомогою
функції
[openssl_get_cipher_methods()](function.openssl-get-cipher-methods.md).

`passphrase`
Кодова фраза. Якщо кодова фраза вкорочена, ніж очікувалося, вона
автоматично доповнюється символами `NUL`; якщо кодова фраза довша,
чим очікувалося, вона автоматично усікається.

`options`
`options` можна задати одній із констант: **`OPENSSL_RAW_DATA`**,
**`OPENSSL_ZERO_PADDING`**.

`iv`
Ненульовий вектор, що ініціалізує.

`tag`
Тег аутентифікації, що передається за посиланням, у режимі шифрування AEAD
(GCM або CCM).

`aad`
Додаткові автентифіковані дані.

`tag_length`
Довжина параметра `tag`. Для режиму GCM має бути від 4 до 16.

### Значення, що повертаються

Повертає зашифрований рядок або **`false`** у разі виникнення
помилки.

### Помилки

Видає помилку рівня **`E_WARNING`**, якщо в параметрі `cipher_algo`
передано невідомий алгоритм шифрування.

Видає помилку рівня **`E_WARNING`**, якщо параметр "iv" передано
пусте значення.

### Список змін

| Версія | Опис                                     |
|--------|------------------------------------------|
| 7.1.0  | Додані параметри tag, aad та tag_length. |

### Приклади

**Приклад #1 Приклад шифрування AES з автентифікацією в режимі GCM PHP
7.1+**

`<?php//$$key повинен бути згенерований заздалегідь криптографічно безпечним образом// наприклад, допомогою openssl_random_pseudo_bytes$plaintext =_ cip="cip="; ())){   $ivlen = openssl_cipher_iv_length($cipher); $iv = openssl_random_pseudo_bytes($ivlen); $ciphertext==openssl_encrypt($plaintext,$cipher,$key,$options=0,$iv, $tag); // зберігаємо $cipher, $iv і $tag для дальшого розшифровки    $original_plaintext = openssl_decrypt($ciphertext, $cipher, $key, $options=0| echo $original_plaintext."
";}?> `

**Приклад #2 Приклад шифрування AES з автентифікацією до PHP 7.1**

`<?php//$$key повинен бути згенерований заздалегідь криптографічно безпечним образом// наприклад, допомогою openssl_random_pseudo_bytes$plaintext =' "дані для шифрування$$; = openssl_random_pseudo_bytes($ivlen);$ciphertext_raw = openssl_encrypt($plaintext, $cipher, $key, $options=OPENSSL_RAW_DATA, $iv);$hmac = hash_h$ ;$ciphertext==base64_encode($iv.$hmac.$ciphertext_raw );// розшифровка....$c = base64_decode($ciphertext);$ivlen = openssl_cipher_iv_l$ iv = substr($c, 0, $ivlen);$hmac = substr($c, $ivlen, $sha2len=32);$ciphertext_raw = substr($c, $ivlen+$sha2len);$original_plaintext ciphertext_raw, $cipher, $ key, $ options = OPENSSL_RAW_DATA, $ iv); / порівняння, не схильне атаці за часу{   echo $original_plaintext."
";}?> `

### Дивіться також

- [openssl_decrypt()](function.openssl-decrypt.md) - Розшифровує
дані
