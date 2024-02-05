---
navigation:
  - function.sem-release.md: « sem\_release
  - function.shm-attach.md: shm\_attach »
  - index.md: PHP Manual
  - ref.sem.md: Функції семафорів
title: sem\_remove
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sem\_remove

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

sem\_remove — Видалення семафору

### Опис

```methodsynopsis
sem_remove(SysvSemaphore $semaphore): bool
```

**sem\_remove()** видаляє вказаний семафор.

Після видалення семафору він стає недоступним.

### Список параметрів

`semaphore`

Семафор, повернутий [sem\_get()](function.sem-get.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`semaphore` тепер чекає екземпляр [SysvSemaphore](class.sysvsemaphore.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [sem\_get()](function.sem-get.md) \- Отримання ідентифікатора семафору
-   [sem\_release()](function.sem-release.md) \- Звільнення семафору
-   [sem\_acquire()](function.sem-acquire.md) \- Захоплення семафору
