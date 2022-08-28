Встановлення ACL для заданої поштової скриньки

-   [« imap\_set\_quota](function.imap-set-quota.html)
    
-   [imap\_setflag\_full »](function.imap-setflag-full.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Встановлення ACL для заданої поштової скриньки
    

# imapsetacl

(PHP 4> = 4.0.7, PHP 5, PHP 7, PHP 8)

imapsetacl — Встановлення ACL для заданої поштової скриньки

### Опис

```methodsynopsis
imap_setacl(    IMAP\Connection $imap,    string $mailbox,    string $user_id,    string $rights): bool
```

Встановлює ACL для заданої поштової скриньки.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.html)

`mailbox`

Ім'я поштової скриньки, докладніше дивіться в описі [imap\_open()](function.imap-open.html)

**Увага**

Якщо [imap.enable\_insecure\_rsh](imap.configuration.html#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

`user_id`

Ідентифікатор користувача, якому видаються права.

`rights`

Права для видачі. Передача порожнього рядка означає видалення всіх прав.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Примітки

На даний момент ця функція підтримується лише при використанні бібліотеки c-client2000 або новішої версії.

### Дивіться також

-   [imap\_getacl()](function.imap-getacl.html) - Отримати ACL для заданої поштової скриньки