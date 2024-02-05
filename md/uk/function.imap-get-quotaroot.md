---
navigation:
  - function.imap-get-quota.md: « imap\_get\_quota
  - function.imap-getacl.md: imap\_getacl »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_get\_quotaroot
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_get\_quotaroot

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

imap\_get\_quotaroot — Отримує параметри квоти для кожного користувача

### Опис

```methodsynopsis
imap_get_quotaroot(IMAP\Connection $imap, string $mailbox): array|false
```

Повертає параметри квоти для кожного користувача. Число з ключем limit визначає максимальний допустимий розмір скриньки. Число з ключем usage визначає поточний рівень використання.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`mailbox`

`mailbox` має містити ім'я скриньки (наприклад, INBOX).

### Значення, що повертаються

Повертає масив цілих чисел, які стосуються конкретного користувача. Як ключі масиву використовуються імена ресурсів, а як значення масиви з ключами limit і usage.

У разі виникнення помилки ця функція поверне **`false`** та масив інформації про з'єднання у разі отримання відповіді, яку вона не зможе розібрати.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Приклади

**Пример #1 Пример использования**imap\_get\_quotaroot()\*\*\*\*

```php
<?php
$mbox = imap_open("{imap.example.org}", "kalowsky", "password", OP_HALFOPEN)
      or die("не удалось подключиться: " . imap_last_error());

$quota = imap_get_quotaroot($mbox, "INBOX");
if (is_array($quota)) {
   $storage = $quota['STORAGE'];
   echo "Уровень использования STORAGE: " .  $storage['usage'];
   echo "Максимальный размер STORAGE: " .  $storage['limit'];

   $message = $quota['MESSAGE'];
   echo "Уровень использования MESSAGE: " .  $message['usage'];
   echo "Максимальный размер MESSAGE: " .  $message['limit'];

   /* ...  */

}

imap_close($mbox);
?>
```

### Примітки

Ця функція доступна лише під час використання бібліотеки c-client2000 або новішої.

Заданий потік `imap` повинен бути відкритий під користувачем, чию скриньку ви хочете перевірити.

### Дивіться також

-   [imap\_open()](function.imap-open.md) \- Відкриває потік IMAP до поштової скриньки
-   [imap\_set\_quota()](function.imap-set-quota.md) \- Встановлює квоту для заданої поштової скриньки
-   [imap\_get\_quota()](function.imap-get-quota.md) \- Отримує налаштування рівня квоти та статистику використання поштових скриньок
