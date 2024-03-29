---
navigation:
  - function.openssl-pkcs7-verify.md: « openssl\_pkcs7\_verify
  - function.openssl-pkey-export-to-file.md: openssl\_pkey\_export\_to\_file »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_pkey\_derive
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_pkey\_derive

(PHP 7 >= 7.3.0, PHP 8)

openssl\_pkey\_derive — Обчислює загальний секрет відкритого значення віддаленого та локального ключа DH або ECDH

### Опис

```methodsynopsis
openssl_pkey_derive(OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $public_key, OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $private_key, int $key_length = 0): string|false
```

\*\*openssl\_pkey\_derive()\*\*принимает набор из`public_key`и`private_key` і породжує загальний секрет ключів DH або EC.

### Список параметрів

`public_key`

Відкритий ключ для виведення. Список допустимих значень дивіться у розділі [Параметри ключа/сертифіката](openssl.certparams.md)

`private_key`

Закритий ключ для виведення. Список допустимих значень дивіться у розділі [Параметри ключа/сертифіката](openssl.certparams.md)

`key_length`

Встановлює бажану довжину секрету, що виробляється, якщо значення не дорівнює нулю.

### Значення, що повертаються

Зроблений секрет у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** openssl\_pkey\_derive()\*\*\*\*

```php
<?php
// Загрузка закрытого ключа
$priv = openssl_pkey_get_private("-----BEGIN PRIVATE KEY-----
MIICJgIBADCCARcGCSqGSIb3DQEDATCCAQgCggEBAJLxRCaZ933uW+AXmabHFDDy
upojBIRlbmQLJZfigDaSA1f9YOTsIv+WwVFTX/J1mtCyx9uBcz0Nt2kmVwxWuc2f
VtCEMPsmLsVXX7xRUFLpyX1Y1IYGBVXQOoOvLWYQjpZgnx47Pkh1Ok1+smffztfC
0DCNt4KorWrbsPcmqBejXHN79KvWFjZmXOksRiNu/Bn76RiqvofC4z8Ri3kHXQG2
197JGZzzFXHadGC3xbkg8UxsNbYhVMKbm0iANfafUH7/hoS9UjAVQYtvwe7YNiW/
HnyfVCrKwcc7sadd8Iphh+3lf5P1AhaQEAMytanrzq9RDXKBxuvpSJifRYasZYsC
AQIEggEEAoIBAGwAYC2E81Y1U2Aox0U7u1+vBcbht/OO87tutMvc4NTLf6NLPHsW
cPqBixs+3rSn4fADzAIvdLBmogjtiIZoB6qyHrllF/2xwTVGEeYaZIupQH3bMK2b
6eUvnpuu4Ytksiz6VpXBBRMrIsj3frM+zUtnq8vKUr+TbjV2qyKR8l3eNDwzqz30
dlbKh9kIhZafclHfRVfyp+fVSKPfgrRAcLUgAbsVjOjPeJ90xQ4DTMZ6vjiv6tHM
hkSjJIcGhRtSBzVF/cT38GyCeTmiIA/dRz2d70lWrqDQCdp9ArijgnpjNKAAulSY
CirnMsGZTDGmLOHg4xOZ5FEAzZI2sFNLlcw=
-----END PRIVATE KEY-----
");

// Загрузка открытого ключа
$pub = openssl_pkey_get_public("-----BEGIN PUBLIC KEY-----
MIICJDCCARcGCSqGSIb3DQEDATCCAQgCggEBAJLxRCaZ933uW+AXmabHFDDyupoj
BIRlbmQLJZfigDaSA1f9YOTsIv+WwVFTX/J1mtCyx9uBcz0Nt2kmVwxWuc2fVtCE
MPsmLsVXX7xRUFLpyX1Y1IYGBVXQOoOvLWYQjpZgnx47Pkh1Ok1+smffztfC0DCN
t4KorWrbsPcmqBejXHN79KvWFjZmXOksRiNu/Bn76RiqvofC4z8Ri3kHXQG2197J
GZzzFXHadGC3xbkg8UxsNbYhVMKbm0iANfafUH7/hoS9UjAVQYtvwe7YNiW/Hnyf
VCrKwcc7sadd8Iphh+3lf5P1AhaQEAMytanrzq9RDXKBxuvpSJifRYasZYsCAQID
ggEFAAKCAQAiCSBpxvGgsTorxAWtcAlSmzAJnJxFgSPef0g7OjhESytnc8G2QYmx
ovMt5KVergcitztWh08hZQUdAYm4rI+zMlAFDdN8LWwBT/mGKSzRkWeprd8E7mvy
ucqC1YXCMqmIwPySvLQUB/Dl8kgau7BLAnIJm8VP+MVrn8g9gghD0qRCgPgtEaDV
vocfgnOU43rhKnIgO0cHOKtw2qybSFB8QuZrYugq4j8Bwkrzh6rdMMeyMl/ej5Aj
c0wamOzuBDtXt0T9+Fx3khHaowjCc7xJZRgZCxg43SbqMWJ9lUg94I7+LTX61Gyv
dtlkbGbtoDOnxeNnN93gwQZngGYZYciu
-----END PUBLIC KEY-----
");

// Выводит шестнадцатеричную версию произведённого ключа
echo bin2hex(openssl_pkey_derive($pub,$priv));
```
