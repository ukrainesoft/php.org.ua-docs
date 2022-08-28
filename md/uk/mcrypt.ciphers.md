Шифри Mcrypt

-   [« Предопределённые константы](mcrypt.constants.html)
    
-   [Mcrypt »](ref.mcrypt.html)
    
-   [PHP Manual](index.html)
    
-   [Mcrypt](book.mcrypt.html)
    
-   Шифри Mcrypt
    

# Шифри Mcrypt

Тут перераховані шифри, що підтримуються модулем mcrypt. Для повного списку шифрів, що підтримуються, дивіться список в кінці файлу mcrypt.h. Головне правило API mcrypt-2.2.x API полягає в тому, що доступ до шифрів з PHP здійснюється шляхом використання констант MCRYPTім'яшифру. Ці константи також працюють з AI libmcrypt-2.4.x та libmcrypt-2.5.x, але також можна задати шифр на ім'я за допомогою функції [mcrypt\_module\_open()](function.mcrypt-module-open.html)

-   MCRYPT3DES
-   MCRYPTARCFOURIV (тільки для libmcrypt > 2.4.x)
-   MCRYPTARCFOUR (тільки для libmcrypt > 2.4.x)
-   MCRYPTBLOWFISH
-   MCRYPTCAST
-   MCRYPTCAST
-   MCRYPTCRYPT
-   MCRYPTDES
-   MCRYPTDESCOMPAT (тільки для libmcrypt 2.2.x)
-   MCRYPTENIGMA (тільки для libmcrypt > 2.4.x, псевдонім для MCRYPTCRYPT)
-   MCRYPTGOST
-   MCRYPTIDEA (не вільний)
-   MCRYPTLOKI97 (тільки для libmcrypt > 2.4.x)
-   MCRYPTMARS (тільки для libmcrypt > 2.4.x, не вільний)
-   MCRYPTPANAMA (тільки для libmcrypt > 2.4.x)
-   MCRYPTRIJNDAEL128 (тільки для libmcrypt > 2.4.x)
-   MCRYPTRIJNDAEL192 (тільки для libmcrypt > 2.4.x)
-   MCRYPTRIJNDAEL256 (тільки для libmcrypt > 2.4.x)
-   MCRYPTRC2
-   MCRYPTRC4 (тільки для libmcrypt 2.2.x)
-   MCRYPTRC6 (тільки для libmcrypt > 2.4.x)
-   MCRYPTRC6128 (тільки для libmcrypt 2.2.x)
-   MCRYPTRC6192 (тільки для libmcrypt 2.2.x)
-   MCRYPTRC6256 (тільки для libmcrypt 2.2.x)
-   MCRYPTSAFER64
-   MCRYPTSAFER128
-   MCRYPTSAFERPLUS (лише для libmcrypt > 2.4.x)
-   MCRYPTSERPENT(тільки для libmcrypt > 2.4.x)
-   MCRYPTSERPENT128 (тільки для libmcrypt 2.2.x)
-   MCRYPTSERPENT192 (тільки для libmcrypt 2.2.x)
-   MCRYPTSERPENT256 (тільки для libmcrypt 2.2.x)
-   MCRYPTSKIPJACK (лише для libmcrypt > 2.4.x)
-   MCRYPTTEAN (тільки для libmcrypt 2.2.x)
-   MCRYPTTHREEWAY
-   MCRYPTTRIPLEDES (тільки для libmcrypt > 2.4.x)
-   MCRYPTTWOFISH (для старих версій mcrypt 2.x або mcrypt > 2.4.x)
-   MCRYPTTWOFISH128 (TWOFISHxxx доступний у нових версіях 2.x, але не в 2.4.x)
-   MCRYPTTWOFISH192
-   MCRYPTTWOFISH256
-   MCRYPTWAKE (тільки для libmcrypt > 2.4.x)
-   MCRYPTXTEA (тільки для libmcrypt > 2.4.x)

Ви повинні (у режимах **`CFB`** і **`OFB`**) або можете (у режимі **`CBC`**) надати ініціалізуючий вектор (IV) для обраної функції шифрування. IV має бути унікальним і має бути однаковим для шифрування та дешифрування. Для даних, які зберігаються в шифрованому вигляді, ви можете отримати висновок функції для індексу, під яким дані були збережені (наприклад, MD5 хеш імені файлу). Або ви можете передати IV разом із зашифрованими даними (див. розділ 9.3 Applied Cryptography by Schneier (ISBN 0-471-11709-9)).