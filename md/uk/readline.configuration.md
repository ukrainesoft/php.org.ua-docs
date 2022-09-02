---
navigation:
  - readline.installation.md: « Установка
  - readline.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - readline.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Readline**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [cli.pager](readline.configuration.md#ini.cli.pager) | "" | PHPINIALL |  |
| [cli.prompt](readline.configuration.md#ini.cli.prompt) | "в > " | PHPINIALL |  |

Коротке пояснення конфігураційних директив.

`cli.pager` string

Зовнішня утиліта для відображення висновку в [командную строку](features.commandline.md)

`cli.prompt` string

Підказка [командного рядка](features.commandline.md)
