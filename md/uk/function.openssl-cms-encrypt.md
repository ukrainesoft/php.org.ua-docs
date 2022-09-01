---
navigation:
  - function.openssl-cms-decrypt.html: « opensslcmsdecrypt
  - function.openssl-cms-read.html: opensslcmsread »
  - index.html: PHP Manual
  - ref.openssl.html: Функции OpenSSL
title: opensslcmsencrypt
---
# opensslcmsencrypt

(PHP 8)

opensslcmsencrypt — Зашифровує CMS-повідомлення

### Опис

```methodsynopsis
openssl_cms_encrypt(    string $input_filename,    string $output_filename,    OpenSSLCertificate|array|string $certificate,    ?array $headers,    int $flags = 0,    int $encoding = OPENSSL_ENCODING_SMIME,    int $cipher_algo = OPENSSL_CIPHER_AES_128_CBC): bool
```

Шифрує вміст одного або кількох одержувачів на основі переданих йому сертифікатів.

### Список параметрів

`input_filename`

Файл, який потрібно зашифрувати.

`output_filename`

Вихідний файл.

`certificate`

Одержувачі, для яких виконується шифрування.

`headers`

Заголовки, які будуть увімкнені при використанні S/MIME.

`flags`

Прапори, що передаються CMSsign.

`encoding`

Кодування для виведення . **`OPENSSL_ENCODING_SMIME`** **`OPENSSL_ENCODING_DER`** або **`OPENSSL_ENCODING_PEM`**

`cipher_algo`

Алгоритм шифрування, що використовується.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Алгоритм шифрування за замовчуванням (`cipher_algo`) тепер AES-128-CBC (**`OPENSSL_CIPHER_AES_128_CBC`**). Раніше використовувався алгоритм PKCS7/CMS (**`OPENSSL_CIPHER_RC2_40`** |
