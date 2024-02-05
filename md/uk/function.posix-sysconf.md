---
navigation:
  - function.posix-strerror.md: « posix\_strerror
  - function.posix-times.md: posix\_times »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_sysconf
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_sysconf

(PHP 8 >= 8.3.0)

posix\_sysconf — Повертає інформацію про систему під час виконання

### Опис

```methodsynopsis
posix_sysconf(int $conf_id): int
```

Повертає інформацію про налаштування під час роботи системи.

### Список параметрів

`conf_id`

Ідентифікатор змінної з наступними константами: **`POSIX_SC_ARG_MAX`** **`POSIX_SC_PAGESIZE`** **`POSIX_SC_NPROCESSORS_CONF`** **`POSIX_SC_NPROCESSORS_ONLN`**

### Значення, що повертаються

Повертає числове значення, пов'язане з ідентифікатором `conf_id`

### Приклади

**Пример #1 Пример использования функции**posix\_sysconf()\*\*\*\*

Повертає кількість активних процесорів.

```php
<?php

echo posix_sysconf(POSIX_SC_NPROCESSORS_ONLN);
?>
```

Результат виконання наведеного прикладу:

```
2
```
