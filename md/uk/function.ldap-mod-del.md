Видалити значення атрибута з поточних атрибутів

-   [« ldapmoddelext](function.ldap-mod_del-ext.html)
    
-   [ldapmodreplaceext »](function.ldap-mod_replace-ext.html)
    
-   [PHP Manual](index.html)
    
-   [Функції LDAP](ref.ldap.html)
    
-   Видалити значення атрибута з поточних атрибутів
    

# ldapmoddel

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapmoddel — Видалити атрибути з поточних атрибутів.

### Опис

```methodsynopsis
ldap_mod_del(    LDAP\Connection $ldap,    string $dn,    array $entry,    ?array $controls = null): bool
```

Видаляє один або більше атрибутів із зазначеного `dn`. Видалення об'єктів здійснюється функцією [ldapdelete()](function.ldap-delete.html)

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.html), що повертається функцією [ldapconnect()](function.ldap-connect.html)

`dn`

Відмінне ім'я об'єкта LDAP.

`entry`

`controls`

Масив [управляющих констант LDAP](ldap.controls.html) для відправки у запиті.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|  | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]` |
|  | Додано підтримку параметра `controls` |

### Дивіться також

-   [ldapmoddelext()](function.ldap-mod_del-ext.html) - Видалити значення атрибутів із поточних атрибутів
-   [ldapmodadd()](function.ldap-mod-add.html) - Додати значення атрибуту до поточних атрибутів
-   [ldapmodreplace()](function.ldap-mod-replace.html) - Замінити значення атрибутів на нові
-   [ldapmodifybatch()](function.ldap-modify-batch.html) - Формування та запуск пакетної зміни запису LDAP