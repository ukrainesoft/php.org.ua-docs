---
navigation:
  - filesystem.installation.md: « Установка
  - filesystem.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - filesystem.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Директиви конфігурації файлової системи та потоків**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [allowurlfopen](filesystem.configuration.md#ini.allow-url-fopen) | "1" | PHPINISYSTEM |  |
| [allowurlinclude](filesystem.configuration.md#ini.allow-url-include) | "0" | PHPINISYSTEM | Оголошена застаріла з версії PHP 7.4.0. |
| [useragent](filesystem.configuration.md#ini.user-agent) | NULL | PHPINIALL |  |
| [defaultsockettimeout](filesystem.configuration.md#ini.default-socket-timeout) | "60" | PHPINIALL |  |
| [from](filesystem.configuration.md#ini.from) | "" | PHPINIALL |  |
| [autodetectlineendings](filesystem.configuration.md#ini.auto-detect-line-endings) | "0" | PHPINIALL | Оголошена застаріла з версії PHP 8.1.0. |
| [systempdir](filesystem.configuration.md#ini.sys-temp-dir) | "" | PHPINISYSTEM |  |

Коротке пояснення конфігураційних директив.

`allow_url_fopen` bool

Ця директива включає підтримку обгорток URL (URL wrappers), які дозволяють працювати з об'єктами URL як із звичайними файлами. Обгортки, доступні за умовчанням, служать для роботи з [віддаленими файлами](features.remote-files.md) з використанням FTP або http протоколу. Деякі модулі, наприклад, [zlib](ref.zlib.md), можуть реєструвати власні обгортки.

`allow_url_include` bool

Ця опція дозволяє використовувати обгортки fopen, які підтримують роботу з URL, у функціях [include](function.include.md) [includeonce](function.include-once.md) [require](function.require.md) [requireonce](function.require-once.md)

> **Зауваження**
> 
> Ця опція вимагає включення опції allowurlfopen.

`user_agent` string

Встановлює рядок, що відсилається PHP, "User-Agent".

`default_socket_timeout` int

Значення часу очікування за промовчанням (у секундах) для потоків, які використовують сокети. Негативне значення означає нескінченний час очікування.

`from` string

Адреса email, що використовується у з'єднаннях FTP без авторизації, а також як значення заголовка From у HTTP з'єднаннях при використанні ftp та http обгорток, відповідно.

`auto_detect_line_endings` bool

Коли ця директива включена, PHP перевіряє дані, які отримують функції [fgets()](function.fgets.md) і [file()](function.file.md) щоб визначити спосіб завершення рядків (Unix, MS-Dos або Macintosh).

Ця директива дозволяє PHP взаємодіяти з системами Macintosh, однак, за умовчанням ця директива вимкнена, оскільки при її використанні виникає (несуттєва) потреба в додаткових ресурсах для визначення символу закінчення першого рядка, а також тому, що програмісти, що використовують у системах Unix символи повернення каретки як роздільники, зіткнуться із зворотно-несумісною поведінкою PHP.

`sys_temp_dir` string
