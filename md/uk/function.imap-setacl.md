---
navigation:
  - function.imap-set-quota.md: « imap\_set\_quota
  - function.imap-setflag-full.md: imap\_setflag\_full »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_setacl
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_setacl

(PHP 4 >= 4.0.7, PHP 5, PHP 7, PHP 8)

imap\_setacl — Встановлює ACL для заданої поштової скриньки

### Опис

```methodsynopsis
imap_setacl(    IMAP\Connection $imap,    string $mailbox,    string $user_id,    string $rights): bool
```

Встановлює ACL для заданої поштової скриньки.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`mailbox`

Ім'я поштової скриньки, докладніше дивіться в описі [imap\_open()](function.imap-open.md)

**Увага**

Якщо [imap.enable\_insecure\_rsh](imap.configuration.md#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

`user_id`

Ідентифікатор користувача, якому видаються права.

`rights`

Права для видачі. Передача порожнього рядка означає видалення всіх прав.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Примітки

На даний момент ця функція підтримується лише при використанні бібліотеки c-client2000 або новішої версії.

### Дивіться також

-   [imap\_getacl()](function.imap-getacl.md) \- Отримує ACL для заданої поштової скриньки
