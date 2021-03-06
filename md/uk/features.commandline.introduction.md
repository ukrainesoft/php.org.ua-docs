- [« Використання PHP у командному рядку](features.commandline.md)
- [Основні відмінності від інших реалізацій SAPI »](features.commandline.differences.md)

- [PHP Manual](index.md)
- [Використання PHP у командному рядку](features.commandline.md)
-   Вступ

## Вступ

Основна мета цього CLI SAPI – розробка консольних додатків на PHP.
Є досить багато відмінностей між CLI SAPI та іншими видами SAPI,
які будуть розглянуті у цьому розділі. Варто зазначити, що CLI SAPI та
CGI - різні SAPI-інтерфейси, хоча у поведінці багато спільного.

CLI SAPI включається за замовчуванням за допомогою **--enable-cli**, але
може бути вимкнено опцією **--disable-cli** при запуску
**./configure**.

Ім'я, розташування та існування бінарних модулів CLI/CGI залежить від
того, як саме встановлено PHP у вашій системі. За замовчуванням при
виконанні **make** створюється як CGI-, так і CLI-модуль, розміщені в
директоріях `sapi/cgi/php-cgi` та `sapi/cli/php` відповідно, всередині
директорії з вихідними кодами PHP. Слід зазначити, що обидва файли мають
однакова назва: `php`. Що станеться під час виконання **make
install**, залежить від того, які опції ви вказали на стадії
конфігурування. Якщо вибрано модуль SAPI під час виконання, наприклад,
apxs, або використовується опція **--disable-cgi**, модуль CLI буде
скопійований в `{PREFIX}/bin/php` при виконанні **make install**,
інакше буде скопійовано CGI-модуль. Наприклад, якщо задана
опція **--with-apxs**, то при виконанні **make install** CLI-версія
буде скопійована в `{PREFIX}/bin/php`. Якщо ви хочете перевизначити
установку CGI-модуль, використовуйте **make install-cli** після виконання
**make install**. Як альтернативу ви могли б вказати опцію
**--disable-cgi** у рядку конфігурації.

> **Примітка**:
>
> Оскільки обидві опції, **--enable-cli** та **--enable-cgi**, включені за
> замовчуванням, просто наявність **--enable-cli** у команді конфігурації
> необов'язково означає, що CLI буде скопійовано в `{PREFIX}/bin/php`
> під час виконання **make install**.

Бінарний файл CLI входить до дистрибутиву для Windows в основній папці в
як файл `php.exe`. CGI-версія знаходиться у файлі `php-cgi.exe`.
Крім того, до дистрибутиву входить файл `php-win.exe`, якщо PHP був
налаштований за допомогою **--enable-cli-win32**. Він повністю
еквівалентний CLI-версії, за винятком того, що абсолютно нічого не
виводить, і, таким чином, не надає консоль (вікно терміналу не
з'являється на екрані).

> **Примітка**: **Який варіант SAPI встановлено?**
>
> Виконайте з командного рядка **php -v** для отримання інформації про
> тому, чи є `php` CGI або CLI. Також ви можете використати
> функцію [php_sapi_name()](function.php-sapi-name.md) або константу
> **`PHP_SAPI`**.

> **Примітка**:
>
> Відповідну сторінку керівництва (`man`) Unix можна переглянути з
> за допомогою команди **man php** у консолі.
