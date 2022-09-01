---
navigation:
  - function.imap-gc.html: « imapгк
  - function.imap-get-quotaroot.html: imapgetquotaroot »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imapgetquota
---
# imapgetquota

(PHP 4> = 4.0.5, PHP 5, PHP 7, PHP 8)

imapgetquota — Отримати налаштування рівня квоти та статистику використання поштових скриньок

### Опис

```methodsynopsis
imap_get_quota(IMAP\Connection $imap, string $quota_root): array|false
```

Повертає налаштування рівня квоти та статистику використання поштових скриньок.

Версія цієї функції для використання звичайними користувачами, не адміністраторами - [imapgetquotaroot()](function.imap-get-quotaroot.md)

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.md)

`quota_root`

`quota_root` має відповідати формату `user.name`, де name - ім'я скриньки, інформація щодо якої потрібна.

### Значення, що повертаються

Повертає асоціативний масив цілих чисел із ключами "limit" та "usage". Число із ключем "limit" визначає максимальний допустимий розмір скриньки. Число із ключем "usage" визначає поточний рівень використання. У разі виникнення помилки поверне **`false`**

Починаючи з PHP 4.3 і вище, функція більш точно відповідає стандарту, описаному в [» RFC2087](http://www.faqs.org/rfcs/rfc2087). Значення маси, що повертається, змінилося для підтримки необмеженої кількості ресурсів, що повертаються (тобто повідомлень або підпапок), де кожен іменований ресурс буде представлений індивідуальним масивом. Кожен елемент масиву міститиме інший масив до ключів "limit" та "usage".

Для забезпечення зворотної сумісності оригінальний метод доступу все ще доступний, хоча передбачається це виправити.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **imapgetquota()****

```php
<?php
$mbox = imap_open("{imap.example.org}", "mailadmin", "password", OP_HALFOPEN)
      or die("не удалось подключиться: " . imap_last_error());

$quota_value = imap_get_quota($mbox, "user.kalowsky");
if (is_array($quota_value)) {
    echo "Уровень использования: " . $quota_value['usage'];
    echo "Размер ящика: " . $quota_value['limit'];
}

imap_close($mbox);
?>
```

**Приклад #2 Приклад використання **imapgetquota()** у PHP 4.3 і вище**

```php
<?php
$mbox = imap_open("{imap.example.org}", "mailadmin", "password", OP_HALFOPEN)
      or die("не удалось подключиться: " . imap_last_error());

$quota_values = imap_get_quota($mbox, "user.kalowsky");
if (is_array($quota_values)) {
   $storage = $quota_values['STORAGE'];
   echo "Уровень использования STORAGE: " .  $storage['usage'];
   echo "Максимальный размер STORAGE: " .  $storage['limit'];

   $message = $quota_values['MESSAGE'];
   echo "Уровень использования MESSAGE: " .  $message['usage'];
   echo "Максимальный размер MESSAGE: " .  $message['limit'];

   /* ...  */
}

imap_close($mbox);
?>
```

### Примітки

Ця функція доступна лише під час використання бібліотеки c-client2000 або новішої.

Заданий потік `imap` має бути відкрито під адміністративним користувачем.

### Дивіться також

-   [imapopen()](function.imap-open.md) - Відкриває потік IMAP до поштової скриньки
-   [imapsetquota()](function.imap-set-quota.md) - Встановити квоту для заданої поштової скриньки
-   [imapgetquotaroot()](function.imap-get-quotaroot.md) - Отримати налаштування квоти для кожного користувача
