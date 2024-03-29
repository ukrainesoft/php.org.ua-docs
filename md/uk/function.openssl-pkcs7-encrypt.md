---
navigation:
  - function.openssl-pkcs7-decrypt.md: « openssl\_pkcs7\_decrypt
  - function.openssl-pkcs7-read.md: openssl\_pkcs7\_read »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_pkcs7\_encrypt
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_pkcs7\_encrypt

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

openssl\_pkcs7\_encrypt — Шифрує повідомлення S/MIME

### Опис

```methodsynopsis
openssl_pkcs7_encrypt(    string $input_filename,    string $output_filename,    OpenSSLCertificate|array|string $certificate,    ?array $headers,    int $flags = 0,    int $cipher_algo = OPENSSL_CIPHER_AES_128_CBC): bool
```

**openssl\_pkcs7\_encrypt()** читає повідомлення з файлу `input_filename`шифрує його за допомогою 40-бітного RC2 шифру таким чином, що розшифрувати його можуть тільки одержувачі, зазначеними в `certificate`

### Список параметрів

`input_filename`

`output_filename`

`certificate`

Масив, або одиничний сертифікат X.509.

`headers`

`headers` задається масивом заголовків, які будуть додані на початок повідомлення перед шифруванням.

`headers` може бути як асоціативним масивом, де як ключі використовуються імена заголовків, або індексованим масивом, що містить повні рядки заголовків.

`flags`

`flags`используется для настройки процесса шифрования. Смотрите[Константи PKCS7](openssl.pkcs7.flags.md)

`cipher_algo`

Одна из[констант шифрів](openssl.ciphers.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Алгоритм шифрування за замовчуванням (`cipher_algo`) тепер AES-128-CBC (**`OPENSSL_CIPHER_AES_128_CBC`**). Раніше використовувався алгоритм PKCS7/CMS (**`OPENSSL_CIPHER_RC2_40`** |
| 8.0.0 | `certificate` тепер приймає екземпляр [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL X.509 CSR` |

### Приклади

**Приклад #1 Приклад використання** openssl\_pkcs7\_encrypt()\*\*\*\*

```php
<?php
// Сообщение, которое вы хотите зашифровать и отправить своему секретному
// агенту с позывным Козодой. У вас есть его сертификат в файле nighthawk.pem
$data = <<<EOD
Козодой,

Совершенно секретно! После прочтения сжечь!

Враги приближаются! Связной с новым поддельным паспортом
будет ждать тебя завтра в кафе в 8.30 утра.

Пароль - "У вас ус отклеился!"
Отзыв - "Это не ус, а борода!"

EOD;

// загружаем ключ
$key = file_get_contents("nighthawk.pem");

// записываем сообщение в файл
$fp = fopen("msg.txt", "w");
fwrite($fp, $data);
fclose($fp);

// шифруем
if (openssl_pkcs7_encrypt("msg.txt", "enc.txt", $key,
    array("To" => "nighthawk@example.com", // ассоциативный синтаксис
          "From: HQ <hq@example.com>", // индексированный синтаксис
          "Subject" => "СРОЧНО!!! ВАЖНО!!!"))) {
    // сообщение зашифровано - отправляем!!
    exec(ini_get("sendmail_path") . " < enc.txt");
}
?>
```
