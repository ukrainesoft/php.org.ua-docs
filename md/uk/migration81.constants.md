---
navigation:
  - migration81.new-functions.html: « Нові функції
  - migration81.incompatible.html: 'Зміни, що ламають зворотну сумісність »'
  - index.html: PHP Manual
  - migration81.html: Миграция с PHP 8.0.x на PHP 8.1.x
title: Нові глобальні константи
---
## Нові глобальні константи

### CURL

-   **`CURLOPT_DOH_URL`**
-   **`CURLOPT_ISSUERCERT_BLOB`**
-   **`CURLOPT_PROXY_ISSUERCERT`**
-   **`CURLOPT_PROXY_ISSUERCERT_BLOB`**
-   **`CURLOPT_PROXY_SSLCERT_BLOB`**
-   **`CURLOPT_PROXY_SSLKEY_BLOB`**
-   **`CURLOPT_SSLCERT_BLOB`**
-   **`CURLOPT_SSLKEY_BLOB`**

### ДД

-   **`IMG_AVIF`**
-   **`IMG_WEBP_LOSSLESS`**

### MySQLi

-   **`MYSQLI_REFRESH_REPLICA`**
    
    Ця нова константа була додана для заміни **`MYSQLI_REFRESH_SLAVE`** відповідно до політики самого MySQL, який відмовився від слова "slave". Стара константа, як і раніше, доступна для зворотної сумісності, але може бути оголошена застарілою/видалена в майбутньому.
    

### PCNTL

-   **`PRIO_DARWIN_BG`**
-   **`PRIO_DARWIN_THREAD`**

### POSIX

-   **`POSIX_RLIMIT_KQUEUES`**
-   **`POSIX_RLIMIT_NPTS`**

### Сокети

Доступні такі параметри сокету за умови, що вони підтримуються в системі:

-   **`SO_ACCEPTFILTER`**
-   **`SO_DONTTRUNC`**
-   **`SO_WANTMORE`**
-   **`SO_MARK`**
-   **`TCP_DEFER_ACCEPT`**

### Sodium

-   **`SODIUM_CRYPTO_STREAM_XCHACHA20_NONCEBYTES`**
-   **`SODIUM_CRYPTO_STREAM_XCHACHA20_KEYBYTES`**
-   **`SODIUM_CRYPTO_SCALARMULT_RISTRETTO255_BYTES`**
-   **`SODIUM_CRYPTO_SCALARMULT_RISTRETTO255_SCALARBYTES`**
-   **`SODIUM_CRYPTO_CORE_RISTRETTO255_BYTES`**
-   **`SODIUM_CRYPTO_CORE_RISTRETTO255_HASHBYTES`**
-   **`SODIUM_CRYPTO_CORE_RISTRETTO255_SCALARBYTES`**
-   **`SODIUM_CRYPTO_CORE_RISTRETTO255_NONREDUCEDSCALARBYTES`**

### Лексер (Tokenizer)

-   **`T_READONLY`**
