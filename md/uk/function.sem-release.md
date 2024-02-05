---
navigation:
  - function.sem-get.md: « sem\_get
  - function.sem-remove.md: sem\_remove »
  - index.md: PHP Manual
  - ref.sem.md: Функції семафорів
title: sem\_release
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sem\_release

(PHP 4, PHP 5, PHP 7, PHP 8)

sem\_release - Звільнення семафору

### Опис

```methodsynopsis
sem_release(SysvSemaphore $semaphore): bool
```

**sem\_release()** звільняє семафор, якщо він був захоплений зухвалим процесом, інакше генерується попередження.

Після звільнення семафор може бути захоплений повторно через виклик [sem\_acquire()](function.sem-acquire.md)

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
-   [sem\_acquire()](function.sem-acquire.md) \- Захоплення семафору
