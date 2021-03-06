- [« Вимоги](imap.requirements.md)
- [Налаштування під час виконання »](imap.configuration.md)

- [PHP Manual](index.md)
- [Встановлення та налаштування](imap.setup.md)
- Встановлення

## Установка

Щоб включити підтримку IMAP у збірку PHP, додайте конфігурацію
опцію **--with-imap[=DIR]**, де DIR це папка установки c-client. Для
нашого вищезгаданого прикладу ви повинні використовувати
**--with-imap=/usr/local/imap-2000b**. Цей шлях залежить від того, де ви
створили цю директорію відповідно до опису вище. Windows
користувачі можуть підключити `php_imap.dll` DLL у `php.ini`.

> **Примітка**: Залежно від того, як налаштований ваш c-client, вам
> може знадобитися додати **--with-imap-ssl=/path/to/openssl/**
> та/або **--with-kerberos=/path/to/kerberos** ключ при конфігуруванні
> PHP.

**Увага**

Модуль IMAP не є безпечним; його не слід використовувати зі
складаннями ZTS.

**Увага**
 Модуль [IMAP](book.imap.md) не може використовуватися разом із модулями
[перекодування](book.recode.md) та [YAZ](book.yaz.md). Це пов'язано з
тим фактом, що вони обидва використовують одні й самі внутрішні символи.
Примітка: Версії Yaz 2.0 і вище позбавлені цього недоліку.
