Видаляє запис із директорії LDAP

-   [« ldapdeleteext](function.ldap-delete-ext.html)
    
-   [ldapdn2ufn »](function.ldap-dn2ufn.html)
    
-   [PHP Manual](index.html)
    
-   [Функції LDAP](ref.ldap.html)
    
-   Видаляє запис із директорії LDAP
    

# ldapdelete

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapdelete — Видалення запису з директорії LDAP

### Опис

```methodsynopsis
ldap_delete(LDAP\Connection $ldap, string $dn, ?array $controls = null): bool
```

Видалення конкретного запису з директорії LDAP.

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.html), що повертається функцією [ldapconnect()](function.ldap-connect.html)

`dn`

Унікальне ім'я запису LDAP.

`controls`

Масив [управляющих констант LDAP](ldap.controls.html) для відправки у запиті.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                               |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|        | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]`                                                                      |
|        | Додано підтримку параметра `controls`                                                                                                                  |

### Дивіться також

-   [ldapdeleteext()](function.ldap-delete-ext.html) - Видалити запис із директорії
-   [ldapadd()](function.ldap-add.html) - Додати запис до LDAP директорії