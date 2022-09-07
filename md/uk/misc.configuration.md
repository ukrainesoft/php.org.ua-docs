---
navigation:
  - misc.installation.md: « Установка
  - misc.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - misc.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштувань різних функцій**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [ignoreuserabort](misc.configuration.md#ini.ignore-user-abort) | "0" | PHPINIALL |  |
| [highlight.string](misc.configuration.md#ini.syntax-highlighting) | "#DD0000" | PHPINIALL |  |
| [highlight.comment](misc.configuration.md#ini.syntax-highlighting) | "#FF8000" | PHPINIALL |  |
| [highlight.keyword](misc.configuration.md#ini.syntax-highlighting) | "#007700" | PHPINIALL |  |
| [highlight.default](misc.configuration.md#ini.syntax-highlighting) | "#0000BB" | PHPINIALL |  |
| [highlight.html](misc.configuration.md#ini.syntax-highlighting) | "#000000" | PHPINIALL |  |
| [browscap](misc.configuration.md#ini.browscap) | NULL | PHPINISYSTEM |  |

Для детального опису констант PHPINI, зверніться до розділу [Де можуть бути встановлені параметри конфігурації](configuration.changes.modes.md)

Коротке пояснення конфігураційних директив.

`ignore_user_abort` bool

**`false`** за замовчуванням. Якщо змінюється на **`true`**, Скрипти не будуть перервані після того, як клієнт розірве з'єднання.

Дивіться також [ignoreuserabort()](function.ignore-user-abort.md)

`highlight.bg` string

`highlight.comment` string

`highlight.default` string

`highlight.html` string

`highlight.keyword` string

`highlight.string` string

Кольори для режиму підсвічування (Syntax Highlighting). Все, що прийнятно в , буде працювати.

`browscap` string

Ім'я (наприклад, browscap.ini) та розташування файлу можливостей браузера. Дивіться також [getbrowser()](function.get-browser.md)
