---
navigation:
  - function.openssl-spki-export.md: « openssl\_spki\_export
  - function.openssl-spki-verify.md: openssl\_spki\_verify »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_spki\_new
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_spki\_new

(PHP 5 >= 5.6.0, PHP 7, PHP 8)

openssl\_spki\_new — Створення нового відкритого підписаного ключа з викликом

### Опис

```methodsynopsis
openssl_spki_new(OpenSSLAsymmetricKey $private_key, string $challenge, int $digest_algo = OPENSSL_ALGO_MD5): string|false
```

Створює новий підписаний відкритий ключ із викликом, використовуючи вказаний алгоритм хешування.

### Список параметрів

`private_key`

`private_key` задається секретним ключем, створеним раніше функцією [openssl\_pkey\_new()](function.openssl-pkey-new.md) (або отриманий іншим чином). Відповідна відкрита частина ключа буде використана для підпису CSR.

`challenge`

Дзвінок, пов'язаний з SPKAC

`digest_algo`

Алгоритм хешування. Дивіться openssl\_get\_md\_method().

### Значення, що повертаються

Повертає підписаний відкритий ключ із рядком дзвінка або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Викликає помилку рівня **`E_WARNING`**, якщо вказано некоректний алгоритм у `digest_algo`

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `private_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL key` |

### Приклади

**Приклад #1 Приклад використання** openssl\_spki\_new()\*\*\*\*

Створює новий SPKAC з використанням стандартного алгоритму (MD5)

```php
<?php
$pkey = openssl_pkey_new('secret password');
$spkac = openssl_spki_new($pkey, 'testing');

if ($spkac !== NULL) {
    echo $spkac;
} else {
    echo "Генерация SPKAC не удалась";
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
MIICRzCCAS8wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDM3V3sS4o4
mB9dczziRnjGAmSp+JwPrHoYMAFGvDNmZGyiWfU586X4BKs++BAj7e/FsAfno0Hd
hN9FwpCNFSox30L03nQvLYJE7f/WqigwBeMRT7Op/xvFks4sT70xP2HRYv4KqP9a
WRcKU6cFH8VxhFhqM2txEIxZKdFLaL28yT7bEDmcglf4JLDdgNMb9rET1dkgtKE6
dOaJHPGjf1uvnOH4YwkQr7n4sLUR3Kdbh0ZJAFuQVDZulo+LLzxBBkqJJcB6FhF+
oXCdHTKZnqAhpWDz+NXYytAmevab6IYm5TWPWsJUv1YKJA5lg2mXbbloIZlN9Mgc
i9fi03bdw+crAgMBAAEWB3Rlc3RpbmcwDQYJKoZIhvcNAQEEBQADggEBALyUvP/o
pPSoWBlorFyZ2RnGwKf9qMpE0q2IJP7G3oDR4LyK/m933DUiZ+YnqThrH/CWb4Ek
y5I3OCyl3S4wCuU1ibZZwDVwYShr5ELp0J9PEf7qMQZOhNsizoC7k+Czb2xB6hYW
sKfsfTKm3cXBtH3fdgc/Z1Z7VSWnAzYo38snqm72NTf5yFRnrQdphNNXi+kn1zHA
lxXRyFDXHOcYsOnwAWfyXFA4QDHQ0ezz0UoCY8gJXovcZb4GRYqOLUAsF2HcNboy
29WN8VqE29sL9QxVZFlwMcqyoLcNnyw38GvNvAGqSvzzbnEFP2MAQXJVe0H0hdp/
MML5G2iNVgNozAo=
```

### Дивіться також

-   [openssl\_spki\_verify()](function.openssl-spki-verify.md) \- Перевіряє підписаний відкритий ключ та виклик
-   [openssl\_spki\_export\_challenge()](function.openssl-spki-export-challenge.md) \- Експорт виклику, пов'язаного з підписаним ключем та викликом
-   [openssl\_spki\_export()](function.openssl-spki-export.md) \- Експорт відкритого ключа у форматі PEM із підписаного відкритого ключа з викликом
-   [openssl\_get\_md\_methods()](function.openssl-get-md-methods.md) \- Отримати список доступних методів хешування
-   [openssl\_csr\_new()](function.openssl-csr-new.md) \- Генерує CSR
-   [openssl\_csr\_sign()](function.openssl-csr-sign.md) \- Підписати CSR за допомогою іншого сертифіката (або ним же) та створити сертифікат
