Отримати настройки квоти для кожного користувача

-   [« imap\_get\_quota](function.imap-get-quota.html)
    
-   [imap\_getacl »](function.imap-getacl.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Отримати настройки квоти для кожного користувача
    

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

Екземпляр [IMAP\\Connection](class.imap-connection.html)

`mailbox`

`mailbox` має містити ім'я скриньки (наприклад, INBOX).

### Значення, що повертаються

Повертає масив цілих чисел, які стосуються конкретного користувача. Як ключі масиву використовуються імена ресурсів, а як значення масиви з ключами "limit" і "usage".

У разі виникнення помилки ця функція поверне **`false`** та масив інформації про з'єднання у разі отримання відповіді, яку вона не зможе розібрати.

### список змін

| Версия | Описание                                                                                                                                                 |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

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

-   [imap\_open()](function.imap-open.html) - Відкриває потік IMAP до поштової скриньки
-   [imap\_set\_quota()](function.imap-set-quota.html) - Встановити квоту для заданої поштової скриньки
-   [imap\_get\_quota()](function.imap-get-quota.html) - Отримати налаштування рівня квоти та статистику використання поштових скриньок