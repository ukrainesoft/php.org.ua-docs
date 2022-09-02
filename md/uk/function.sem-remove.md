---
navigation:
  - function.sem-release.md: « semrelease
  - function.shm-attach.md: shmattach »
  - index.md: PHP Manual
  - ref.sem.md: Функції семафорів
title: semremove
---
# semremove

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

semremove — Видалення семафору

### Опис

```methodsynopsis
sem_remove(SysvSemaphore $semaphore): bool
```

**semremove()** видаляє вказаний семафор.

Після видалення семафору він стає недоступним.

### Список параметрів

`semaphore`

Семафор, повернутий [semget()](function.sem-get.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `semaphore` тепер чекає екземпляр [SysvSemaphore](class.sysvsemaphore.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [semget()](function.sem-get.md) - Отримання ідентифікатора семафору
-   [semrelease()](function.sem-release.md) - Звільнення семафору
-   [semacquire()](function.sem-acquire.md) - Захоплення семафору
