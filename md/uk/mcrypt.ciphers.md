---
navigation:
  - mcrypt.constants.md: « Зумовлені константи
  - ref.mcrypt.md: Mcrypt »
  - index.md: PHP Manual
  - book.mcrypt.md: Mcrypt
title: Шифри Mcrypt
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Шифри Mcrypt

Тут перелічені шифри, що підтримуються модулем mcrypt. Для повного списку шифрів, що підтримуються, дивіться список в кінці файлу mcrypt.h. Головне правило API mcrypt-2.2.x API полягає в тому, що доступ до шифрів з PHP здійснюється шляхом використання констант MCRYPT\_ім'я\_шифру. Ці константи також працюють з AI libmcrypt-2.4.x та libmcrypt-2.5.x, але також можна задати шифр на ім'я за допомогою функції [mcrypt\_module\_open()](function.mcrypt-module-open.md)

-   MCRYPT\_3DES
-   MCRYPT\_ARCFOUR\_IV (тільки для libmcrypt > 2.4.x)
-   MCRYPT\_ARCFOUR (тільки для libmcrypt > 2.4.x)
-   MCRYPT\_BLOWFISH
-   MCRYPT\_CAST\_128
-   MCRYPT\_CAST\_256
-   MCRYPT\_CRYPT
-   MCRYPT\_DES
-   MCRYPT\_DES\_COMPAT (тільки для libmcrypt 2.2.x)
-   MCRYPT\_ENIGMA (тільки для libmcrypt > 2.4.x, псевдонім для MCRYPT\_CRYPT)
-   MCRYPT\_GOST
-   MCRYPT\_IDEA (не вільний)
-   MCRYPT\_LOKI97 (тільки для libmcrypt > 2.4.x)
-   MCRYPT\_MARS (тільки для libmcrypt > 2.4.x, не вільний)
-   MCRYPT\_PANAMA (тільки для libmcrypt > 2.4.x)
-   MCRYPT\_RIJNDAEL\_128 (тільки для libmcrypt > 2.4.x)
-   MCRYPT\_RIJNDAEL\_192 (тільки для libmcrypt > 2.4.x)
-   MCRYPT\_RIJNDAEL\_256 (тільки для libmcrypt > 2.4.x)
-   MCRYPT\_RC2
-   MCRYPT\_RC4 (тільки для libmcrypt 2.2.x)
-   MCRYPT\_RC6 (тільки для libmcrypt > 2.4.x)
-   MCRYPT\_RC6\_128 (тільки для libmcrypt 2.2.x)
-   MCRYPT\_RC6\_192 (тільки для libmcrypt 2.2.x)
-   MCRYPT\_RC6\_256 (тільки для libmcrypt 2.2.x)
-   MCRYPT\_SAFER64
-   MCRYPT\_SAFER128
-   MCRYPT\_SAFERPLUS (лише для libmcrypt > 2.4.x)
-   MCRYPT\_SERPENT(тільки для libmcrypt > 2.4.x)
-   MCRYPT\_SERPENT\_128 (тільки для libmcrypt 2.2.x)
-   MCRYPT\_SERPENT\_192 (тільки для libmcrypt 2.2.x)
-   MCRYPT\_SERPENT\_256 (тільки для libmcrypt 2.2.x)
-   MCRYPT\_SKIPJACK (тільки для libmcrypt > 2.4.x)
-   MCRYPT\_TEAN (тільки для libmcrypt 2.2.x)
-   MCRYPT\_THREEWAY
-   MCRYPT\_TRIPLEDES (тільки для libmcrypt > 2.4.x)
-   MCRYPT\_TWOFISH (для старих версій mcrypt 2.x або mcrypt > 2.4.x)
-   MCRYPT\_TWOFISH128 (TWOFISHxxx доступний у нових версіях 2.x, але не в 2.4.x)
-   MCRYPT\_TWOFISH192
-   MCRYPT\_TWOFISH256
-   MCRYPT\_WAKE (тільки для libmcrypt > 2.4.x)
-   MCRYPT\_XTEA (тільки для libmcrypt > 2.4.x)

Ви повинні (у режимах **`CFB`** і **`OFB`**) або можете (у режимі **`CBC`**) надати ініціалізуючий вектор (IV) для обраної функції шифрування. IV має бути унікальним і має бути однаковим для шифрування та дешифрування. Для даних, які зберігаються в шифрованому вигляді, ви можете отримати висновок функції для індексу, під яким дані були збережені (наприклад, MD5 хеш імені файлу). Або ви можете передати IV разом із зашифрованими даними (див. розділ 9.3 Applied Cryptography by Schneier (ISBN 0-471-11709-9)).
