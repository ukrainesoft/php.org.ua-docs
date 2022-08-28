Запечатати (зашифрувати) дані

-   [« openssl\_random\_pseudo\_bytes](function.openssl-random-pseudo-bytes.html)
    
-   [openssl\_sign »](function.openssl-sign.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenSSL](ref.openssl.html)
    
-   Запечатати (зашифрувати) дані
    

# opensslseal

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

opensslseal — Задрукувати (зашифрувати) дані

### Опис

```methodsynopsis
openssl_seal(    string $data,    string &$sealed_data,    array &$encrypted_keys,    array $public_key,    string $cipher_algo,    string &$iv = null): int|false
```

**opensslseal()** запечатує (шифрує) `data`, використовуючи метод `cipher_algo` із згенерованим випадково секретним ключем. Ключ буде зашифрований кожним відкритим ключем, вказаним у масиві `public_key`, і кожен зашифрований ключ буде поміщений у `encrypted_keys`. Тобто ви можете надіслати запечатані дані відразу кільком одержувачам. Кожен отримувач повинен отримати як запечатані дані, так і зашифрований відповідним відкритим ключем ключ для їхнього відкриття.

### Список параметрів

`data`

Дані, що запечатуються.

`sealed_data`

Запечатані дані.

`encrypted_keys`

Масив зашифрованих ключів.

`public_key`

Масив екземплярів [OpenSSLAsymmetricKey](class.opensslasymmetrickey.html), що містять відкриті ключі.

`cipher_algo`

Метод шифрування.

**Застереження**

Значення за замовчуванням (`'RC4'`) вважається небезпечним. Настійно рекомендується вказувати метод безпечного шифрування.

`iv`

Ініціалізуючий вектор.

### Значення, що повертаються

Повертає довжину запечатаних даних або **`false`**. У разі успішного виконання `sealed_data` містяться запечатані дані, а в `encrypted_keys` зашифровані ключі.

### список змін

| Версия | Описание                                                                                                                                                                                                            |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | `public_key` тепер приймає масив (array) екземплярів [OpenSSLAsymmetricKey](class.opensslasymmetrickey.html); раніше приймався масив (array) ресурсів ([resource](language.types.resource.html)) типу `OpenSSL key` |
|        | `cipher_algo` більше не є необов'язковим параметром.                                                                                                                                                                |
|        | `iv` тепер допускає значення null.                                                                                                                                                                                  |

### Приклади

**Приклад #1 Приклад використання **opensslseal()****

```php
<?php
// $data содержит данные для запечатывания

// извлекаем открытые ключи получателей и подготавливаем их
$fp = fopen("/src/openssl-0.9.6/demos/maurice/cert.pem", "r");
$cert = fread($fp, 8192);
fclose($fp);
$pk1 = openssl_get_publickey($cert);
// повторяем для второго получателя
$fp = fopen("/src/openssl-0.9.6/demos/sign/cert.pem", "r");
$cert = fread($fp, 8192);
fclose($fp);
$pk2 = openssl_get_publickey($cert);

// задаём метод
$method = 'AES256';

// генерируем IV
$ivLength = openssl_cipher_iv_length( $method );
$iv = openssl_random_pseudo_bytes( $ivLength, $strong );
if (! $strong) {
 error_log('Инициализирующий вектор может быть не крипографически сильным!');
}

// запечатываем сообщение, только владельцы $pk1 и $pk2 смогут его распечатать,
// используя ключи $ekeys[0] и $ekeys[1] соответственно.
openssl_seal($data, $sealed, $ekeys, array($pk1, $pk2), $method, $iv);

// освобождаем ресурсы ключей
openssl_free_key($pk1);
openssl_free_key($pk2);
?>
```

### Дивіться також

-   [openssl\_open()](function.openssl-open.html) - Відкрити запечатані дані