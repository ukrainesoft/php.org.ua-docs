---
navigation:
  - function.imap-search.html: « imapsearch
  - function.imap-setacl.html: imapsetacl »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imapsetquota
---
# imapsetquota

(PHP 4> = 4.0.5, PHP 5, PHP 7, PHP 8)

imapsetquota — Встановити квоту для заданої поштової скриньки

### Опис

```methodsynopsis
imap_set_quota(IMAP\Connection $imap, string $quota_root, int $mailbox_size): bool
```

Встановлює верхню межу квоти для заданої поштової скриньки

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.html)

`quota_root`

Поштова скринька, для якої встановлюється квота у вигляді рядка у форматі IMAP: `user.name`

`mailbox_size`

Максимальний розмір (у кілобайтах) для `quota_root`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **imapsetquota()****

```php
<?php
$mbox = imap_open("{imap.example.org:143}", "mailadmin", "password");

if (!imap_set_quota($mbox, "user.kalowsky", 3000)) {
    echo "Ошибка при установке квоты\n";
    return;
}

imap_close($mbox);
?>
```

### Примітки

На даний момент ця функція підтримується лише при використанні бібліотеки c-client2000 або свіжішої.

Заданий `imap` має бути відкрито від імені адміністратора поштового сервера, інакше функція завершиться з помилкою.

### Дивіться також

-   [imapopen()](function.imap-open.html) - Відкриває потік IMAP до поштової скриньки
-   [imapgetquota()](function.imap-get-quota.html) - Отримати налаштування рівня квоти та статистику використання поштових скриньок
