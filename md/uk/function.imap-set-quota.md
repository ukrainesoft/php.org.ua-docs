---
navigation:
  - function.imap-search.md: « imap\_search
  - function.imap-setacl.md: imap\_setacl »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_set\_quota
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_set\_quota

(PHP 4 >= 4.0.5, PHP 5, PHP 7, PHP 8)

imap\_set\_quota — Встановлює квоту для заданої поштової скриньки

### Опис

```methodsynopsis
imap_set_quota(IMAP\Connection $imap, string $quota_root, int $mailbox_size): bool
```

Встановлює верхню межу квоти для заданої поштової скриньки.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`quota_root`

Поштова скринька, для якої буде встановлено квоту. Рядок у форматі стандарту IMAP: `user.name`

`mailbox_size`

Максимальний розмір (у кілобайтах) для `quota_root`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Приклади

**Приклад #1 Приклад використання** imap\_set\_quota()\*\*\*\*

```php
<?php
$mbox = imap_open("{imap.example.org:143}", "mailadmin", "password");

if (!imap_set_quota($mbox, "user.kalowsky", 3000)) {
    echo "Ошибка при установке квоты\n";
    return;
}

imap_close($mbox);
?>
```

### Примітки

На даний момент ця функція підтримується лише при використанні бібліотеки c-client2000 або свіжішої.

Заданий `imap` має бути відкрито від імені адміністратора поштового сервера, інакше функція завершиться з помилкою.

### Дивіться також

-   [imap\_open()](function.imap-open.md) \- Відкриває потік IMAP до поштової скриньки
-   [imap\_get\_quota()](function.imap-get-quota.md) \- Отримує налаштування рівня квоти та статистику використання поштових скриньок
