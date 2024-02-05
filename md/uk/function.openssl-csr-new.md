---
navigation:
  - function.openssl-csr-get-subject.md: « openssl\_csr\_get\_subject
  - function.openssl-csr-sign.md: openssl\_csr\_sign »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_csr\_new
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_csr\_new

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

openssl\_csr\_new — Генерує CSR

### Опис

```methodsynopsis
openssl_csr_new(    array $distinguished_names,    OpenSSLAsymmetricKey &$private_key,    ?array $options = null,    ?array $extra_attributes = null): OpenSSLCertificateSigningRequest|false
```

**openssl\_csr\_new()** створює новий CSR ґрунтуючись на інформації, зазначеній у параметрі `distinguished_names`

> **Зауваження**: Для коректної роботи цієї функції має бути правильний openssl.cnf. Для більш детальної інформації дивіться зауваження під [розділом установки](openssl.installation.md)

### Список параметрів

`distinguished_names`

Унікальне ім'я (Distinguished Name) або поля суб'єкта для використання у сертифікаті.

`private_key`

Параметр`private_key` має бути заданий закритим ключем раніше згенерованим функцією [openssl\_pkey\_new()](function.openssl-pkey-new.md) (або отриманий за допомогою будь-якої іншої функції сімейства openssl\_pkey). Відповідна відкрита частина ключа буде використана для підписання CSR.

`options`

За замовчуванням для ініціалізації запиту використовується інформація з системного `openssl.conf`. Ви можете вказати розділ конфігураційного файлу шляхом завдання ключа `config_section_section`в`options`. Також ви можете задати альтернативний конфігураційний файл openssl шляхом завдання ключа `config` значенням шляху до нього. Відповідність ключів, зазначених у `options`ключам из`openssl.conf`представлено ниже.

**Перевизначення конфігурації**

| Ключ `options` | Тип | Соответствие в `openssl.conf` | Опис |
| --- | --- | --- | --- |
| digest\_alg | string | default\_md | Один из методов[openssl\_get\_md\_methods()](function.openssl-get-md-methods.md) |
| x509\_extensions | string | x509\_extensions | Визначає, яке розширення має використовуватись для створення сертифіката x509 |
| req\_extensions | string | req\_extensions | Визначає, яке розширення має використовуватись для створення CSR |
| private\_key\_bits | int | default\_bits | Задає, скільки біт має використовуватись для генерації закритого ключа |
| private\_key\_type | int | none | Задає тип закритого ключа, що створюється. Одна з констант: **`OPENSSL_KEYTYPE_DSA`** **`OPENSSL_KEYTYPE_DH`** **`OPENSSL_KEYTYPE_RSA`**или**`OPENSSL_KEYTYPE_EC`**По умолчанию**`OPENSSL_KEYTYPE_RSA`** |
| encrypt\_key | bool | encrypt\_key | Чи повинен шифруватися (паролем) ключ, що експортується? |
| encrypt\_key\_cipher | int | none | Одна из[констант шифрів](openssl.ciphers.md) |
| curve\_name | string | none | Одне з [openssl\_get\_curve\_names()](function.openssl-get-curve-names.md) |
| config | string | N/A | Шлях до альтернативного конфігураційного файлу openssl.conf. |

`extra_attributes`

`extra_attributes` використовується для визначення додаткових опцій для CSR. І `distinguished_names`, и`extra_attributes` є асоціативними масивами, ключі яких перетворюються на OI-и і застосовуються до відповідних частин запиту.

### Значення, що повертаються

Повертає CSR або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `csr` тепер приймає екземпляр [OpenSSLCertificateSigningRequest](class.opensslcertificatesigningrequest.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL X.509 CSR` |
| 8.0.0 | `private_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL key` |
| 7.1.0 | Параметр`options` тепер підтримує `curve_name` |

### Приклади

**Приклад #1 Створення самопідписаного сертифіката**

```php
<?php
// для сервера сертификации SSL, commonName является доменным именем
// для сертификатов S/MIME, commonName является владельцем расположения адреса email
// и поля идентификации относятся к владельцу домена или электронной почты,
// подлежащим защите
$dn = array(
    "countryName" => "GB",
    "stateOrProvinceName" => "Somerset",
    "localityName" => "Glastonbury",
    "organizationName" => "The Brain Room Limited",
    "organizationalUnitName" => "PHP Documentation Team",
    "commonName" => "Wez Furlong",
    "emailAddress" => "wez@example.com"
);

// Создание пары закрытый/открытый ключ
$privkey = openssl_pkey_new(array(
    "private_key_bits" => 2048,
    "private_key_type" => OPENSSL_KEYTYPE_RSA,
));

// Создание CSR
$csr = openssl_csr_new($dn, $privkey, array('digest_alg' => 'sha256'));

// Создание самоподписанного сертификата со сроком жизни 365 дней
$x509 = openssl_csr_sign($csr, null, $privkey, $days=365, array('digest_alg' => 'sha256'));

// Сохранение закрытого ключа, CSR и самоподписанного сертификата
openssl_csr_export($csr, $csrout) and var_dump($csrout);
openssl_x509_export($x509, $certout) and var_dump($certout);
openssl_pkey_export($privkey, $pkeyout, "mypassword") and var_dump($pkeyout);

// Покажем возникшие ошибки, если они были
while (($e = openssl_error_string()) !== false) {
    echo $e . "\n";
}
?>
```

**Приклад #2 Створення самопідписаного сертифіката ECC (починаючи з PHP 7.1.0)**

```php
<?php
$subject = array(
    "commonName" => "docs.php.net",
);

// Создание пары закрытый/открытый ключ
$private_key = openssl_pkey_new(array(
    "private_key_type" => OPENSSL_KEYTYPE_EC,
    "curve_name" => 'prime256v1',
));

// Создание CSR
$csr = openssl_csr_new($subject, $private_key, array('digest_alg' => 'sha384'));

// Создание самоподписанного EC сертификата
$x509 = openssl_csr_sign($csr, null, $private_key, $days=365, array('digest_alg' => 'sha384'));
openssl_x509_export_to_file($x509, 'ecc-cert.pem');
openssl_pkey_export_to_file($private_key, 'ecc-private.key');
?>
```

### Дивіться також

-   [openssl\_csr\_sign()](function.openssl-csr-sign.md) \- Підписати CSR за допомогою іншого сертифіката (або ним же) та створити сертифікат
