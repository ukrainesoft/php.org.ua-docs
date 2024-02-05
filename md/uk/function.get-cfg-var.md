---
navigation:
  - function.gc-status.md: « gc\_status
  - function.get-current-user.md: get\_current\_user »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: get\_cfg\_var
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# get\_cfg\_var

(PHP 4, PHP 5, PHP 7, PHP 8)

get\_cfg\_var — Витягує налаштування конфігурації PHP

### Опис

```methodsynopsis
get_cfg_var(string $option): string|array|false
```

Витягує значення налаштування конфігурації PHP `option`

Функція не поверне жодної інформації, заданої під час складання PHP або вказаної в конфігураційному файлі Apache.

Щоб перевірити, що система використовує [файл конфігурації](configuration.file.md)спробуйте отримати значення налаштування конфігурації cfg\_file\_path. Якщо це налаштування доступне, використовується файл конфігурації.

### Список параметрів

`option`

Ім'я конфігураційної установки.

### Значення, що повертаються

Повертає поточне значення конфігурації PHP `option`или\*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ini\_get()](function.ini-get.md) \- Отримує значення налаштування конфігурації
-   [ini\_get\_all()](function.ini-get-all.md) \- Отримує всі налаштування конфігурації
