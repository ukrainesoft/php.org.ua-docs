---
navigation:
  - function.set-include-path.md: « set\_include\_path
  - function.sys-get-temp-dir.md: sys\_get\_temp\_dir »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: set\_time\_limit
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# set\_time\_limit

(PHP 4, PHP 5, PHP 7, PHP 8)

set\_time\_limit — Обмеження часу виконання скрипту

### Опис

```methodsynopsis
set_time_limit(int $seconds): bool
```

Задає час у секундах, протягом якого сценарій повинен завершити роботу. Якщо скрипт не встигає, викликається фатальна помилка. За промовчанням надається 30 секунд або час, записаний у налаштуванні `max_execution_time` у php.ini (якщо таке налаштування встановлено).

При виклику **set\_time\_limit()** перезапускає лічильник із нуля. Іншими словами, якщо час очікування спочатку був 30 секунд, і через 25 секунд після запуску скрипта буде викликана функція `set_time_limit(20)`, Скрипт буде працювати максимум 45 секунд.

### Список параметрів

`seconds`

Максимальний час виконання за секунди. Якщо встановлено нуль, час виконання необмежений.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, інакше **`false`**

### Примітки

> **Зауваження** :
> 
> Функция**set\_time\_limit()** та директива [max\_execution\_time](info.configuration.md#ini.max-execution-time) впливають на час виконання лише самого скрипту. Час, витрачений на різні дії поза скриптом, такі як системні виклики функції [system()](function.system.md), Потокові операції, запити до баз даних і т.п. не включаються до розрахунку виконання скрипта. Це не стосується систем Windows, де розраховується абсолютний час виконання.

### Дивіться також

-   [max\_execution\_time](info.configuration.md#ini.max-execution-time)
-   [max\_input\_time](info.configuration.md#ini.max-input-time)
