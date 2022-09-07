---
navigation:
  - function.msg-set-queue.md: « msgsetqueue
  - function.sem-acquire.md: semacquire »
  - index.md: PHP Manual
  - ref.sem.md: Функції семафорів
title: msgстатиqueue
---
# msgстатиqueue

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

msgстатиqueue — Отримання інформації із структури даних черги повідомлень

### Опис

```methodsynopsis
msg_stat_queue(SysvMessageQueue $queue): array|false
```

**msgстатиqueue()** повертає мета-дані черги повідомлень, що задається `queue`. Це корисно, наприклад, визначення процесу-відправника отриманого вами щойно повідомлення.

### Список параметрів

`queue`

Черга повідомлень.

### Значення, що повертаються

У разі успішного виконання значення, що повертається, являє собою масив, ключі і значення якого означають наступне:

< td>gid власника черги.< td>`msg_rtime`< td>Кількість повідомлень у черзі.

<table class="doctable table"><caption><strong>Структура масиву для msg_stat_queue</strong></caption><tbody class="tbody"><tr><td><code class="literal">msg_perm .uid</code></td><td>uid власника черги</td></tr><tr><td><code class="literal">msg_perm.gid</code></td></tr><tr><td><code class="literal">msg_perm.mode</code></td><td>Режим доступу до черги.</td></tr><tr><td><code class="literal">msg_stime</code></td><td>Час останньої відправки повідомлення в чергу.</td></tr><tr><td>Час останнього отримання повідомлення з черги.</td></tr><tr><td><code class="literal">msg_ctime</code></td><td>Час останньої зміни черги.</td></tr><tr><td><code class="literal">msg_qnum</code></td></tr><tr><td><code class="literal">msg_qbytes</code></td><td>Максимальна кількість байт, допустима в одній черзі повідомлень . У Linux це значення можна отримати і змінити через <var class="filename">/proc/sys/kernel/msgmnb</var>.</td></tr><tr><td><code class="literal ">msg_lspid</code></td><td>pid процесу, що останнім надіслав повідомлення в чергу.</td></tr><tr><td><code class="literal">msg_lrpid</code></td><td>pid процесу, що останнім отримав повідомлення з черги.</td></tr></tbody></table>

Повертає **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `queue` тепер чекає екземпляр [SysvMessageQueue](class.sysvmessagequeue.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [msgremovequeue()](function.msg-remove-queue.md) - Видалення черги повідомлень
-   [msgreceive()](function.msg-receive.md) - Отримання повідомлення з черги повідомлень
-   [msggetqueue()](function.msg-get-queue.md) - Створення або підключення до черги повідомлень
-   [msgsetqueue()](function.msg-set-queue.md) - Встановлення інформації у структурі даних черги повідомлень
