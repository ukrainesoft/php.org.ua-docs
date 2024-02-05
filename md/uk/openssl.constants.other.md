---
navigation:
  - openssl.constsni.md: Константа SNI (Server Name Indication)
  - openssl.certparams.md: Параметри ключа/сертифіката »
  - index.md: PHP Manual
  - openssl.constants.md: Обумовлені константи
title: Інші константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Інші константи

**`OPENSSL_RAW_DATA`**(bool)

Если константа\*\*`OPENSSL_RAW_DATA`\*\*передана в функции[openssl\_encrypt()](function.openssl-encrypt.md) або [openssl\_decrypt()](function.openssl-decrypt.md), дані повертаються як є. Якщо константа не вказана, стороні, що викликає, повертаються дані в кодуванні Base64.

**`OPENSSL_ZERO_PADDING`**(bool)

За замовчуванням операції шифрування доповнюються стандартним заповненням блоку, а заповнення перевіряється та видаляється при дешифруванні. Якщо константа \*\*`OPENSSL_ZERO_PADDING`\*\*передана в параметр`options`функций[openssl\_encrypt()](function.openssl-encrypt.md) або [openssl\_decrypt()](function.openssl-decrypt.md), то заповнення не виконується, загальний обсяг зашифрованих або розшифрованих даних повинен бути кратний розмір блоку, інакше виникне помилка.

**`OPENSSL_ENCODING_SMIME`**(int)

Вказує, що вибрано кодування S/MIME.

**`OPENSSL_ENCODING_DER`**(int)

Вказує, що вибрано кодування DER (Distinguished Encoding Rules).

**`OPENSSL_ENCODING_PEM`**(int)

Вказує, що вибрано кодування PEM (Privacy-Enhanced Mail).
