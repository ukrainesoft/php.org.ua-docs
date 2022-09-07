---
navigation:
  - openssl.cms.flags.md: « Прапори/Константи CMS
  - openssl.ciphers.md: Алгоритми шифрування »
  - index.md: PHP Manual
  - openssl.constants.md: Обумовлені константи
title: Алгоритми підпису
---
## Алгоритми підпису

**`OPENSSL_ALGO_DSS1`** (int)

**`OPENSSL_ALGO_SHA1`** (int)

Використовується як алгоритм за замовчуванням для функцій [opensslsign()](function.openssl-sign.md) і [opensslverify()](function.openssl-verify.md)

**`OPENSSL_ALGO_SHA224`** (int)

**`OPENSSL_ALGO_SHA256`** (int)

**`OPENSSL_ALGO_SHA384`** (int)

**`OPENSSL_ALGO_SHA512`** (int)

**`OPENSSL_ALGO_RMD160`** (int)

**`OPENSSL_ALGO_MD5`** (int)

**`OPENSSL_ALGO_MD4`** (int)

**`OPENSSL_ALGO_MD2`** (int)

Ця константа доступна, лише якщо PHP скомпільовано за допомогою MD2. Для цього потрібно передати до -DHAVEOPENSSLMD2H CFLAG під час компіляції PHP і включити md2 під час компіляції OpenSSL 1.0.0+.
