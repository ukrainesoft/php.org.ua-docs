---
navigation:
  - gnupg.examples-clearsign.md: « Прозоре підписування тексту
  - function.gnupg-adddecryptkey.md: gnupg\_adddecryptkey »
  - index.md: PHP Manual
  - book.gnupg.md: GnuPG
title: GnuPG Функції
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GnuPG Функції

# Примітки

Цей модуль дозволяє використовувати зв'язок ключів поточного користувача. Зв'язка, як правило, розташована в ~/.gnupg/. Щоб вказати іншу папку, збережіть шлях до зв'язування ключів у змінному оточенні GNUPGHOME. Дивіться [putenv](function.putenv.md) для отримання додаткової інформації, як це зробити.

Деякі функції потребують специфікації ключа. Ця специфікація може бути всім, що стосується унікального ключа (ідентифікатор користувача, ідентифікатор ключа, відбитки пальців, ...). У цій документації використовується відбиток пальця у всіх прикладах.

> **Зауваження** :
> 
> Як альтернатива явно документованим функціям, що використовують resource, ви можете використовувати об'єктно-орієнтований стиль за допомогою об'єктів **gnupg**

## Зміст

-   [gnupg\_adddecryptkey](function.gnupg-adddecryptkey.md)— Додати ключ для розшифровки
-   [gnupg\_addencryptkey](function.gnupg-addencryptkey.md)— Додає ключ для шифрування
-   [gnupg\_addsignkey](function.gnupg-addsignkey.md)— Додати ключ для підписання
-   [gnupg\_cleardecryptkeys](function.gnupg-cleardecryptkeys.md)— Видаляє всі ключі, які були встановлені для розшифровки раніше
-   [gnupg\_clearencryptkeys](function.gnupg-clearencryptkeys.md)— Видаляє всі ключі, встановлені для шифрування раніше
-   [gnupg\_clearsignkeys](function.gnupg-clearsignkeys.md)— Видаляє всі ключі, які були встановлені для підписання раніше
-   [gnupg\_decrypt](function.gnupg-decrypt.md) \- Розшифровує переданий текст
-   [gnupg\_decryptverify](function.gnupg-decryptverify.md)— Розшифровує та перевіряє підпис переданого тексту
-   [gnupg\_deletekey](function.gnupg-deletekey.md)— Видаляє ключ із зв'язування ключів
-   [gnupg\_encrypt](function.gnupg-encrypt.md) \- Шифрує заданий текст
-   [gnupg\_encryptsign](function.gnupg-encryptsign.md)— Шифрує та підписує переданий текст
-   [gnupg\_export](function.gnupg-export.md) \- Експортує ключ
-   [gnupg\_getengineinfo](function.gnupg-getengineinfo.md)— Повертає інформацію про двигун
-   [gnupg\_geterror](function.gnupg-geterror.md)— Повертає текст повідомлення про помилку, якщо функція не була виконана
-   [gnupg\_geterrorinfo](function.gnupg-geterrorinfo.md)— Повертає інформацію про помилку
-   [gnupg\_getprotocol](function.gnupg-getprotocol.md)— Повертає активний протокол для всіх операцій.
-   [gnupg\_gettrustlist](function.gnupg-gettrustlist.md) \- Пошук довірчих елементів
-   [gnupg\_import](function.gnupg-import.md) \- Імпортує ключ
-   [gnupg\_init](function.gnupg-init.md) \- Ініціалізувати GnuPG
-   [gnupg\_keyinfo](function.gnupg-keyinfo.md)— Повертає масив з інформацією про всі ключі, які відповідають заданому шаблону
-   [gnupg\_listsignatures](function.gnupg-listsignatures.md) \- Перераховує підписи ключа
-   [gnupg\_setarmor](function.gnupg-setarmor.md)— Перемикає висновок у текстовому чи бінарному режимі
-   [gnupg\_seterrormode](function.gnupg-seterrormode.md)— Встановлює режим звітування про помилки (error\_reporting)
-   [gnupg\_setsignmode](function.gnupg-setsignmode.md)— Встановлює режим підписування
-   [gnupg\_sign](function.gnupg-sign.md)— Підписує переданий текст
-   [gnupg\_verify](function.gnupg-verify.md) \- Перевіряє підпис тексту
