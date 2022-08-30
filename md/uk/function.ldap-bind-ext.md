Прив'язати до директорії LDAP

-   [« ldapadd](function.ldap-add.html)
    
-   [ldapbind »](function.ldap-bind.html)
    
-   [PHP Manual](index.html)
    
-   [Функції LDAP](ref.ldap.html)
    
-   Прив'язати до директорії LDAP
    

# ldapbindext

(PHP 7> = 7.3.0, PHP 8)

ldapbindext — Прив'язати до директорії LDAP

### Опис

```methodsynopsis
ldap_bind_ext(    LDAP\Connection $ldap,    ?string $dn = null,    ?string $password = null,    ?array $controls = null): LDAP\Result|false
```

Робить те саме, що й [ldapbind()](function.ldap-bind.html), але повертає екземпляр [LDAPResult](class.ldap-result.html) для розбору за допомогою [ldapparseresult()](function.ldap-parse-result.html)

### Список параметрів

Дивіться [ldapbind()](function.ldap-bind.html)

### Значення, що повертаються

Повертає екземпляр [LDAPResult](class.ldap-result.html) або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                               |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|        | Повертає екземпляр [LDAPResult](class.ldap-result.html); раніше повертався ресурс ([resource](language.types.resource.html)                            |
|        | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]`                                                                      |

### Дивіться також

-   [ldapbind()](function.ldap-bind.html) - Прив'язати до LDAP директорії
-   [ldapparseresult()](function.ldap-parse-result.html) - Витягти інформацію з результату