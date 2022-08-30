Нові глобальні константи

-   [« Нові функції](migration72.new-functions.html)
    
-   [Зміни, що ламають зворотну сумісність »](migration72.incompatible.html)
    
-   [PHP Manual](index.html)
    
-   [Миграция с PHP 7.1.x на PHP 7.2.x](migration72.html)
    
-   Нові глобальні константи
    

## Нові глобальні константи

### Ядро PHP

-   [**`PHP_FLOAT_DIG`**](reserved.constants.html#constant.php-float-dig)
-   [**`PHP_FLOAT_EPSILON`**](reserved.constants.html#constant.php-float-epsilon)
-   [**`PHP_FLOAT_MIN`**](reserved.constants.html#constant.php-float-min)
-   [**`PHP_FLOAT_MAX`**](reserved.constants.html#constant.php-float-max)
-   [**`PHP_OS_FAMILY`**](reserved.constants.html#constant.php-os-family)

### [Інформація про файл](book.fileinfo.html)

-   [**`FILEINFO_EXTENSION`**](fileinfo.constants.html#constant.fileinfo-extension)

### [JSON](book.json.html)

-   **`JSON_INVALID_UTF8_IGNORE`**
-   **`JSON_INVALID_UTF8_SUBSTITUTE`**

### [ДД](book.image.html)

-   [**`IMG_EFFECT_MULTIPLY`**](image.constants.html#constant.img-effect-multiply)
-   [**`IMG_BMP`**](image.constants.html#constant.img-bmp)

### [LDAP](book.ldap.html)

-   [**`LDAP_EXOP_START_TLS`**](ldap.constants.html#constant.ldap-exop-start-tls)
-   [**`LDAP_EXOP_MODIFY_PASSWD`**](ldap.constants.html#constant.ldap-exop-modify-passwd)
-   [**`LDAP_EXOP_REFRESH`**](ldap.constants.html#constant.ldap-exop-refresh)
-   [**`LDAP_EXOP_WHO_AM_I`**](ldap.constants.html#constant.ldap-exop-who-am-i)
-   [**`LDAP_EXOP_TURN`**](ldap.constants.html#constant.ldap-exop-turn)

### [Хеширование пароля](book.password.html)

-   [**`PASSWORD_ARGON2I`**](password.constants.html#constant.password-argon2i)
-   [**`PASSWORD_ARGON2_DEFAULT_MEMORY_COST`**](password.constants.html#constant.password-argon2-default-memory-cost)
-   [**`PASSWORD_ARGON2_DEFAULT_TIME_COST`**](password.constants.html#constant.password-argon2-default-time-cost)
-   [**`PASSWORD_ARGON2_DEFAULT_THREADS`**](password.constants.html#constant.password-argon2-default-threads)

### [PCRE](book.pcre.html)

-   **`PREG_UNMATCHED_AS_NULL`**

### [PDO](book.pdo.html)

-   [**`PDO::PARAM_STR_NATL`**](pdo.constants.html#pdo.constants.param-str-natl)
-   [**`PDO::PARAM_STR_CHAR`**](pdo.constants.html#pdo.constants.param-str-char)
-   [**`PDO::ATTR_DEFAULT_STR_PARAM`**](pdo.constants.html#pdo.constants.attr-default-str-param)

### [Sodium](book.sodium.html)

-   [**`SODIUM_LIBRARY_VERSION`**](sodium.constants.html#constant.sodium-library-version)
-   [**`SODIUM_LIBRARY_MAJOR_VERSION`**](sodium.constants.html#constant.sodium-library-major-version)
-   [**`SODIUM_LIBRARY_MINOR_VERSION`**](sodium.constants.html#constant.sodium-library-minor-version)
-   [**`SODIUM_CRYPTO_AEAD_AES256GCM_KEYBYTES`**](sodium.constants.html#constant.sodium-crypto-aead-aes256gcm-keybytes)
-   [**`SODIUM_CRYPTO_AEAD_AES256GCM_NSECBYTES`**](sodium.constants.html#constant.sodium-crypto-aead-aes256gcm-nsecbytes)
-   [**`SODIUM_CRYPTO_AEAD_AES256GCM_NPUBBYTES`**](sodium.constants.html#constant.sodium-crypto-aead-aes256gcm-npubbytes)
-   [**`SODIUM_CRYPTO_AEAD_AES256GCM_ABYTES`**](sodium.constants.html#constant.sodium-crypto-aead-aes256gcm-abytes)
-   [**`SODIUM_CRYPTO_AEAD_CHACHA20POLY1305_KEYBYTES`**](sodium.constants.html#constant.sodium-crypto-aead-chacha20poly1305-keybytes)
-   [**`SODIUM_CRYPTO_AEAD_CHACHA20POLY1305_NSECBYTES`**](sodium.constants.html#constant.sodium-crypto-aead-chacha20poly1305-nsecbytes)
-   [**`SODIUM_CRYPTO_AEAD_CHACHA20POLY1305_NPUBBYTES`**](sodium.constants.html#constant.sodium-crypto-aead-chacha20poly1305-npubbytes)
-   [**`SODIUM_CRYPTO_AEAD_CHACHA20POLY1305_ABYTES`**](sodium.constants.html#constant.sodium-crypto-aead-chacha20poly1305-abytes)
-   [**`SODIUM_CRYPTO_AEAD_CHACHA20POLY1305_IETF_KEYBYTES`**](sodium.constants.html#constant.sodium-crypto-aead-chacha20poly1305-ietf-keybytes)
-   [**`SODIUM_CRYPTO_AEAD_CHACHA20POLY1305_IETF_NSECBYTES`**](sodium.constants.html#constant.sodium-crypto-aead-chacha20poly1305-ietf-nsecbytes)
-   [**`SODIUM_CRYPTO_AEAD_CHACHA20POLY1305_IETF_NPUBBYTES`**](sodium.constants.html#constant.sodium-crypto-aead-chacha20poly1305-ietf-npubbytes)
-   [**`SODIUM_CRYPTO_AEAD_CHACHA20POLY1305_IETF_ABYTES`**](sodium.constants.html#constant.sodium-crypto-aead-chacha20poly1305-ietf-abytes)
-   [**`SODIUM_CRYPTO_AUTH_BYTES`**](sodium.constants.html#constant.sodium-crypto-auth-bytes)
-   [**`SODIUM_CRYPTO_AUTH_KEYBYTES`**](sodium.constants.html#constant.sodium-crypto-auth-keybytes)
-   [**`SODIUM_CRYPTO_BOX_SEALBYTES`**](sodium.constants.html#constant.sodium-crypto-box-sealbytes)
-   [**`SODIUM_CRYPTO_BOX_SECRETKEYBYTES`**](sodium.constants.html#constant.sodium-crypto-box-secretkeybytes)
-   [**`SODIUM_CRYPTO_BOX_PUBLICKEYBYTES`**](sodium.constants.html#constant.sodium-crypto-box-publickeybytes)
-   [**`SODIUM_CRYPTO_BOX_KEYPAIRBYTES`**](sodium.constants.html#constant.sodium-crypto-box-keypairbytes)
-   [**`SODIUM_CRYPTO_BOX_MACBYTES`**](sodium.constants.html#constant.sodium-crypto-box-macbytes)
-   [**`SODIUM_CRYPTO_BOX_NONCEBYTES`**](sodium.constants.html#constant.sodium-crypto-box-noncebytes)
-   [**`SODIUM_CRYPTO_BOX_SEEDBYTES`**](sodium.constants.html#constant.sodium-crypto-box-seedbytes)
-   [**`SODIUM_CRYPTO_KDF_BYTES_MIN`**](sodium.constants.html#constant.sodium-crypto-kdf-bytes-min)
-   [**`SODIUM_CRYPTO_KDF_BYTES_MAX`**](sodium.constants.html#constant.sodium-crypto-kdf-bytes-max)
-   [**`SODIUM_CRYPTO_KDF_CONTEXTBYTES`**](sodium.constants.html#constant.sodium-crypto-kdf-contextbytes)
-   [**`SODIUM_CRYPTO_KDF_KEYBYTES`**](sodium.constants.html#constant.sodium-crypto-kdf-keybytes)
-   [**`SODIUM_CRYPTO_KX_SEEDBYTES`**](sodium.constants.html#constant.sodium-crypto-kx-seedbytes)
-   [**`SODIUM_CRYPTO_KX_SESSIONKEYBYTES`**](sodium.constants.html#constant.sodium-crypto-kx-sessionkeybytes)
-   [**`SODIUM_CRYPTO_KX_PUBLICKEYBYTES`**](sodium.constants.html#constant.sodium-crypto-kx-publickeybytes)
-   [**`SODIUM_CRYPTO_KX_SECRETKEYBYTES`**](sodium.constants.html#constant.sodium-crypto-kx-secretkeybytes)
-   [**`SODIUM_CRYPTO_KX_KEYPAIRBYTES`**](sodium.constants.html#constant.sodium-crypto-kx-keypairbytes)
-   [**`SODIUM_CRYPTO_GENERICHASH_BYTES`**](sodium.constants.html#constant.sodium-crypto-generichash-bytes)
-   [**`SODIUM_CRYPTO_GENERICHASH_BYTES_MIN`**](sodium.constants.html#constant.sodium-crypto-generichash-bytes-min)
-   [**`SODIUM_CRYPTO_GENERICHASH_BYTES_MAX`**](sodium.constants.html#constant.sodium-crypto-generichash-bytes-max)
-   [**`SODIUM_CRYPTO_GENERICHASH_KEYBYTES`**](sodium.constants.html#constant.sodium-crypto-generichash-keybytes)
-   [**`SODIUM_CRYPTO_GENERICHASH_KEYBYTES_MIN`**](sodium.constants.html#constant.sodium-crypto-generichash-keybytes-min)
-   [**`SODIUM_CRYPTO_GENERICHASH_KEYBYTES_MAX`**](sodium.constants.html#constant.sodium-crypto-generichash-keybytes-max)
-   [**`SODIUM_CRYPTO_PWHASH_ALG_ARGON2I13`**](sodium.constants.html#constant.sodium-crypto-pwhash-alg-argon2i13)
-   [**`SODIUM_CRYPTO_PWHASH_ALG_DEFAULT`**](sodium.constants.html#constant.sodium-crypto-pwhash-alg-default)
-   [**`SODIUM_CRYPTO_PWHASH_SALTBYTES`**](sodium.constants.html#constant.sodium-crypto-pwhash-saltbytes)
-   [**`SODIUM_CRYPTO_PWHASH_STRPREFIX`**](sodium.constants.html#constant.sodium-crypto-pwhash-strprefix)
-   [**`SODIUM_CRYPTO_PWHASH_OPSLIMIT_INTERACTIVE`**](sodium.constants.html#constant.sodium-crypto-pwhash-opslimit-interactive)
-   [**`SODIUM_CRYPTO_PWHASH_MEMLIMIT_INTERACTIVE`**](sodium.constants.html#constant.sodium-crypto-pwhash-memlimit-interactive)
-   [**`SODIUM_CRYPTO_PWHASH_OPSLIMIT_MODERATE`**](sodium.constants.html#constant.sodium-crypto-pwhash-opslimit-moderate)
-   [**`SODIUM_CRYPTO_PWHASH_MEMLIMIT_MODERATE`**](sodium.constants.html#constant.sodium-crypto-pwhash-memlimit-moderate)
-   [**`SODIUM_CRYPTO_PWHASH_OPSLIMIT_SENSITIVE`**](sodium.constants.html#constant.sodium-crypto-pwhash-opslimit-sensitive)
-   [**`SODIUM_CRYPTO_PWHASH_MEMLIMIT_SENSITIVE`**](sodium.constants.html#constant.sodium-crypto-pwhash-memlimit-sensitive)
-   [**`SODIUM_CRYPTO_PWHASH_SCRYPTSALSA208SHA256_SALTBYTES`**](sodium.constants.html#constant.sodium-crypto-pwhash-scryptsalsa208sha256-saltbytes)
-   [**`SODIUM_CRYPTO_PWHASH_SCRYPTSALSA208SHA256_STRPREFIX`**](sodium.constants.html#constant.sodium-crypto-pwhash-scryptsalsa208sha256-strprefix)
-   [**`SODIUM_CRYPTO_PWHASH_SCRYPTSALSA208SHA256_OPSLIMIT_INTERACTIVE`**](sodium.constants.html#constant.sodium-crypto-pwhash-scryptsalsa208sha256-opslimit-interactive)
-   [**`SODIUM_CRYPTO_PWHASH_SCRYPTSALSA208SHA256_MEMLIMIT_INTERACTIVE`**](sodium.constants.html#constant.sodium-crypto-pwhash-scryptsalsa208sha256-memlimit-interactive)
-   [**`SODIUM_CRYPTO_PWHASH_SCRYPTSALSA208SHA256_OPSLIMIT_SENSITIVE`**](sodium.constants.html#constant.sodium-crypto-pwhash-scryptsalsa208sha256-opslimit-sensitive)
-   [**`SODIUM_CRYPTO_PWHASH_SCRYPTSALSA208SHA256_MEMLIMIT_SENSITIVE`**](sodium.constants.html#constant.sodium-crypto-pwhash-scryptsalsa208sha256-memlimit-sensitive)
-   [**`SODIUM_CRYPTO_SCALARMULT_BYTES`**](sodium.constants.html#constant.sodium-crypto-scalarmult-bytes)
-   [**`SODIUM_CRYPTO_SCALARMULT_SCALARBYTES`**](sodium.constants.html#constant.sodium-crypto-scalarmult-scalarbytes)
-   [**`SODIUM_CRYPTO_SHORTHASH_BYTES`**](sodium.constants.html#constant.sodium-crypto-shorthash-bytes)
-   [**`SODIUM_CRYPTO_SHORTHASH_KEYBYTES`**](sodium.constants.html#constant.sodium-crypto-shorthash-keybytes)
-   [**`SODIUM_CRYPTO_SECRETBOX_KEYBYTES`**](sodium.constants.html#constant.sodium-crypto-secretbox-keybytes)
-   [**`SODIUM_CRYPTO_SECRETBOX_MACBYTES`**](sodium.constants.html#constant.sodium-crypto-secretbox-macbytes)
-   [**`SODIUM_CRYPTO_SECRETBOX_NONCEBYTES`**](sodium.constants.html#constant.sodium-crypto-secretbox-noncebytes)
-   [**`SODIUM_CRYPTO_SIGN_BYTES`**](sodium.constants.html#constant.sodium-crypto-sign-bytes)
-   [**`SODIUM_CRYPTO_SIGN_SEEDBYTES`**](sodium.constants.html#constant.sodium-crypto-sign-seedbytes)
-   [**`SODIUM_CRYPTO_SIGN_PUBLICKEYBYTES`**](sodium.constants.html#constant.sodium-crypto-sign-publickeybytes)
-   [**`SODIUM_CRYPTO_SIGN_SECRETKEYBYTES`**](sodium.constants.html#constant.sodium-crypto-sign-secretkeybytes)
-   [**`SODIUM_CRYPTO_SIGN_KEYPAIRBYTES`**](sodium.constants.html#constant.sodium-crypto-sign-keypairbytes)
-   [**`SODIUM_CRYPTO_STREAM_NONCEBYTES`**](sodium.constants.html#constant.sodium-crypto-stream-noncebytes)
-   [**`SODIUM_CRYPTO_STREAM_KEYBYTES`**](sodium.constants.html#constant.sodium-crypto-stream-keybytes)

### [Zip](book.zip.html)

-   [**`ZipArchive::EM_NONE`**](zip.constants.html#ziparchive.constants.em-none)
-   [**`ZipArchive::EM_AES_128`**](zip.constants.html#ziparchive.constants.em-aez-128)
-   [**`ZipArchive::EM_AES_192`**](zip.constants.html#ziparchive.constants.em-aez-192)
-   [**`ZipArchive::EM_AES_256`**](zip.constants.html#ziparchive.constants.em-aes256)