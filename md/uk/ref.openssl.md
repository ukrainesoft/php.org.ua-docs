Функції OpenSSL

-   [« Проверка сертификатов](openssl.cert.verification.html)
    
-   [openssl\_cipher\_iv\_length »](function.openssl-cipher-iv-length.html)
    
-   [PHP Manual](index.html)
    
-   [OpenSSL](book.openssl.html)
    
-   Функції OpenSSL
    

# Функції OpenSSL

## Зміст

-   [openssl\_cipher\_iv\_length](function.openssl-cipher-iv-length.html) — Отримує довжину вектора, що ініціалізує, шифру.
-   [openssl\_cms\_decrypt](function.openssl-cms-decrypt.html) — Розшифровує CMS-повідомлення
-   [openssl\_cms\_encrypt](function.openssl-cms-encrypt.html) — Зашифровує CMS-повідомлення
-   [openssl\_cms\_read](function.openssl-cms-read.html) — Експортує файл CMS до масиву сертифікатів PEM
-   [openssl\_cms\_sign](function.openssl-cms-sign.html) - Підписує файл
-   [openssl\_cms\_verify](function.openssl-cms-verify.html) — Перевіряє підпис CMS
-   [openssl\_csr\_export\_to\_file](function.openssl-csr-export-to-file.html) — Експортує CSR у файл
-   [openssl\_csr\_export](function.openssl-csr-export.html) — Експортує CSR у вигляді рядка
-   [openssl\_csr\_get\_public\_key](function.openssl-csr-get-public-key.html) — Повертає відкритий ключ CSR
-   [openssl\_csr\_get\_subject](function.openssl-csr-get-subject.html) — Повертає суб'єкт CSR
-   [openssl\_csr\_new](function.openssl-csr-new.html) - Генерує CSR
-   [openssl\_csr\_sign](function.openssl-csr-sign.html) — Підписати CSR за допомогою іншого сертифіката (або ним же) та створити сертифікат
-   [openssl\_decrypt](function.openssl-decrypt.html) - Розшифровує дані
-   [openssl\_dh\_compute\_key](function.openssl-dh-compute-key.html) — Обчислює загальний секретний ключ для віддаленого відкритого ключа DH і локального ключа DH
-   [openssl\_digest](function.openssl-digest.html) - Обчислення дайджесту
-   [openssl\_encrypt](function.openssl-encrypt.html) - Шифрує дані
-   [openssl\_error\_string](function.openssl-error-string.html) — Повертає повідомлення про помилку openSSL
-   [openssl\_free\_key](function.openssl-free-key.html) — Вивільнення ресурсу ключа
-   [openssl\_get\_cert\_locations](function.openssl-get-cert-locations.html) — Отримати доступні місця розташування сертифікатів
-   [openssl\_get\_cipher\_methods](function.openssl-get-cipher-methods.html) — Отримати список доступних алгоритмів шифрування
-   [openssl\_get\_curve\_names](function.openssl-get-curve-names.html) - Список доступних імен кривих для ECC
-   [openssl\_get\_md\_methods](function.openssl-get-md-methods.html) — Отримати список доступних методів хешування
-   [openssl\_get\_privatekey](function.openssl-get-privatekey.html) - Псевдонім opensslpkeygetprivate
-   [openssl\_get\_publickey](function.openssl-get-publickey.html) - Псевдонім opensslpkeygetpublic
-   [openssl\_open](function.openssl-open.html) — Відкрити запечатані дані
-   [openssl\_pbkdf2](function.openssl-pbkdf2.html) — Генерує рядки PKCS5 v2 PBKDF2
-   [openssl\_pkcs12\_export\_to\_file](function.openssl-pkcs12-export-to-file.html) — Експортує у сумісний із PKCS#12 файл сховища сертифікатів
-   [openssl\_pkcs12\_export](function.openssl-pkcs12-export.html) — Експортує сумісний із PKCS#12 файл сховища сертифікатів у змінну
-   [openssl\_pkcs12\_read](function.openssl-pkcs12-read.html) — Розбирає сховище сертифікатів PKCS#12 у масив
-   [openssl\_pkcs7\_decrypt](function.openssl-pkcs7-decrypt.html) — Розшифрувати повідомлення, зашифроване S/MIME
-   [openssl\_pkcs7\_encrypt](function.openssl-pkcs7-encrypt.html) — Шифрує повідомлення S/MIME
-   [openssl\_pkcs7\_read](function.openssl-pkcs7-read.html) — Експортувати файл PKCS7 до масиву сертифікатів PEM
-   [openssl\_pkcs7\_sign](function.openssl-pkcs7-sign.html) — Підписати повідомлення S/MIME
-   [openssl\_pkcs7\_verify](function.openssl-pkcs7-verify.html) — Перевірити підпис повідомлення S/MIME
-   [openssl\_pkey\_derive](function.openssl-pkey-derive.html) — Обчислює загальний секрет відкритого значення віддаленого та локального ключа DH або ECDH
-   [openssl\_pkey\_export\_to\_file](function.openssl-pkey-export-to-file.html) — Записує у файл ключ у форматі PEM
-   [openssl\_pkey\_export](function.openssl-pkey-export.html) — Отримує рядок із ключем у форматі PEM
-   [openssl\_pkey\_free](function.openssl-pkey-free.html) — Визволяє ресурс закритого ключа
-   [openssl\_pkey\_get\_details](function.openssl-pkey-get-details.html) — Отримує масив із детальною інформацією про ключ
-   [openssl\_pkey\_get\_private](function.openssl-pkey-get-private.html) — Отримати закритий ключ
-   [openssl\_pkey\_get\_public](function.openssl-pkey-get-public.html) — Витягує відкритий ключ із сертифіката та готує його до використання.
-   [openssl\_pkey\_new](function.openssl-pkey-new.html) - Генерує новий закритий ключ
-   [openssl\_private\_decrypt](function.openssl-private-decrypt.html) — Розшифровує дані за допомогою закритого ключа
-   [openssl\_private\_encrypt](function.openssl-private-encrypt.html) - Шифрує дані секретним ключем
-   [openssl\_public\_decrypt](function.openssl-public-decrypt.html) — Розшифрування даних за допомогою відкритого ключа
-   [openssl\_public\_encrypt](function.openssl-public-encrypt.html) - Шифрування даних відкритим ключем
-   [openssl\_random\_pseudo\_bytes](function.openssl-random-pseudo-bytes.html) - Генерує псевдовипадкову послідовність байт
-   [openssl\_seal](function.openssl-seal.html) - Запечатати (зашифрувати) дані
-   [openssl\_sign](function.openssl-sign.html) - Генерація підпису
-   [openssl\_spki\_export\_challenge](function.openssl-spki-export-challenge.html) — Експорт дзвінка, пов'язаного з підписаним ключем та дзвінком
-   [openssl\_spki\_export](function.openssl-spki-export.html) — Експорт відкритого ключа у форматі PEM із підписаного відкритого ключа з викликом
-   [openssl\_spki\_new](function.openssl-spki-new.html) — Створення нового відкритого підписаного ключа з викликом
-   [openssl\_spki\_verify](function.openssl-spki-verify.html) — Перевіряє підписаний відкритий ключ та виклик
-   [openssl\_verify](function.openssl-verify.html) - Звіряння сигнатури
-   [openssl\_x509\_check\_private\_key](function.openssl-x509-check-private-key.html) — Перевірити, чи секретний ключ відноситься до сертифіката
-   [openssl\_x509\_checkpurpose](function.openssl-x509-checkpurpose.html) — Перевіряє, чи можна використовувати сертифікат для конкретних завдань
-   [openssl\_x509\_export\_to\_file](function.openssl-x509-export-to-file.html) — Експортує сертифікат у файл
-   [openssl\_x509\_export](function.openssl-x509-export.html) — Експортує сертифікат у рядок
-   [openssl\_x509\_fingerprint](function.openssl-x509-fingerprint.html) - Обчислює відбиток або дайджест, заданий сертифікатом X.509
-   [openssl\_x509\_free](function.openssl-x509-free.html) — Вивільняє ресурс сертифіката
-   [openssl\_x509\_parse](function.openssl-x509-parse.html) — Розібрати сертифікат X509 та отримати масив із даними про нього
-   [openssl\_x509\_read](function.openssl-x509-read.html) — Розібрати сертифікат X.509 та повернути для нього об'єкт
-   [openssl\_x509\_verify](function.openssl-x509-verify.html) — Перевірити цифровий підпис сертифіката x509 за допомогою публічного ключа