- [« openssl_cms_sign](function.openssl-cms-sign.md)
- [openssl_csr_export_to_file »](function.openssl-csr-export-to-file.md)

- [PHP Manual](index.md)
- [Функції OpenSSL](ref.openssl.md)
- Перевіряє підпис CMS

#openssl_cms_verify

(PHP 8)

openssl_cms_verify — Перевіряє підпис CMS

### Опис

**openssl_cms_verify**(
string `$input_filename`,
int `$flags` = 0,
?string `$certificates` = **`null`**,
array `$ca_info` = [],
?string `$untrusted_certificates_filename` = **`null`**,
?string `$content` = **`null`**,
?string `$pk7` = **`null`**,
?string `$sigfile` = **`null`**,
int `$encoding` = **`OPENSSL_ENCODING_SMIME`**
): bool

Перевіряє підпис CMS, прикріплений або від'єднаний, із зазначеним
кодуванням.

### Список параметрів

`input_filename`
Вхідний файл

`flags`
Прапори, які передаються **cms_verify()**.

`certificates`
Файл із сертифікатом, який підписав і, на вибір, проміжними
сертифікати.

`ca_info`
Масив, що містить самозавірені сертифікати центру сертифікації.

`untrusted_certificates_filename`
Файл, який містить додаткові проміжні сертифікати.

`content`
Файл, який показує вміст, коли підписи від'єднані.

`pk7`

`sigfile`
Файл, який потрібно зберегти підпис.

`encoding`
Кодування вхідного файлу. **`OPENSSL_ENCODING_SMIME`**,
**`OPENSSL_ENCODING_DER`** або **`OPENSSL_ENCODING_PEM`**.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.
