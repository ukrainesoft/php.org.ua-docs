- [« Встановлення та налаштування](mail.setup.md)
- [Установка »](mail.installation.md)

- [PHP Manual](index.md)
- [Встановлення та налаштування](mail.setup.md)
- Вимоги

## Вимоги

Для роботи функцій Mail PHP повинен мати доступ до бінарних файлів
`sendmail` у вашій системі під час компіляції. Якщо ви використовуєте
іншу поштову програму, таку як qmail або postfix, ви маєте бути
впевнені, що використовуєте відповідні обгортки sendmail, що постачаються
із цими продуктами. PHP буде в першу чергу шукати файли sendmail по
шляхи в змінній оточенні `PATH`, і далі:
`/usr/bin:/usr/sbin:/usr/etc:/etc:/usr/ucblib:/usr/lib`. Дуже
рекомендується мати sendmail доступним із змінної оточення `PATH`.
Також, користувач під ким був скомпільований PHP повинен мати доступ до
бінарних файлів sendmail.
