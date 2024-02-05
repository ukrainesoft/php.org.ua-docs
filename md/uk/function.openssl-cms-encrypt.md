---
navigation:
  - function.openssl-cms-decrypt.md: « openssl\_cms\_decrypt
  - function.openssl-cms-read.md: openssl\_cms\_read »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_cms\_encrypt
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_cms\_encrypt

(PHP 8)

openssl\_cms\_encrypt — Зашифровує CMS-повідомлення

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

Прапори, що передаються CMS\_sign.

`encoding`

Кодування для виведення . **`OPENSSL_ENCODING_SMIME`** **`OPENSSL_ENCODING_DER`** або **`OPENSSL_ENCODING_PEM`**

`cipher_algo`

Алгоритм шифрування, що використовується.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Алгоритм шифрування за замовчуванням (`cipher_algo`) тепер AES-128-CBC (**`OPENSSL_CIPHER_AES_128_CBC`**). Раніше використовувався алгоритм PKCS7/CMS (**`OPENSSL_CIPHER_RC2_40`** |
