Налаштування під час виконання

-   [« Установка](mail.installation.html)
    
-   [Типы ресурсов »](mail.resources.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](mail.setup.html)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Конфігураційні опції надсилання листів**

| Имя                                                                                      | По умолчанию               | Место изменения | Список изменений |
|------------------------------------------------------------------------------------------|----------------------------|-----------------|------------------|
| [mail.add\_x\_header](mail.configuration.html#ini.mail.add-x-header)                     | "0"                        | PHPINIPERDIR    |                  |
| [mail.log](mail.configuration.html#ini.mail.log)                                         | NULL                       | PHPINISYSTEM    | PHPINIPERDIR     |
| [mail.force\_extra\_parameters](mail.configuration.html#ini.mail.force_extra_parameters) | NULL                       | PHPINISYSTEM    | PHPINIPERDIR     |
| [SMTP](mail.configuration.html#ini.smtp)                                                 | "localhost"                | PHPINIALL       |                  |
| [smtp\_port](mail.configuration.html#ini.smtp-port)                                      | "25"                       | PHPINIALL       |                  |
| [sendmail\_from](mail.configuration.html#ini.sendmail-from)                              | NULL                       | PHPINIALL       |                  |
| [sendmail\_path](mail.configuration.html#ini.sendmail-path)                              | "/usr/sbin/sendmail -t -i" | PHPINISYSTEM    |                  |

Для детального опису констант PHPINI, зверніться до розділу [Где могут быть установлены параметры конфигурации](configuration.changes.modes.html)

Коротке пояснення конфігураційних директив.

`mail.add_x_header` bool

Додає заголовок `X-PHP-Originating-Script`, який міститиме UID скрипта та ім'я файлу.

`mail.log` string

Шлях до лог-файлу, в який будуть записуватись всі виклики функції [mail()](function.mail.html). Записи в лозі містять повний шлях до скрипту, номер рядка, адреса одержувача `To` та заголовки.

`mail.force_extra_parameters` string

Примусово додати зазначені параметри для надсилання до sendmail. Ці параметри завжди замінюють значення п'ятого параметра в [mail()](function.mail.html), навіть у безпечному режимі.

`SMTP` string

Використовується лише у Windows: домен або IP-адреса SMTP-сервера, до якого буде звертатися PHP під час надсилання пошти функцією [mail()](function.mail.html)

`smtp_port` int

Використовується лише у Windows: порт `SMTP`сервера, до якого буде звертатися PHP під час надсилання пошти функцією [mail()](function.mail.html); за замовчуванням 25.

`sendmail_from` string

Адреса, яка буде використовуватися в заголовку `"From:"` у листах, що надсилаються безпосередньо через SMTP (лише для Windows). Ця директива також встановлює заголовок `"Return-Path:"`

`sendmail_path` string

Шлях до програми **sendmail**зазвичай /usr/sbin/sendmail або /usr/lib/sendmail . **configure** намагається знайти sendmail автоматично та встановити значення за замовчуванням самостійно, але якщо це не вдалося, ви можете встановити шлях тут.

Системи, що не використовують **sendmail**, повинні встановити цю директиву в дорогу до обгортки/замінника sendmail. Наприклад, користувачі [» Qmail](http://cr.yp.to/qmail.html) зазвичай встановлюють значення /var/qmail/bin/sendmail або /var/qmail/bin/qmail-inject.

**qmail-inject** не вимагає додаткових опцій для надсилання листів.

Ця директива також працює у Windows. Якщо вона встановлена, smtp, smtpport та sendmailfrom будуть проігноровані та виконається вказана програма.