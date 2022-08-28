Встановлення

-   [« Требования](curl.requirements.html)
    
-   [Настройка во время выполнения »](curl.configuration.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](curl.setup.html)
    
-   Встановлення
    

## Встановлення

Для використання cURL необхідно зібрати PHP з опцією **\-with-curl=DIR**де DIR - ім'я каталогу, що містить підкаталоги lib і include. Каталог include повинен містити підкаталог curl із файлами easy.h та curl.h. У каталозі lib має бути файл libcurl.a.

> **Зауваження** **Примітка для користувачів Win32**  
> Для роботи з цим модулем у Windows файли libeay32.dll та ssleay32.dll, або, починаючи з OpenSSL 1.1, libcrypto-.dll і libssl-.dll, повинні існувати в системної змінної оточення PATH. Також libssh2.dll повинен бути присутнім у вашому змінному оточенні PATH. Вам не потрібно файл libcurl.dll із сайту cURL.