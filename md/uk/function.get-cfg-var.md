---
navigation:
  - function.gc-status.html: « gcstatus
  - function.get-current-user.html: getcurrentuser »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: getcfgvar
---
# getcfgvar

(PHP 4, PHP 5, PHP 7, PHP 8)

getcfgvar — Витягує налаштування конфігурації PHP

### Опис

```methodsynopsis
get_cfg_var(string $option): string|array|false
```

Витягує значення налаштування конфігурації PHP `option`

Функція не поверне жодної інформації, заданої під час складання PHP або вказаної в конфігураційному файлі Apache.

Щоб перевірити, що система використовує [файл конфигурации](configuration.file.md)спробуйте отримати значення налаштування конфігурації cfgfilepath. Якщо це налаштування доступне, використовується файл конфігурації.

### Список параметрів

`option`

Ім'я конфігураційної установки.

### Значення, що повертаються

Повертає поточне значення конфігурації PHP `option` або **`false`** у разі виникнення помилки.

### Дивіться також

-   [iniget()](function.ini-get.html) - Отримує значення налаштування конфігурації
-   [inigetall()](function.ini-get-all.html) - Отримує всі налаштування конфігурації
