---
navigation:
  - filter.installation.md: « Встановлення
  - filter.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - filter.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Параметри конфігурації Filter**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [filter.default](filter.configuration.md#ini.filter.default) | "unsafe\_raw" | **`INI_PERDIR`** | Параметр застарів, починаючи з PHP 8.1.0. |
| [filter.default\_flags](filter.configuration.md#ini.filter.default-flags) | NULL | **`INI_PERDIR`** |  |

Додаткова інформація та опис режимів INI\_\* дано у розділі «[Місця встановлення параметрів конфігурації](configuration.changes.modes.md)».

Коротке пояснення конфігураційних директив.

`filter.default`string

Фільтрує всі дані [$\_GET](reserved.variables.get.md) [$\_POST](reserved.variables.post.md) [$\_COOKIE](reserved.variables.cookies.md) [$\_REQUEST](reserved.variables.request.md) і [$\_SERVER](reserved.variables.server.md) цим фільтром. Вихідні дані можуть бути отримані за допомогою [filter\_input()](function.filter-input.md)

Приймає ім'я вказаного фільтра як значення за промовчанням. Імена фільтрів можна знайти в [списку існуючих фільтрів](filter.filters.md)

> **Зауваження** :
> 
> Будьте уважні з прапорами за промовчанням для стандартних фільтрів. Слід явно встановлювати їх у значення, яке вам необхідно. Наприклад, для установки фільтра за умовчанням, який буде працювати точнісінько аналогічно функції [htmlspecialchars()](function.mdspecialchars.md)Вам необхідно встановити прапори за промовчанням в 0 так, як показано нижче.
> 
> **Приклад #1 Налаштування стандартного фільтра для роботи аналогічно функції htmlspecialchars**
> 
> ```php
> filter.default = full_special_chars
> filter.default_flags = 0
> ```

`filter.default_flags`int

Прапори за промовчанням, які застосовуються, коли встановлено стандартний фільтр. За замовчуванням встановлено \*\*`FILTER_FLAG_NO_ENCODE_QUOTES`\*\*в целях сохранения обратной совместимости. Смотрите[список існуючих прапорів](filter.filters.flags.md) для ознайомлення зі списком усіх імен прапорів.
