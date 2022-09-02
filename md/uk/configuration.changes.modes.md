---
navigation:
  - configuration.file.per-user.md: « Файли .user.ini
  - configuration.changes.md: Як змінити налаштування конфігурації »
  - index.md: PHP Manual
  - configuration.md: Конфігурація часу виконання
title: Де можна встановити параметри конфігурації
---
## Де можна встановити параметри конфігурації

Ці режими визначають, коли і де директива PHP може або не може бути встановлена, і кожна директива в посібнику відноситься до одного з цих режимів. Наприклад, деякі налаштування можуть бути встановлені за допомогою PHP-скрипту, який використовує [iniset()](function.ini-set.md), а інші можуть вимагати php.ini або httpd.conf.

Наприклад, директива [outputbuffering](outcontrol.configuration.md#ini.output-buffering) відповідає `PHP_INI_PERDIR`тому вона не може бути встановлена ​​через [iniset()](function.ini-set.md). Тим не менш, директива [displayerrors](errorfunc.configuration.md#ini.display-errors) відповідає `PHP_INI_ALL`тому вона може бути встановлена ​​звідусіль, включаючи [iniset()](function.ini-set.md)

**Визначення режимів PHPINI**

| Режим | Описание |
| --- | --- |
| `PHP_INI_USER` | Значення може бути встановлено в скриптах користувача (за допомогою [iniset()](function.ini-set.md)) або в [реестре Windows](configuration.changes.md#configuration.changes.windows). Значення може бути встановлене в .user.ini |
| `PHP_INI_PERDIR` | Значення може бути встановлене в php.ini, .htaccess або httpd.conf |
| `PHP_INI_SYSTEM` | Значення може бути встановлене в php.ini або httpd.conf |
| `PHP_INI_ALL` | Значення може бути встановлене звідусіль |
