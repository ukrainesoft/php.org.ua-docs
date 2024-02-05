---
navigation:
  - function.socket-set-timeout.md: « socket\_set\_timeout
  - book.rrd.md: RRD »
  - index.md: PHP Manual
  - ref.network.md: Мережеві функції
title: syslog
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# syslog

(PHP 4, PHP 5, PHP 7, PHP 8)

syslog - Генерує повідомлення для системного журналу

### Опис

```methodsynopsis
syslog(int $priority, string $message): true
```

Функция**syslog()** генерує повідомлення, яке надсилається до системного журналу.

З приводу інформації щодо встановлення користувача повідомлень журналу дивіться Unix керівництво в частині syslog.conf (5). Додаткову інформацію про функціонал syslog можна отримати за допомогою man для syslog (3) на Unix-машинах.

### Список параметрів

`priority`

Параметр`priority` - це комбінація типу та рівня. Можливими значеннями є:

**Пріоритети **syslog()** (за зменшенням)**

| Константа | Опис |
| --- | --- |
| **`LOG_EMERG`** | система непридатна |
| **`LOG_ALERT`** | необхідні негайні заходи |
| **`LOG_CRIT`** | критичні умови |
| **`LOG_ERR`** | умови помилки |
| **`LOG_WARNING`** | умови попередження |
| **`LOG_NOTICE`** | нормальні, але значну умову |
| **`LOG_INFO`** | інформаційне повідомлення |
| **`LOG_DEBUG`** | повідомлення налагодження |

`message`

Надіслане повідомлення.

### Значення, що повертаються

Функція завжди повертає **`true`**

### Приклади

**Пример #1 Пример использования**syslog()\*\*\*\*

```php
<?php
// открыть syslog, включить в сообщение ID процесса, также отправить
// сообщение, и использовать определённый пользователем
// механизм журналирования
openlog("myScriptLog", LOG_PID | LOG_PERROR, LOG_LOCAL0);

// некий код

if (authorized_client()) {
    // что-нибудь сделать
} else {
    // неавторизованный клиент!
    // отправить сообщение журнала о попытке
    $access = date("Y/m/d H:i:s");
    syslog(LOG_WARNING, "Неавторизованный клиент: $access {$_SERVER['REMOTE_ADDR']} ({$_SERVER['HTTP_USER_AGENT']})");
}

closelog();
?>
```

### Примітки

У Windows служба syslog емулюється, використовуючи журнал подій (Event Log).

> **Зауваження** :
> 
> Использование значений с`LOG_LOCAL0`по`LOG_LOCAL7`для параметра`facility` у функції [openlog()](function.openlog.md) недоступно у Windows.

### Дивіться також

-   [openlog()](function.openlog.md) \- Відкриває підключення до системного журналу
-   [closelog()](function.closelog.md) \- Закриває з'єднання із системним журналом
-   [syslog.filter](errorfunc.configuration.md#ini.syslog.filter)Налаштування INI (починаючи з PHP 7.3)
