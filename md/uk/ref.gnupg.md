GnuPG Функції

-   [« Прозоре підписування тексту](gnupg.examples-clearsign.html)
    
-   [gnupgadddecryptkey »](function.gnupg-adddecryptkey.html)
    
-   [PHP Manual](index.md)
    
-   [GnuPG](book.gnupg.md)
    
-   GnuPG Функції
    

# GnuPG Функції

# Примітки

Цей модуль дозволяє використовувати зв'язок ключів поточного користувача. Зв'язка, як правило, розташована в ~/.gnupg/. Щоб вказати іншу папку, збережіть шлях до зв'язування ключів у змінному оточенні GNUPGHOME. Дивіться [putenv](function.putenv.md) для отримання додаткової інформації, як це зробити.

Деякі функції потребують специфікації ключа. Ця специфікація може бути всім, що стосується унікального ключа (ідентифікатор користувача, ідентифікатор ключа, відбитки пальців, ...). У цій документації використовується відбиток пальця у всіх прикладах.

> **Зауваження**
> 
> Як альтернатива явно документованим функціям, що використовують resource, ви можете використовувати об'єктно-орієнтований стиль за допомогою об'єктів **gnupg**

## Зміст

-   [gnupgadddecryptkey](function.gnupg-adddecryptkey.html) — Додати ключ для розшифровки
-   [gnupgaddencryptkey](function.gnupg-addencryptkey.html) — Додає ключ для шифрування
-   [gnupgaddsignkey](function.gnupg-addsignkey.html) — Додати ключ для підписання
-   [gnupgcleardecryptkeys](function.gnupg-cleardecryptkeys.html) — Видаляє всі ключі, які були встановлені для розшифровки раніше
-   [gnupgclearencryptkeys](function.gnupg-clearencryptkeys.html) — Видаляє всі ключі, які були встановлені для шифрування раніше
-   [gnupgclearsignkeys](function.gnupg-clearsignkeys.html) — Видаляє всі ключі, які були встановлені для підписання раніше
-   [gnupgdecrypt](function.gnupg-decrypt.html) - Розшифровує переданий текст
-   [gnupgdecryptverify](function.gnupg-decryptverify.html) — Розшифровує та перевіряє підпис переданого тексту
-   [gnupgdeletekey](function.gnupg-deletekey.html) — Видаляє ключ із зв'язування ключів
-   [gnupgencrypt](function.gnupg-encrypt.html) - Шифрує заданий текст
-   [gnupgencryptsign](function.gnupg-encryptsign.html) — Шифрує та підписує переданий текст
-   [gnupgexport](function.gnupg-export.html) - Експортує ключ
-   [gnupggetengineinfo](function.gnupg-getengineinfo.html) — Повертає інформацію про двигун
-   [gnupggeterror](function.gnupg-geterror.html) — Повертає текст повідомлення про помилку, якщо функція не була виконана
-   [gnupggeterrorinfo](function.gnupg-geterrorinfo.html) — Повертає інформацію про помилку
-   [gnupggetprotocol](function.gnupg-getprotocol.html) — Повертає активний протокол для всіх операцій.
-   [gnupggettrustlist](function.gnupg-gettrustlist.html) - Пошук довірчих елементів
-   [gnupgimport](function.gnupg-import.html) - Імпортує ключ
-   [gnupginit](function.gnupg-init.html) - Ініціалізувати GnuPG
-   [gnupgkeyinfo](function.gnupg-keyinfo.html) — Повертає масив з інформацією про всі ключі, які відповідають заданому шаблону
-   [gnupglistsignatures](function.gnupg-listsignatures.html) - Перераховує підписи ключа
-   [gnupgsetarmor](function.gnupg-setarmor.html) — Перемикає висновок у текстовому чи бінарному режимі
-   [gnupgseterrormode](function.gnupg-seterrormode.html) — Встановлює режим звітування про помилки (errorreporting)
-   [gnupgsetsignmode](function.gnupg-setsignmode.html) — Встановлює режим підписування
-   [gnupgsign](function.gnupg-sign.html) — Підписує переданий текст
-   [gnupgverify](function.gnupg-verify.html) - Перевіряє підпис тексту