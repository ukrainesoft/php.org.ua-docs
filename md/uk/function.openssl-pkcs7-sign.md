---
navigation:
  - function.openssl-pkcs7-read.md: « openssl\_pkcs7\_read
  - function.openssl-pkcs7-verify.md: openssl\_pkcs7\_verify »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_pkcs7\_sign
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_pkcs7\_sign

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

openssl\_pkcs7\_sign — Підписати повідомлення S/MIME

### Опис

```methodsynopsis
openssl_pkcs7_sign(    string $input_filename,    string $output_filename,    OpenSSLCertificate|string $certificate,    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $private_key,    ?array $headers,    int $flags = PKCS7_DETACHED,    ?string $untrusted_certificates_filename = null): bool
```

**openssl\_pkcs7\_sign()** бере вміст файлу `input_filename` та підписує його з використанням сертифіката `certificate` та закритого ключа `private_key`

### Список параметрів

`input_filename`

Файл, який слід підписати.

`output_filename`

Файл, до якого буде записано цифровий підпис.

`certificate`

Сертифікат X.509, який буде використаний для підпису `input_filename`Смотрите[параметри ключа/сертифіката](openssl.certparams.md)

`private_key`

`private_key` задається секретним ключем, що відповідає сертифікату (`certificate`). Смотрите[параметри відкритого/секретного ключа](openssl.certparams.md)

`headers`

`headers` задається масивом заголовків, які будуть додані на початок даних після підписання. (дивіться [openssl\_pkcs7\_encrypt()](function.openssl-pkcs7-encrypt.md) для отримання додаткової інформації про формат цього параметра).

`flags`

`flags` використовується для налаштування виводу. Дивіться [константи PKCS7](openssl.pkcs7.flags.md)

`untrusted_certificates_filename`

`untrusted_certificates_filename` може містити ім'я файлу, де зберігаються додаткові сертифікати для додавання їх до підпису, наприклад, для полегшення верифікації підпису різними користувачами.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `certificate` тепер приймає екземпляр [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL X.509 CSR` |
| 8.0.0 | `private_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) або [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL key`or`OpenSSL X.509 CSR` |

### Приклади

**Пример #1 Пример использования**openssl\_pkcs7\_sign()\*\*\*\*

```php
<?php
// сообщение, которое вы хотите подписать для того, чтобы получатели могли
// проверить, что его послали именно вы
$data = <<<EOD

Разрешаю потратить на обед с контрагентом не более 100,000 рублей.

Ваш директор.
EOD;
// сохраняем сообщение в фалй
$fp = fopen("msg.txt", "w");
fwrite($fp, $data);
fclose($fp);
// шифруем
if (openssl_pkcs7_sign("msg.txt", "signed.txt", "file://mycert.pem",
    array("file://mycert.pem", "mypassphrase"),
    array("To" => "joes@example.com", // ассоциативный синтаксис
          "From: HQ <ceo@example.com>", // индексированный синтаксис
          "Subject" => "Представительские расходы")
    )) {
    // сообщение подписано - отправляем!
    exec(ini_get("sendmail_path") . " < signed.txt");
}
?>
```
