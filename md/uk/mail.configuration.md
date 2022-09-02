---
navigation:
  - mail.installation.md: « Установка
  - mail.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - mail.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Конфігураційні опції надсилання листів**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [mail.addзheader](mail.configuration.md#ini.mail.add-x-header) | "0" | PHPINIPERDIR |  |
| [mail.log](mail.configuration.md#ini.mail.log) | NULL | PHPINISYSTEM | PHPINIPERDIR |
| [mail.forceextraparameters](mail.configuration.md#ini.mail.force_extra_parameters) | NULL | PHPINISYSTEM | PHPINIPERDIR |
| [SMTP](mail.configuration.md#ini.smtp) | "localhost" | PHPINIALL |  |
| [smtpport](mail.configuration.md#ini.smtp-port) | "25" | PHPINIALL |  |
| [sendmailfrom](mail.configuration.md#ini.sendmail-from) | NULL | PHPINIALL |  |
| [sendmailpath](mail.configuration.md#ini.sendmail-path) | "/usr/sbin/sendmail -t -i" | PHPINISYSTEM |  |

Для детального опису констант PHPINI, зверніться до розділу [Де можуть бути встановлені параметри конфігурації](configuration.changes.modes.md)

Коротке пояснення конфігураційних директив.

`mail.add_x_header` bool

Додає заголовок `X-PHP-Originating-Script`, який міститиме UID скрипта та ім'я файлу.

`mail.log` string

Шлях до лог-файлу, в який будуть записуватись всі виклики функції [mail()](function.mail.md). Записи в лозі містять повний шлях до скрипту, номер рядка, адреса одержувача `To` та заголовки.

`mail.force_extra_parameters` string

Примусово додати зазначені параметри для надсилання до sendmail. Ці параметри завжди замінюють значення п'ятого параметра в [mail()](function.mail.md), навіть у безпечному режимі.

`SMTP` string

Використовується лише у Windows: домен або IP-адреса SMTP-сервера, до якого буде звертатися PHP під час надсилання пошти функцією [mail()](function.mail.md)

`smtp_port` int

Використовується лише у Windows: порт `SMTP`сервера, до якого буде звертатися PHP під час надсилання пошти функцією [mail()](function.mail.md); за замовчуванням 25.

`sendmail_from` string

Адреса, яка буде використовуватися в заголовку `"From:"` у листах, що надсилаються безпосередньо через SMTP (лише для Windows). Ця директива також встановлює заголовок `"Return-Path:"`

`sendmail_path` string

Шлях до програми **sendmail**зазвичай /usr/sbin/sendmail або /usr/lib/sendmail . **configure** намагається знайти sendmail автоматично та встановити значення за замовчуванням самостійно, але якщо це не вдалося, ви можете встановити шлях тут.

Системи, що не використовують **sendmail**, повинні встановити цю директиву в дорогу до обгортки/замінника sendmail. Наприклад, користувачі [» Qmail](http://cr.yp.to/qmail.md) зазвичай встановлюють значення /var/qmail/bin/sendmail або /var/qmail/bin/qmail-inject.

**qmail-inject** не вимагає додаткових опцій для надсилання листів.

Ця директива також працює у Windows. Якщо вона встановлена, smtp, smtpport та sendmailfrom будуть проігноровані та виконається вказана програма.
