Інші константи

-   [« Константа SNI (Server Name Indication)](openssl.constsni.md)
    
-   [Параметри ключа/сертифіката »](openssl.certparams.md)
    
-   [PHP Manual](index.md)
    
-   [Обумовлені константи](openssl.constants.md)
    
-   Інші константи
    

## Інші константи

**`OPENSSL_RAW_DATA`** (bool)

Якщо **`OPENSSL_RAW_DATA`** встановлена ​​в [opensslencrypt()](function.openssl-encrypt.html) або [openssldecrypt()](function.openssl-decrypt.html), дані, що повертаються, повертаються як є. Якщо константа не вказана, стороні, що викликає, повертаються дані в кодуванні Base64.

**`OPENSSL_ZERO_PADDING`** (bool)

За замовчуванням операції шифрування доповнюються стандартним заповненням блоку, а заповнення перевіряється та видаляється при дешифруванні. Якщо **`OPENSSL_ZERO_PADDING`** встановлений в `options` функції [opensslencrypt()](function.openssl-encrypt.html) або [openssldecrypt()](function.openssl-decrypt.html), то заповнення не виконується, загальний обсяг зашифрованих або розшифрованих даних повинен бути кратний розмір блоку, інакше виникне помилка.

**`OPENSSL_ENCODING_SMIME`** (int)

Вказує, що використовується кодування S/MIME.

**`OPENSSL_ENCODING_DER`** (int)

Вказує, що використовується кодування DER (Distinguished Encoding Rules).

**`OPENSSL_ENCODING_PEM`** (int)

Вказує, що використовується кодування PEM (Privacy-Enhanced Mail).