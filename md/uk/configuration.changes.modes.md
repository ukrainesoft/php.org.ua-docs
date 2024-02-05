---
navigation:
  - configuration.file.per-user.md: « Файли .user.ini
  - configuration.changes.md: Як змінити налаштування конфігурації »
  - index.md: PHP Manual
  - configuration.md: Конфігурація часу виконання
title: Місця встановлення параметрів конфігурації
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Місця встановлення параметрів конфігурації

Ці режими визначають, коли і де директива PHP може або не може бути встановлена, і кожна директива в посібнику відноситься до одного з цих режимів. Наприклад, деякі налаштування можуть бути встановлені за допомогою PHP-скрипту, який використовує [ini\_set()](function.ini-set.md), а інші можуть вимагати php.ini або httpd.conf.

Наприклад, директива [output\_buffering](outcontrol.configuration.md#ini.output-buffering) відповідає \*\*`INI_PERDIR`\*\*тому її не можна встановлювати через функцію [ini\_set()](function.ini-set.md). Тим не менш, директива [display\_errors](errorfunc.configuration.md#ini.display-errors) відповідає \*\*`INI_ALL`\*\*тому її можна встановлювати звідусіль, включаючи функцію [ini\_set()](function.ini-set.md)

**Константи режиму INI**

| Константы | Опис |
| --- | --- |
| **`INI_USER`**(int) | Запис задають у скриптах користувача (наприклад, функцією [ini\_set()](function.ini-set.md) [у реєстрі Windows](configuration.changes.md#configuration.changes.windows) або файлі .user.ini |
| **`INI_PERDIR`**(int) | Запис встановлюють у файлах php.ini, .htaccess, httpd.conf чи .user.ini |
| **`INI_SYSTEM`**(int) | Запис встановлюють у файлах php.ini або httpd.conf |
| **`INI_ALL`**(int) | Запис дозволено встановлювати будь-де |
