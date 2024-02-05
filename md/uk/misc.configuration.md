---
navigation:
  - misc.installation.md: « Встановлення
  - misc.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - misc.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштувань різних функцій**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [ignore\_user\_abort](misc.configuration.md#ini.ignore-user-abort) | "0" | **`INI_ALL`** |  |
| [highlight.string](misc.configuration.md#ini.syntax-highlighting) | "#DD0000" | **`INI_ALL`** |  |
| [highlight.comment](misc.configuration.md#ini.syntax-highlighting) | "#FF8000" | **`INI_ALL`** |  |
| [highlight.keyword](misc.configuration.md#ini.syntax-highlighting) | "#007700" | **`INI_ALL`** |  |
| [highlight.default](misc.configuration.md#ini.syntax-highlighting) | "#0000BB" | **`INI_ALL`** |  |
| [highlight.md](misc.configuration.md#ini.syntax-highlighting) | "#000000" | **`INI_ALL`** |  |
| [browscap](misc.configuration.md#ini.browscap) | NULL | **`INI_SYSTEM`** |  |

Додаткова інформація та опис режимів INI\_\* дано у розділі «[Місця встановлення параметрів конфігурації](configuration.changes.modes.md)».

Коротке пояснення конфігураційних директив.

`ignore_user_abort`bool

**`false`**по умолчанию. Если изменяется на**`true`**, Скрипти не будуть перервані після того, як клієнт розірве з'єднання.

Смотрите также[ignore\_user\_abort()](function.ignore-user-abort.md)

`highlight.bg`string

`highlight.comment`string

`highlight.default`string

`highlight.md`string

`highlight.keyword`string

`highlight.string`string

Кольори для режиму підсвічування (Syntax Highlighting). Все, що прийнятно в , буде працювати.

`browscap`string

Ім'я (наприклад, browscap.ini) та розташування файлу можливостей браузера. Дивіться також [get\_browser()](function.get-browser.md)
