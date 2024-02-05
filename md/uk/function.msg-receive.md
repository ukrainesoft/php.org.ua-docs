---
navigation:
  - function.msg-queue-exists.md: « msg\_queue\_exists
  - function.msg-remove-queue.md: msg\_remove\_queue »
  - index.md: PHP Manual
  - ref.sem.md: Функції семафорів
title: msg\_receive
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# msg\_receive

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

msg\_receive — отримання повідомлення з черги повідомлень

### Опис

```methodsynopsis
msg_receive(    SysvMessageQueue $queue,    int $desired_message_type,    int &$received_message_type,    int $max_message_size,    mixed &$message,    bool $unserialize = true,    int $flags = 0,    int &$error_code = null): bool
```

\*\*msg\_receive()\*\*получает первое сообщение из задаваемой параметром`queue` черги повідомлень з типом, зазначеним у `desired_message_type`

### Список параметрів

`queue`

Черга повідомлень.

`desired_message_type`

Якщо в `desired_message_type` вказано 0, повертається перше повідомлення із черги. Якщо `desired_message_type` більше 0, то повертається перше повідомлення із зазначеним типом. Якщо `desired_message_type` менше 0, то повертається перше повідомлення з типом, меншим або рівним по модулю вказаному в `desired_message_type`. Якщо немає повідомлень, які відповідають критеріям, ваш скрипт очікує їх появи у черзі. Ви можете змінити цю поведінку, вказавши \*\*`MSG_IPC_NOWAIT`\*\*в параметре`flags`

`received_message_type`

Цей параметр зберігає тип отриманого повідомлення.

`max_message_size`

Максимальний розмір повідомлення, що приймається, задається в `max_message_size`; якщо повідомлення в черзі більше за цей розмір, то функція завершується помилкою (якщо ви не встановите `flags` як описано нижче).

`message`

Полученное сообщение сохраняется в`message`якщо не було помилок при отриманні.

`unserialize`

Если установлено в\*\*`true`\*\*повідомлення розглядається як серіалізоване з використанням того ж механізму, що і в модулі сесій. Повідомлення десеріалізується, а потім повертається до вашого скрипту. Це дозволяє легко отримувати масиви та складні об'єкти з інших PHP-скриптів, або, якщо ви використовуєте WDDX-серіалізатор, з будь-яких сумісних з WDDX джерел.

Якщо в `unserialize`указано\*\*`false`\*\*, повідомлення повертається у вигляді бінарно-безпечного рядка

`flags`

Необов'язковий параметр `flags` дозволяє передати прапорці в низькорівневий системний виклик msgrcv. За замовчуванням його значення 0, однак ви можете вказати одне або кілька таких значень (складаючи їх або виконуючи операцію бінарного АБО).

<table class="doctable table"><caption><strong>Flag values ​​for msg_receive</strong></caption><tbody class="tbody"><tr><td><strong><code>MSG_IPC_NOWAIT</code></strong></td><td>Якщо немає повідомлень, які відповідають умовам <code class="parameter">desired_message_type</code>, повертатися негайно, а не чекати. Функція завершується помилкою і повертає ціле значення <strong><code>MSG_ENOMSG</code></strong>.</td></tr><tr><td><strong><code>MSG_EXCEPT</code></strong></td><td>Використання цього прапора в комбінації із зазначеним у <code class="parameter">desired_message_type</code> позитивним значенням, дозволяє отримати перше повідомлення, тип якого не дорівнює значенню <code class="parameter">desired_message_type</code>.</td></tr><tr><td><strong><code>MSG_NOERROR</code></strong></td><td>Якщо розмір повідомлення перевищує <code class="parameter">max_message_size</code>, то встановлення цього прапора призводить до усічення повідомлення до <code class="parameter">max_message_size</code> без сигналізації про помилку.</td></tr></tbody></table>

`error_code`

Якщо функція завершується аварійно, необов'язковий параметр `error_code` міститиме значення системної змінної errno.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

При успішному завершенні структура даних черги повідомлень оновлюється таким чином: `msg_lrpid` містить ідентифікатор процесу, що викликав, `msg_qnum` зменшується на 1 та `msg_rtime`устанавливается соответственно текущему времени.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`queue` тепер чекає екземпляр [SysvMessageQueue](class.sysvmessagequeue.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [msg\_remove\_queue()](function.msg-remove-queue.md) \- Видалення черги повідомлень
-   [msg\_send()](function.msg-send.md) \- Надсилання повідомлення в чергу повідомлень
-   [msg\_stat\_queue()](function.msg-stat-queue.md) \- Отримання інформації із структури даних черги повідомлень
-   [msg\_set\_queue()](function.msg-set-queue.md) \- Встановлення інформації у структурі даних черги повідомлень
