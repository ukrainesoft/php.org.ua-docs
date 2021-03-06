- [« imap_num_msg](function.imap-num-msg.md)
- [imap_open »](function.imap-open.md)

- [PHP Manual](index.md)
- [Функції IMAP](ref.imap.md)
- Отримати кількість нових повідомлень у поточній поштовій скриньці

#imap_num_recent

(PHP 4, PHP 5, PHP 7, PHP 8)

imap_num_recent — Отримати кількість нових повідомлень у поточному поштовому
ящику

### Опис

**imap_num_recent**([IMAP\Connection](class.imap-connection.md)
`$imap`): int

Повертає кількість нових повідомлень у поточній поштовій скриньці.

### Список параметрів

`imap`
Примірник [IMAP\Connection](class.imap-connection.md).

### Значення, що повертаються

Повертає кількість нових повідомлень у поточній поштовій скриньці у вигляді
цілого числа.

### Список змін

| Версія | Опис                                                                                                                                                   |
| ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 8.1.0  | Параметр imap тепер чекає на екземпляр [IMAP\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md)). |

### Дивіться також

- [imap_num_msg()](function.imap-num-msg.md) - Отримати кількість
повідомлень у поточній поштовій скриньці
- [imap_status()](function.imap-status.md) - Отримати інформацію з
статусу поштової скриньки
