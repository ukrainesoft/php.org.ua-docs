---
navigation:
  - function.imap-get-quota.md: « imapgetquota
  - function.imap-getacl.md: imapgetacl »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imapgetquotaroot
---
# imapgetquotaroot

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

imapgetquotaroot — Отримати параметри квоти для кожного користувача

### Опис

```methodsynopsis
imap_get_quotaroot(IMAP\Connection $imap, string $mailbox): array|false
```

Повертає параметри квоти для кожного користувача. Число із ключем "limit" визначає максимальний допустимий розмір скриньки. Число із ключем "usage" визначає поточний рівень використання.

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.md)

`mailbox`

`mailbox` має містити ім'я скриньки (наприклад, INBOX).

### Значення, що повертаються

Повертає масив цілих чисел, які стосуються конкретного користувача. Як ключі масиву використовуються імена ресурсів, а як значення масиви з ключами "limit" і "usage".

У разі виникнення помилки ця функція поверне **`false`** та масив інформації про з'єднання у разі отримання відповіді, яку вона не зможе розібрати.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **imapgetquotaroot()****

```php
<?php
$mbox = imap_open("{imap.example.org}", "kalowsky", "password", OP_HALFOPEN)
      or die("не удалось подключиться: " . imap_last_error());

$quota = imap_get_quotaroot($mbox, "INBOX");
if (is_array($quota)) {
   $storage = $quota['STORAGE'];
   echo "Уровень использования STORAGE: " .  $storage['usage'];
   echo "Максимальный размер STORAGE: " .  $storage['limit'];

   $message = $quota['MESSAGE'];
   echo "Уровень использования MESSAGE: " .  $message['usage'];
   echo "Максимальный размер MESSAGE: " .  $message['limit'];

   /* ...  */

}

imap_close($mbox);
?>
```

### Примітки

Ця функція доступна лише під час використання бібліотеки c-client2000 або новішої.

Заданий потік `imap` повинен бути відкритий під користувачем, чию скриньку ви хочете перевірити.

### Дивіться також

-   [imapopen()](function.imap-open.md) - Відкриває потік IMAP до поштової скриньки
-   [imapsetquota()](function.imap-set-quota.md) - Встановити квоту для заданої поштової скриньки
-   [imapgetquota()](function.imap-get-quota.md) - Отримати налаштування рівня квоти та статистику використання поштових скриньок
