Розшифровує дані

-   [« opensslcsrsign](function.openssl-csr-sign.html)
    
-   [opensslдхcomputekey »](function.openssl-dh-compute-key.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenSSL](ref.openssl.html)
    
-   Розшифровує дані
    

# openssldecrypt

(PHP 5> = 5.3.0, PHP 7, PHP 8)

openssldecrypt - Розшифровує дані

### Опис

```methodsynopsis
openssl_decrypt(    string $data,    string $cipher_algo,    string $passphrase,    int $options = 0,    string $iv = "",    ?string $tag = null,    string $aad = ""): string|false
```

Бере необроблений або кодований у base64 рядок і розшифровує його за допомогою заданого методу та ключа.

### Список параметрів

`data`

Дані для розшифрування.

`cipher_algo`

Метод шифрування. Список доступних методів можна отримати за допомогою функції [opensslgetciphermethods()](function.openssl-get-cipher-methods.html)

`passphrase`

Ключ.

`options`

`options` можна задати одній з констант: **`OPENSSL_RAW_DATA`** **`OPENSSL_ZERO_PADDING`**

`iv`

Ненульовий вектор, що ініціалізує.

`tag`

Тег аутентифікації в режимі шифрування AEAD. Якщо він некоректний, то автентифікація завершиться невдачею та функція поверне **`false`**

**Застереження**

Довжина `tag` не перевіряється функцією. Сторона, що викликає, несе відповідальність за те, щоб довжина тега відповідала довжині тега, отриманого при виклику [opensslencrypt()](function.openssl-encrypt.html). В іншому випадку, дешифрування може бути успішним, якщо цей тег збігається тільки з початком правильного тега.

`aad`

Додаткові автентифіковані дані.

### Значення, що повертаються

Розшифрований рядок або **`false`** у разі виникнення помилки.

### Помилки

Видає помилку рівня **`E_WARNING`**, якщо параметр `cipher_algo` передано невідомий алгоритм шифрування.

Видає помилку рівня **`E_WARNING`**, якщо параметр `iv` передано порожнє значення.

### список змін

| Версия | Описание                                     |
|--------|----------------------------------------------|
|        | Параметр `tag` тепер допускає значення null. |
|        | Додані параметри `tag` і `aad`               |

### Дивіться також

-   [opensslencrypt()](function.openssl-encrypt.html) - Шифрує дані