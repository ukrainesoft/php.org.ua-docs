Встановлення ACL для заданої поштової скриньки

-   [« imapsetquota](function.imap-set-quota.html)
    
-   [imapsetflagfull »](function.imap-setflag-full.html)
    
-   [PHP Manual](index.md)
    
-   [Функции IMAP](ref.imap.md)
    
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

Екземпляр [IMAPConnection](class.imap-connection.html)

`mailbox`

Ім'я поштової скриньки, докладніше дивіться в описі [imapopen()](function.imap-open.html)

**Увага**

Якщо [imap.enableinsecurersh](imap.configuration.html#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

`user_id`

Ідентифікатор користувача, якому видаються права.

`rights`

Права для видачі. Передача порожнього рядка означає видалення всіх прав.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                             |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Примітки

На даний момент ця функція підтримується лише при використанні бібліотеки c-client2000 або новішої версії.

### Дивіться також

-   [imapgetacl()](function.imap-getacl.html) - Отримати ACL для заданої поштової скриньки