---
navigation:
  - function.sem-get.html: « semget
  - function.sem-remove.html: semremove »
  - index.md: PHP Manual
  - ref.sem.md: Функції семафорів
title: semrelease
---
# semrelease

(PHP 4, PHP 5, PHP 7, PHP 8)

semrelease - Звільнення семафору

### Опис

```methodsynopsis
sem_release(SysvSemaphore $semaphore): bool
```

**semrelease()** звільняє семафор, якщо він був захоплений зухвалим процесом, інакше генерується попередження.

Після звільнення семафор може бути захоплений повторно через виклик [semacquire()](function.sem-acquire.md)

### Список параметрів

`semaphore`

Семафор, повернутий [semget()](function.sem-get.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `semaphore` тепер чекає екземпляр [SysvSemaphore](class.sysvsemaphore.md); раніше очікувався ресурс (resource). |

### Дивіться також

-   [semget()](function.sem-get.md) - Отримання ідентифікатора семафору
-   [semacquire()](function.sem-acquire.md) - Захоплення семафору
