Алгоритми підпису

-   [« Флаги/Константы CMS](openssl.cms.flags.html)
    
-   [Алгоритмы шифрования »](openssl.ciphers.html)
    
-   [PHP Manual](index.html)
    
-   [Предопределённые константы](openssl.constants.html)
    
-   Алгоритми підпису
    

## Алгоритми підпису

**`OPENSSL_ALGO_DSS1`** (int)

**`OPENSSL_ALGO_SHA1`** (int)

Використовується як алгоритм за замовчуванням для функцій [opensslsign()](function.openssl-sign.html) і [opensslverify()](function.openssl-verify.html)

**`OPENSSL_ALGO_SHA224`** (int)

**`OPENSSL_ALGO_SHA256`** (int)

**`OPENSSL_ALGO_SHA384`** (int)

**`OPENSSL_ALGO_SHA512`** (int)

**`OPENSSL_ALGO_RMD160`** (int)

**`OPENSSL_ALGO_MD5`** (int)

**`OPENSSL_ALGO_MD4`** (int)

**`OPENSSL_ALGO_MD2`** (int)

Ця константа доступна, лише якщо PHP скомпільовано за допомогою MD2. Для цього потрібно передати до -DHAVEOPENSSLMD2H CFLAG під час компіляції PHP і включити md2 під час компіляції OpenSSL 1.0.0+.