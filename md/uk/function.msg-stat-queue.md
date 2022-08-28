Отримання інформації із структури даних черги повідомлень

-   [« msg\_set\_queue](function.msg-set-queue.html)
    
-   [sem\_acquire »](function.sem-acquire.html)
    
-   [PHP Manual](index.html)
    
-   [Функции семафоров](ref.sem.html)
    
-   Отримання інформації із структури даних черги повідомлень
    

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

| Версия | Описание                                                                                                                    |
|--------|-----------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `queue` тепер чекає екземпляр [SysvMessageQueue](class.sysvmessagequeue.html); раніше очікували ресурс (resource). |

### Дивіться також

-   [msg\_remove\_queue()](function.msg-remove-queue.html) - Видалення черги повідомлень
-   [msg\_receive()](function.msg-receive.html) - Отримання повідомлення з черги повідомлень
-   [msg\_get\_queue()](function.msg-get-queue.html) - Створення або підключення до черги повідомлень
-   [msg\_set\_queue()](function.msg-set-queue.html) - Встановлення інформації у структурі даних черги повідомлень