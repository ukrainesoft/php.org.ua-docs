---
navigation:
  - function.msg-stat-queue.md: « msg\_stat\_queue
  - function.sem-get.md: sem\_get »
  - index.md: PHP Manual
  - ref.sem.md: Функції семафорів
title: sem\_acquire
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sem\_acquire

(PHP 4, PHP 5, PHP 7, PHP 8)

sem\_acquire - Захоплення семафору

### Опис

```methodsynopsis
sem_acquire(SysvSemaphore $semaphore, bool $non_blocking = false): bool
```

**sem\_acquire()** блокується (за потреби) до моменту захоплення семафору. Процес, який спробує захопити семафор, вже захоплений ним же буде заблокований назавжди, якщо буде перевищено максимальне значення семафору.

Після виконання запиту всі захоплені, але явно не звільнені процесом, семафори звільняються автоматично і генерується попередження.

### Список параметрів

`semaphore`

`semaphore`\- семафор.

`non_blocking`

Вказує, чи процес повинен чекати для захоплення семафора. Якщо встановлено **`true`**, виклик негайно поверне \*\*`false`\*\*якщо семафор не може бути захоплений.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`semaphore` тепер чекає екземпляр [SysvSemaphore](class.sysvsemaphore.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [sem\_get()](function.sem-get.md) \- Отримання ідентифікатора семафору
-   [sem\_release()](function.sem-release.md) \- Звільнення семафору
