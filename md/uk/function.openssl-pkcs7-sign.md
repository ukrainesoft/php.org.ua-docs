---
navigation:
  - function.openssl-pkcs7-read.html: « opensslpkcs7read
  - function.openssl-pkcs7-verify.html: opensslpkcs7verify »
  - index.html: PHP Manual
  - ref.openssl.html: Функции OpenSSL
title: opensslpkcs7sign
---
# opensslpkcs7sign

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

opensslpkcs7sign — Підписати повідомлення S/MIME

### Опис

```methodsynopsis
openssl_pkcs7_sign(    string $input_filename,    string $output_filename,    OpenSSLCertificate|string $certificate,    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $private_key,    ?array $headers,    int $flags = PKCS7_DETACHED,    ?string $untrusted_certificates_filename = null): bool
```

**opensslpkcs7sign()** бере вміст файлу `input_filename` та підписує його з використанням сертифіката `certificate` та закритого ключа `private_key`

### Список параметрів

`input_filename`

Файл, який слід підписати.

`output_filename`

Файл, до якого буде записано цифровий підпис.

`certificate`

Сертифікат X.509, який буде використаний для підпису `input_filename`. Дивіться [параметри ключа/сертифіката](openssl.certparams.html)

`private_key`

`private_key` задається секретним ключем, що відповідає сертифікату (`certificate`). Дивіться [параметри відкритого/секретного ключа](openssl.certparams.html)

`headers`

`headers` задається масивом заголовків, які будуть додані на початок даних після підписання. (дивіться [opensslpkcs7encrypt()](function.openssl-pkcs7-encrypt.html) для отримання додаткової інформації про формат цього параметра).

`flags`

`flags` використовується для налаштування виводу. Дивіться [константи PKCS7](openssl.pkcs7.flags.html)

`untrusted_certificates_filename`

`untrusted_certificates_filename` може містити ім'я файлу, де зберігаються додаткові сертифікати для додавання їх до підпису, наприклад, для полегшення верифікації підпису різними користувачами.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `certificate` тепер приймає екземпляр [OpenSSLCertificate](class.opensslcertificate.html); раніше приймався ресурс ([resource](language.types.resource.html)) типу `OpenSSL X.509 CSR` |
|  | `private_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.html) або [OpenSSLCertificate](class.opensslcertificate.html); раніше приймався ресурс ([resource](language.types.resource.html)) типу `OpenSSL key` ор `OpenSSL X.509 CSR` |

### Приклади

**Приклад #1 Приклад використання **opensslpkcs7sign()****

```php
<?php
// сообщение, которое вы хотите подписать для того, чтобы получатели могли
// проверить, что его послали именно вы
$data = <<<EOD

Разрешаю потратить на обед с контрагентом не более 100,000 рублей.

Ваш директор.
EOD;
// сохраняем сообщение в фалй
$fp = fopen("msg.txt", "w");
fwrite($fp, $data);
fclose($fp);
// шифруем
if (openssl_pkcs7_sign("msg.txt", "signed.txt", "file://mycert.pem",
    array("file://mycert.pem", "mypassphrase"),
    array("To" => "joes@example.com", // ассоциативный синтаксис
          "From: HQ <ceo@example.com>", // индексированный синтаксис
          "Subject" => "Представительские расходы")
    )) {
    // сообщение подписано - отправляем!
    exec(ini_get("sendmail_path") . " < signed.txt");
}
?>
```
