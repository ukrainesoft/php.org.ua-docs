---
navigation:
  - readline.installation.html: « Установка
  - readline.resources.html: Типи ресурсів »
  - index.html: PHP Manual
  - readline.setup.html: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Readline**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [cli.pager](readline.configuration.html#ini.cli.pager) | "" | PHPINIALL |  |
| [cli.prompt](readline.configuration.html#ini.cli.prompt) | "в > " | PHPINIALL |  |

Коротке пояснення конфігураційних директив.

`cli.pager` string

Зовнішня утиліта для відображення висновку в [командную строку](features.commandline.html)

`cli.prompt` string

Підказка [командного рядка](features.commandline.html)
