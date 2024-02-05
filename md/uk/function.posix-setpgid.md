---
navigation:
  - function.posix-setgid.md: « posix\_setgid
  - function.posix-setrlimit.md: posix\_setrlimit »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_setpgid
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_setpgid

(PHP 4, PHP 5, PHP 7, PHP 8)

posix\_setpgid - Встановлює ідентифікатор групи процесу для менеджера завдань

### Опис

```methodsynopsis
posix_setpgid(int $process_id, int $process_group_id): bool
```

Добавляет к процессу`process_id` ідентифікатор групи `process_group_id`

### Список параметрів

`process_id`

Ідентифікатор процесу.

`process_group_id`

Ідентифікатор групи процесу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   Для отримання більш повної інформації про процеси та керування завданнями зверніться до POSIX.1 та setsid(2) посібника в POSIX системах.
