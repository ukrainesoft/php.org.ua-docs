---
navigation:
  - readline.installation.md: « Встановлення
  - readline.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - readline.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Readline**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [cli.pager](readline.configuration.md#ini.cli.pager) | "" | **`INI_ALL`** |  |
| [cli.prompt](readline.configuration.md#ini.cli.prompt) | "\\\\b \\\\> " | **`INI_ALL`** |  |

Коротке пояснення конфігураційних директив.

`cli.pager`string

Зовнішня утиліта для відображення висновку в [командний рядок](features.commandline.md)

`cli.prompt`string

Подсказка[командного рядка](features.commandline.md)
