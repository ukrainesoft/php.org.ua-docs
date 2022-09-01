---
navigation:
  - phar.getsupportedcompression.html: '« Phar::getSupportedCompression'
  - phar.getversion.html: 'Phar::getVersion »'
  - index.html: PHP Manual
  - class.phar.html: Phar
title: 'Phar::getSupportedSignatures'
---
# Phar::getSupportedSignatures

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.1.0)

Phar::getSupportedSignatures — Отримати масив підтримуваних алгоритмів підпису архіву

### Опис

```methodsynopsis
final public static Phar::getSupportedSignatures(): array
```

Повертає масив підтримуваних алгоритмів підпису архіву

### Список параметрів

Без параметрів.

### Значення, що повертаються

Повертає масив приблизно такого змісту: `MD5` `SHA-1` `SHA-256` `SHA-512` `OpenSSL`

### Дивіться також

-   [Phar::getSignature()](phar.getsignature.md) - Отримати MD5/SHA1/SHA256/SHA512/OpenSSL підпис Phar-архіву
-   [Phar::setSignatureAlgorithm()](phar.setsignaturealgorithm.md) - Встановити алгоритм підписання phar-архіву та застосування його
