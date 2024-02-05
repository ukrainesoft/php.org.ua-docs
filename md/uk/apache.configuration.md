---
navigation:
  - apache.installation.md: « Встановлення
  - apache.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - apache.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка модуля Apache PHP залежить від налаштувань у php.ini. Налаштування конфігурації з php.ini можуть бути перевизначені через налаштування прапора [php\_flag](configuration.changes.md#configuration.changes.apache) у конфігураційному файлі сервера або локальному файлі .htaccess.

**Приклад #1 Відключення PHP-сервера для директорії за допомогою .htaccess**

```
php_flag engine off
```

**Установки конфігурації Apache**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [engine](apache.configuration.md#ini.engine) | "1" | **`INI_ALL`** |  |
| [child\_terminate](apache.configuration.md#ini.child-terminate) | "0" | **`INI_ALL`** |  |
| [last\_modified](apache.configuration.md#ini.last-modified) | "0" | **`INI_ALL`** |  |
| [xbithack](apache.configuration.md#ini.xbithack) | "0" | **`INI_ALL`** |  |

Додаткова інформація та опис режимів INI\_\* дано у розділі «[Місця встановлення параметрів конфігурації](configuration.changes.modes.md)».

Коротке пояснення конфігураційних директив.

`engine`bool

Включає чи вимикає інтерпретатор PHP. Ця директива дуже корисна в модулі Apache PHP. Вона використовується сайтами, яким необхідно дозволити чи заборонити інтерпретатор PHP на основі директорій чи віртуальних хостів. Встановлююча **`engine off`** за потребою у файлі httpd.conf можна дозволити або заборонити інтерпретатор PHP.

`child_terminate`bool

Ця установка керує тим, чи можуть скрипти PHP вимагати закінчення дочірніх процесів після завершення запиту. Дивіться також [apache\_child\_terminate()](function.apache-child-terminate.md)

`last_modified`bool

Надсилає скриптам PHP дату модифікації як заголовок Last-Modified для цього запиту.

`xbithack`bool

Виконання файлів з бітом, що запускається як PHP, незалежно від розширення.
