---
navigation:
  - curl.requirements.md: « Вимоги
  - curl.configuration.md: Налаштування під час виконання »
  - index.md: PHP Manual
  - curl.setup.md: Встановлення та налаштування
title: Установка
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Установка

Для використання cURL необхідно зібрати PHP з опцією \*\*--with-curl\[=DIR\]\*\*де DIR - ім'я каталогу, що містить підкаталоги lib і include. Каталог include повинен містити підкаталог curl із файлами easy.h та curl.h. У каталозі lib має бути файл libcurl.a.

> **Зауваження** **Примітка для користувачів Win32**  
> Для роботи з цим модулем у Windows файли libeay32.dll та ssleay32.dll, або, починаючи з OpenSSL 1.1, libcrypto-\*.dll і libssl-\*.dll повинні існувати в системній змінній оточенні PATH. Також libssh2.dll повинен бути присутнім у вашому змінному оточенні PATH. Вам не потрібно файл libcurl.dll із сайту cURL.
