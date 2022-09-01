---
navigation:
  - apache.installation.md: « Встановлення
  - apache.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - apache.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка модуля Apache PHP залежить від налаштувань у php.ini. Налаштування конфігурації з php.ini можуть бути перевизначені через налаштування прапора [phpflag](configuration.changes.html#configuration.changes.apache) у конфігураційному файлі сервера або локальному файлі .htaccess.

**Приклад #1 Відключення PHP-сервера для директорії за допомогою .htaccess**

```
php_flag engine off
```

**Установки конфігурації Apache**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [engine](apache.configuration.html#ini.engine) | "1" | PHPINIALL |  |
| [childterminate](apache.configuration.html#ini.child-terminate) | "0" | PHPINIALL |  |
| [lastmodified](apache.configuration.html#ini.last-modified) | "0" | PHPINIALL |  |
| [xbithack](apache.configuration.html#ini.xbithack) | "0" | PHPINIALL |  |

Для детального опису констант PHPINI, зверніться до розділу [Де можуть бути встановлені параметри конфігурації](configuration.changes.modes.md)

Коротке пояснення конфігураційних директив.

`engine` bool

Включає чи вимикає інтерпретатор PHP. Ця директива насправді дуже корисна у модулі Apache PHP. Вона використовується сайтами, яким необхідно дозволити чи заборонити інтерпретатор PHP на основі директорій чи віртуальних хостів. Встановлююча **`engine off`** за потребою у файлі httpd.conf можна дозволити або заборонити інтерпретатор PHP.

`child_terminate` bool

Ця Встановлення керує тим, чи можуть скрипти PHP вимагати закінчення дочірніх процесів після завершення запиту. Дивіться також [apachechildterminate()](function.apache-child-terminate.md)

`last_modified` bool

Надсилає скриптам PHP дату модифікації як заголовок Last-Modified для цього запиту.

`xbithack` bool

Виконання файлів з бітом, що запускається як PHP, незалежно від розширення.
